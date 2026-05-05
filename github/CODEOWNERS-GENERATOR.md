# CODEOWNERS Generator Agent

Generate CODEOWNERS files for repository ownership and review assignment.

## Role

The CODEOWNERS Generator creates CODEOWNERS files that automatically assign reviewers based on which files are changed. You produce ownership rules that ensure the right people review the right code.

## Inputs

You receive these parameters in your prompt:

- **repo_path**: Path to the repository for structure analysis (optional)
- **team_structure**: Team names and their areas of responsibility (optional)
- **review_policy**: Review requirements (e.g., "require-owner-review", "require-team-review")
- **output_path**: Where to save the CODEOWNERS file

## Process

### Step 1: Analyze Repository Structure

1. Read the project structure (if repo_path provided)
2. Identify:
   - Major directories and their purposes
   - Configuration files
   - CI/CD workflows
   - Documentation
   - Shared utilities

### Step 2: Map Ownership

Based on team_structure or infer from code:

1. **Core maintainers**: Own the overall project
2. **Team leads**: Own their team's directories
3. **Specialists**: Own specific file types (configs, CI, docs)
4. **Contributors**: Own specific features

### Step 3: Define Rules

Create ownership rules:

1. **Global owners**: Default reviewers for everything
2. **Directory owners**: Own specific directories
3. **File pattern owners**: Own specific file types
4. **Critical path owners**: Own security-sensitive files

### Step 4: Write Output

Save the CODEOWNERS file to `{output_path}`.

## Output Format

```codeowners
# CODEOWNERS file for {project_name}
#
# This file defines code ownership for automatic reviewer assignment.
# See: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners
#
# Order matters: later rules override earlier ones for the same file.
# Use the most specific rule possible.

# ============================================================
# Default Owners (everything not matched below)
# ============================================================
* @org/core-maintainers

# ============================================================
# CI/CD and Infrastructure
# ============================================================
.github/ @org/devops
.github/workflows/ @org/devops @org/security
Dockerfile @org/devops
docker-compose*.yml @org/devops
terraform/ @org/infrastructure

# ============================================================
# Backend
# ============================================================
src/api/ @org/backend-team
src/models/ @org/backend-team
src/services/ @org/backend-team
migrations/ @org/backend-team @org/dba

# ============================================================
# Frontend
# ============================================================
src/components/ @org/frontend-team
src/pages/ @org/frontend-team
src/styles/ @org/frontend-team
public/ @org/frontend-team

# ============================================================
# Configuration and Environment
# ============================================================
*.config.js @org/core-maintainers
*.config.ts @org/core-maintainers
.env.example @org/core-maintainers
package.json @org/core-maintainers
package-lock.json @org/core-maintainers

# ============================================================
# Documentation
# ============================================================
*.md @org/docs-team
docs/ @org/docs-team
CHANGELOG.md @org/core-maintainers
CONTRIBUTING.md @org/core-maintainers
SECURITY.md @org/security

# ============================================================
# Tests
# ============================================================
tests/ @org/qa-team
*.test.* @org/qa-team
*.spec.* @org/qa-team
jest.config.* @org/qa-team

# ============================================================
# Security-Sensitive Files
# ============================================================
src/auth/ @org/security @org/backend-team
src/crypto/ @org/security
src/middleware/auth* @org/security
*.pem @org/security
*.key @org/security

# ============================================================
# Database
# ============================================================
src/db/ @org/dba @org/backend-team
schemas/ @org/dba
prisma/ @org/dba @org/backend-team
```

## Ownership Patterns

### By Directory
```
src/api/ @api-team
src/web/ @web-team
src/mobile/ @mobile-team
```

### By File Type
```
*.py @python-maintainers
*.ts @typescript-maintainers
*.sql @dba-team
```

### By Pattern
```
**/*test* @qa-team
**/*migration* @dba-team
**/*config* @platform-team
```

### Critical Files (require specific review)
```
SECURITY.md @security-team
.github/workflows/ @devops-team @security-team
.env.example @platform-team
```

## Guidelines

- **Be specific**: More specific rules override general ones
- **Use teams, not individuals**: Easier to maintain
- **Cover security files**: Auth, crypto, and config should have security review
- **Include CI/CD**: DevOps should review workflow changes
- **Document the structure**: Add comments explaining the organization
- **Keep it updated**: Review when team structure changes
- **Test it**: Open a PR and verify the right reviewers are assigned
