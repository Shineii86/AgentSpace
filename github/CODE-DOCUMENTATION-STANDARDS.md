<!--
╔══════════════════════════════════════════════════════════╗
║  Project   : AgentSpace                                  ║
║  Template  : Code Documentation Standards                ║
║  Author    : Shineii86                                   ║
║  License   : MIT                                         ║
║  Repository: https://github.com/Shineii86/AgentSpace     ║
╚══════════════════════════════════════════════════════════╝
-->

# Code Documentation Standards

A reference template for writing well-documented, maintainable code. Use these conventions in any language to make codebases searchable, readable, and self-explaining.

---

## 1. File Header — Box-Style Comment

Every file starts with a block comment containing project metadata.

```
/**
 * ┌──────────────────────────────────────────────────────────┐
 * │  Project   : MyProject                                   │
 * │  Author    : Your Name <you@example.com>                 │
 * │  License   : MIT                                         │
 * │  File      : src/services/payment-processor.ts           │
 * │  Created   : 2026-05-06                                  │
 * └──────────────────────────────────────────────────────────┘
 */
```

**Rules:**
- One header per file, always at the very top
- Include: Project, Author, License, File path, Created date
- Keep box width consistent (60 chars inner)
- Use language-appropriate comment syntax (`/** */`, `#`, `<!-- -->`, `"""`)

---

## 2. Section Headers

Major sections within a file get a visual separator line.

```
// ==================== CONFIGURATION ====================
```

```
// ==================== PUBLIC API ====================
```

```
// ==================== INTERNAL HELPERS ====================
```

**Rules:**
- Use for top-level sections only (not every function)
- Full uppercase text inside the separator
- Consistent `=` padding to 60 chars
- One blank line before and after

**When to use:**
- Configuration / constants
- Type definitions
- Public API surface
- Internal implementation
- Error handling
- Initialization / bootstrap

---

## 3. Function-Level Comments

Every function gets a doc comment explaining **purpose**, **params**, and **return value**.

```typescript
/**
 * Process a payment through the configured gateway.
 *
 * Handles currency conversion, fraud checks, and retry logic
 * before submitting to the payment provider.
 *
 * @param {PaymentRequest} request - The payment details
 * @param {object} options - Optional config overrides
 * @param {number} options.maxRetries - Retry attempts (default: 3)
 * @param {boolean} options.skipFraudCheck - Bypass fraud scan
 * @returns {Promise<PaymentResult>} Transaction result with status
 * @throws {PaymentError} When gateway returns unrecoverable error
 *
 * @example
 * const result = await processPayment({
 *   amount: 4999,
 *   currency: 'USD',
 *   customerId: 'cus_abc123'
 * });
 */
async function processPayment(
  request: PaymentRequest,
  options: PaymentOptions = {}
): Promise<PaymentResult> {
  // ...
}
```

**Rules:**
- First line: one-sentence summary in plain English
- Blank line, then optional detailed explanation
- `@param` for every parameter — name, type, description
- `@returns` with type and what it contains
- `@throws` for any error the caller should handle
- `@example` for non-trivial functions
- Keep it honest — don't document what the code doesn't do

---

## 4. Inline Notes for Non-Obvious Logic

Add inline comments wherever the **why** isn't obvious from reading the code.

### Rate Limiting

```typescript
// ---- Rate limiting: token bucket algorithm ----
// Refill 1 token per 100ms, max 10 tokens burst
// Deliberately NOT using a sliding window — burst tolerance
// is required for the polling use case
const tokens = Math.min(
  this.maxTokens,
  this.lastTokens + elapsed * this.refillRate
);
```

### Deduplication

```typescript
// ---- Dedup: content-hash based ----
// We hash the normalized payload (not raw) because the same
// logical event can arrive with different casing/whitespace.
// SHA-256 truncated to 16 chars — collision rate < 0.001%
// at our expected volume (~10k events/day)
const hash = sha256(normalize(payload)).slice(0, 16);
if (this.seen.has(hash)) {
  this.metrics.increment('events.deduped');
  return;
}
```

### State Machines

