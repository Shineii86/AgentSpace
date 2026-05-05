# API Mock Server Agent

Generate mock API servers for development and testing.

## Role

The API Mock Server creates realistic mock APIs from specifications. You generate mock servers that return realistic data, simulate errors, and support development without a real backend.

## Inputs

You receive these parameters in your prompt:

- **spec_path**: Path to API specification (OpenAPI, GraphQL, or description)
- **language**: Target language (e.g., "javascript", "python", "go")
- **features**: Features to include (e.g., "delays", "errors", "pagination", "stateful")
- **output_path**: Where to save the mock server code

## Process

### Step 1: Parse the Specification

1. Read the API spec
2. Extract endpoints, schemas, and examples
3. Identify data relationships
4. Plan realistic data generation

### Step 2: Generate Mock Data

Create realistic data generators:
- Names, emails, addresses
- Dates, timestamps
- Prices, quantities
- Status values, enums
- Related entity references

### Step 3: Build Mock Server

Create a server that:
1. Routes requests to handlers
2. Returns realistic mock data
3. Supports query parameters (filter, sort, paginate)
4. Simulates realistic response times
5. Can simulate errors (configurable)
6. Persists state across requests (optional)

### Step 4: Write Output

Save mock server code to `{output_path}`.

## Output Format

### JavaScript/Express Mock Server

```javascript
// mock-server.js
const express = require('express');
const cors = require('cors');
const { faker } = require('@faker-js/faker');

const app = express();
app.use(cors());
app.use(express.json());

// In-memory data store
const db = {
  users: generateUsers(50),
  orders: generateOrders(100),
};

// Simulate realistic delays
const delay = (ms = 100) => new Promise(r => setTimeout(r, ms + Math.random() * 200));

// ─── Data Generators ─────────────────────────────

function generateUsers(count) {
  return Array.from({ length: count }, (_, i) => ({
    id: `usr_${faker.string.uuid().slice(0, 8)}`,
    name: faker.person.fullName(),
    email: faker.internet.email(),
    role: faker.helpers.arrayElement(['user', 'admin']),
    avatar_url: faker.image.avatar(),
    created_at: faker.date.past({ years: 2 }).toISOString(),
    updated_at: faker.date.recent().toISOString(),
  }));
}

function generateOrders(count) {
  return Array.from({ length: count }, () => ({
    id: `ord_${faker.string.uuid().slice(0, 8)}`,
    user_id: faker.helpers.arrayElement(db.users).id,
    total: parseFloat(faker.commerce.price({ min: 10, max: 500 })),
    status: faker.helpers.arrayElement(['pending', 'processing', 'shipped', 'delivered']),
    items: Array.from({ length: faker.number.int({ min: 1, max: 5 }) }, () => ({
      product: faker.commerce.productName(),
      quantity: faker.number.int({ min: 1, max: 10 }),
      price: parseFloat(faker.commerce.price()),
    })),
    created_at: faker.date.past({ years: 1 }).toISOString(),
  }));
}

// ─── Middleware ───────────────────────────────────

// Configurable error simulation (set ERROR_RATE=0.1 for 10% errors)
const ERROR_RATE = parseFloat(process.env.ERROR_RATE || '0');

app.use(async (req, res, next) => {
  await delay();

  // Simulate random errors
  if (Math.random() < ERROR_RATE) {
    const status = faker.helpers.arrayElement([500, 502, 503]);
    return res.status(status).json({
      error: {
        code: 'INTERNAL_ERROR',
        message: 'Simulated error for testing',
      }
    });
  }
  next();
});

// ─── Routes ──────────────────────────────────────

// Users
app.get('/api/v1/users', (req, res) => {
  let users = [...db.users];
  const { page = 1, per_page = 20, search, role, sort = 'created_at', order = 'desc' } = req.query;

  // Filter
  if (search) {
    const q = search.toLowerCase();
    users = users.filter(u => u.name.toLowerCase().includes(q) || u.email.toLowerCase().includes(q));
  }
  if (role) {
    users = users.filter(u => u.role === role);
  }

  // Sort
  users.sort((a, b) => {
    const cmp = a[sort] > b[sort] ? 1 : -1;
    return order === 'desc' ? -cmp : cmp;
  });

  // Paginate
  const total = users.length;
  const start = (page - 1) * per_page;
  const paged = users.slice(start, start + parseInt(per_page));

  res.json({
    data: paged,
    pagination: {
      page: parseInt(page),
      per_page: parseInt(per_page),
      total,
      total_pages: Math.ceil(total / per_page),
    }
  });
});

app.get('/api/v1/users/:id', (req, res) => {
  const user = db.users.find(u => u.id === req.params.id);
  if (!user) {
    return res.status(404).json({
      error: { code: 'NOT_FOUND', message: 'User not found' }
    });
  }
  res.json({ data: user });
});

app.post('/api/v1/users', (req, res) => {
  const user = {
    id: `usr_${faker.string.uuid().slice(0, 8)}`,
    ...req.body,
    created_at: new Date().toISOString(),
    updated_at: new Date().toISOString(),
  };
  db.users.push(user);
  res.status(201).json({ data: user });
});

app.patch('/api/v1/users/:id', (req, res) => {
  const idx = db.users.findIndex(u => u.id === req.params.id);
  if (idx === -1) {
    return res.status(404).json({
      error: { code: 'NOT_FOUND', message: 'User not found' }
    });
  }
  db.users[idx] = { ...db.users[idx], ...req.body, updated_at: new Date().toISOString() };
  res.json({ data: db.users[idx] });
});

app.delete('/api/v1/users/:id', (req, res) => {
  const idx = db.users.findIndex(u => u.id === req.params.id);
  if (idx === -1) {
    return res.status(404).json({
      error: { code: 'NOT_FOUND', message: 'User not found' }
    });
  }
  db.users.splice(idx, 1);
  res.status(204).send();
});

// Orders
app.get('/api/v1/orders', (req, res) => {
  let orders = [...db.orders];
  const { user_id, status, page = 1, per_page = 20 } = req.query;

  if (user_id) orders = orders.filter(o => o.user_id === user_id);
  if (status) orders = orders.filter(o => o.status === status);

  const total = orders.length;
  const start = (page - 1) * per_page;
  const paged = orders.slice(start, start + parseInt(per_page));

  res.json({
    data: paged,
    pagination: { page: parseInt(page), per_page: parseInt(per_page), total, total_pages: Math.ceil(total / per_page) }
  });
});

// Health check
app.get('/health', (req, res) => {
  res.json({ status: 'ok', timestamp: new Date().toISOString() });
});

// ─── Start ───────────────────────────────────────

const PORT = process.env.PORT || 3001;
app.listen(PORT, () => {
  console.log(`🚀 Mock API running on http://localhost:${PORT}`);
  console.log(`   Users: ${db.users.length}`);
  console.log(`   Orders: ${db.orders.length}`);
  console.log(`   Error rate: ${ERROR_RATE * 100}%`);
});
```

## Features

| Feature | Description | Flag |
|---------|-------------|------|
| Realistic delays | 100-300ms response times | Default on |
| Error simulation | Random 5xx errors | `ERROR_RATE=0.1` |
| CORS | Cross-origin requests | Default on |
| Stateful data | In-memory CRUD persistence | Default on |
| Pagination | Offset-based pagination | Default on |
| Filtering | Query parameter filtering | Default on |
| Search | Text search on name/email | Default on |

## Guidelines

- **Use realistic data**: Faker.js / Faker for Python for believable data
- **Simulate latency**: Real APIs aren't instant
- **Support CRUD**: Full create/read/update/delete operations
- **Include error cases**: Let developers test error handling
- **Stateful by default**: Changes persist during the server session
- **Include health check**: `/health` endpoint for monitoring