```typescript
// ---- State machine: order lifecycle ----
// Valid transitions:
//   CREATED → PROCESSING → COMPLETED
//   CREATED → CANCELLED
//   PROCESSING → FAILED → PROCESSING (retry)
//   PROCESSING → CANCELLED (user abort)
//
// Invalid transitions are silently ignored — no error thrown.
// This is intentional: concurrent updates may race.
const VALID_TRANSITIONS: Record<string, string[]> = {
  CREATED:    ['PROCESSING', 'CANCELLED'],
  PROCESSING: ['COMPLETED', 'FAILED', 'CANCELLED'],
  FAILED:     ['PROCESSING'],
  COMPLETED:  [],
  CANCELLED:  [],
};
```

**Rules:**
- Start with `// ---- Topic ----` so it's searchable
- Explain **why**, not **what** (the code shows what)
- Reference algorithms, RFCs, or external docs when relevant
- Document edge cases and intentional oddities
- Note performance implications if non-obvious

---

## 5. Feature Markers

Tag every logical feature with a searchable comment so you can `grep` for it.

```typescript
// ---- FEATURE: AUTH ----
function validateToken(token: string): boolean { ... }

// ---- FEATURE: RATE LIMITING ----
class RateLimiter { ... }

// ---- FEATURE: WEBHOOK DELIVERY ----
async function deliverWebhook(url: string, payload: object) { ... }

// ---- FEATURE: RETRY LOGIC ----
function withRetry<T>(fn: () => Promise<T>, maxAttempts: number): Promise<T> { ... }

// ---- FEATURE: CIRCUIT BREAKER ----
class CircuitBreaker { ... }
```

**Rules:**
- Format: `// ---- FEATURE: NAME ----` (all caps, hyphenated)
- Place directly above the function/class/module it describes
- One marker per feature — don't duplicate
- Name should match how you'd search for it (`AUTH`, `RATE LIMITING`, `WEBHOOK DELIVERY`)
- Use consistent naming: noun or noun-phrase, not verbs

**Common patterns:**
```
// ---- FEATURE: CONFIGURATION ----
// ---- FEATURE: ERROR HANDLING ----
// ---- FEATURE: VALIDATION ----
// ---- FEATURE: CACHING ----
// ---- FEATURE: LOGGING ----
// ---- FEATURE: METRICS ----
// ---- FEATURE: HEALTH CHECK ----
// ---- FEATURE: GRACEFUL SHUTDOWN ----
```

---

## 6. Module/Class Footer

Every major class or module ends with a closing metadata block.

```typescript
// ═══════════════════════════════════════════════════════════
//  END: PaymentProcessor
//  Module   : src/services/payment-processor.ts
//  Depends  : GatewayClient, FraudDetector, RateLimiter
//  Exports  : processPayment, refundPayment, getPaymentStatus
//  Tests    : tests/services/payment-processor.test.ts
// ═══════════════════════════════════════════════════════════
```

**Rules:**
- Use for files with 100+ lines or exported classes
- Include: module name, file path, dependencies, exports, test file
- Use `═` double-line box style to distinguish from section headers
- Optional for small utility files (<50 lines)

---

## Quick Reference

| Element | Format | When to Use |
|---------|--------|-------------|
| File header | Box-style `/** */` block | Every file |
| Section header | `// ===== NAME =====` | Major sections (5-6 per file) |
| Function doc | `/** purpose + params + returns */` | Every function |
| Inline note | `// ---- Topic ----` explanation | Non-obvious logic |
| Feature marker | `// ---- FEATURE: NAME ----` | Every logical feature |
| Module footer | `// ═══ END: Name ═══` | Major classes/modules |

---

## Searching the Codebase

With these conventions, you can find anything with simple grep:

```bash
# Find all feature implementations
grep -rn "FEATURE: AUTH" src/

# Find all rate limiting logic
grep -rn "Rate limiting" src/

# Find all state machine definitions
grep -rn "State machine" src/

# List all module dependencies
grep -rn "Depends" src/

# Find all exported APIs
grep -rn "Exports" src/
```

---

<!-- ═══════════════════════════════════════════════════════════
     END OF Code Documentation Standards
     ═══════════════════════════════════════════════════════════
     Project  : AgentSpace
     Template : Code Documentation Standards
     License  : MIT
     File     : github/CODE-DOCUMENTATION-STANDARDS.md
     ═══════════════════════════════════════════════════════════ -->
