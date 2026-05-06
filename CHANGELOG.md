# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Newest entries are added at the top.

## [1.13.0] - 2026-05-06

### Changed

#### Brutalist Website Redesign (`index.html`)
- Complete rewrite matching Fragment API reference design language
- Warm light theme: `#f5f0e8` background, `#1a1a1a` text, `#ffcc00` accent, `#e63b2e` secondary, `#0055ff` tertiary
- Space Grotesk for all headlines (black weight, uppercase, tight tracking)
- Inter for body text
- Thick 4px borders on all cards, nav, footer, sections
- Hard drop shadows (`4px 4px 0 #1a1a1a` / `8px 8px 0 #1a1a1a`)
- Active state: `translateY(1px) translateX(1px)` with shadow removal
- Hero: massive 96px uppercase headline with drop-shadow accent text
- Hero description with left accent border and rotated highlight span
- Feature cards with decorative glow circles that scale on hover
- Code block with terminal chrome (red/yellow/blue dots), yellow shadow
- CTA section with rotated card that straightens on hover
- Stats bar with border-separated counters
- Footer: dark `#1a1a1a` background, yellow logo, red hover links
- Fixed nav with bold uppercase links, active bottom-border highlight
- Mobile menu with left-border accent on open
- All SVG icons, zero emojis
- All contributors under @Shineii86

---

## [1.12.0] - 2026-05-06

### Changed

#### Complete Website Redesign (`index.html`)
- Full visual overhaul with polished, production-grade design
- Replaced all emoji icons with inline SVG icons throughout (categories, features, navigation, footer, usage section)
- Added dedicated SVG icon system with consistent sizing (icon, icon-sm, icon-lg, icon-xl)
- New multi-column footer with brand description, project links, community links, and resources
- Proper copyright notice: "© 2026 Shineii86. All rights reserved. Licensed under the MIT License."
- Added green pulse indicator for "Auto-synced from GitHub" status
- Added "Usage" section with three cards: With Any LLM, With OpenClaw, As Templates
- Added call-to-action (CTA) section with gradient background
- Enhanced navigation with animated underline on hover and mobile menu button
- Refined hero section with larger typography and improved spacing
- Improved card hover states with smoother cubic-bezier transitions
- Added OG meta tags for better social sharing (og:url, og:title, og:description)
- Added author meta tag
- Footer column headings: Project, Community, Resources
- All contributors credited under @Shineii86
- Responsive design preserved with mobile-friendly adjustments
- Zero emojis — pure SVG icons for a professional aesthetic

---

## [1.11.0] - 2026-05-06

### Added

#### Auto-Synced Website (`index.html`)
- Dark glassmorphism design matching hero banner aesthetic
- Auto-fetches all agents from GitHub API on page load — zero manual updates
- Hero section with live stats (agent count, category count, GitHub stars)
- 14 category cards with accent-colored left bars and agent listings
- Grid background + nebula glow effects
- Sticky navbar with blur backdrop
- Agent definition format section with syntax highlighting
- Feature cards (Copy & Paste, Customizable, Composable, Consistent Structure)
- Footer with copyright, links, and "Auto-synced from GitHub" indicator
- Responsive design (mobile-friendly)
- GitHub Pages enabled at https://shineii86.github.io/AgentSpace/

---

## [1.10.0] - 2026-05-06

### Changed

#### Complete SVG Banner Redesign — All 15 Banners

**Hero Banner (`assets/banners/hero.svg`)**
- New deep space background (#020617 dark / #f8fafc light)
- Grid pattern overlay with subtle lines
- Neural network constellation (12 nodes, 15 connection lines)
- Animated dashed connections with moving stroke-dashoffset
- Floating particles + orbiting particles on each node
- Staggered ring expand animations
- 18 twinkling stars with varied timing
- Gradient title (#6366f1 → #ec4899 → #f59e0b) with shimmer
- Tag pills: 101 Agents, 14 Categories, MIT License, Any LLM Ready

**All 14 Category Banners**
- Unified design system matching hero aesthetic
- Geometric constellation (5 nodes, 7 lines, 2 dashed) in right area
- Animated floating + orbiting particles on constellation nodes
- 6 twinkling stars with staggered animation
- Radial nebula gradient clouds (dual per banner)
- Glow filter (feGaussianBlur + feMerge) on animated dots
- Card: deep space glassmorphism (#020617 / #f8fafc)
- New per-category accent colors

---

## [1.9.1] - 2026-05-06

### Changed

#### SVG Banners — Style Consistency Fix
All 6 new category banners redesigned to match existing v1.8.0 banner style:
- Changed from 800×200 dark-only to 1200×100 with `@media (prefers-color-scheme: light/dark)` auto-switching
- Added glassmorphism card, left accent bar, animated floating dots, bottom shimmer line
- Added emoji icon, agent count badge pill, separator line, ambient glow orbs

#### README — All Sections to List Format
Converted all 14 category sections (including original 8) from HTML tables to clean list format:
- `- [**AGENT-NAME**](path) — Description` style for better readability
- Italicized category descriptions instead of blockquote `>` format

---

## [1.9.0] - 2026-05-06

### Added

#### New Categories (6 new categories, 36 new agents)

**🌐 Web & Frontend** (`web-frontend/`)
- `CSS-ARCHITECT.md` — Design scalable CSS architectures (BEM, ITCSS, utility-first, design tokens, theming)
- `REACT-ENGINEER.md` — Build production-grade React applications with hooks, server components, TypeScript
- `ACCESSIBILITY-AUDITOR.md` — Audit web interfaces for WCAG 2.2 AA/AAA compliance
- `PERFORMANCE-OPTIMIZER.md` — Diagnose and fix Core Web Vitals (LCP, INP, CLS)
- `RESPONSIVE-DESIGNER.md` — Design fluid responsive layouts with CSS Grid, Flexbox, container queries
- `DESIGN-SYSTEM-BUILDER.md` — Build scalable design systems with tokens, components, documentation

**🗄️ Backend** (`backend/`)
- `API-SERVER-BUILDER.md` — Build production-ready API servers with clean architecture and observability
- `DATABASE-ENGINEER.md` — Design schemas, optimize queries, write migrations for SQL/NoSQL
- `AUTH-ARCHITECT.md` — Design auth systems (OAuth 2.0, JWT, RBAC/ABAC, MFA, SSO)
- `MICROSERVICE-ARCHITECT.md` — Design microservice architectures with bounded contexts and resilience
- `CACHING-STRATEGIST.md` — Design multi-layer caching strategies (browser, CDN, app, database)
- `MIDDLEWARE-DESIGNER.md` — Design reusable middleware pipelines for cross-cutting concerns

**🖥️ Systems** (`systems/`)
- `SHELL-SCRIPTER.md` — Write robust, portable shell scripts with proper error handling and safety
- `LINUX-ADMIN.md` — Manage Linux systems: packages, services, users, networking, security hardening
- `NETWORK-ENGINEER.md` — Design and troubleshoot network infrastructure (DNS, LB, firewalls, VPNs)
- `CONTAINER-SPECIALIST.md` — Build optimized Docker images, manage orchestration and security
- `SYSTEMD-ENGINEER.md` — Design systemd services, timers, socket activation, resource controls
- `LOG-ANALYZER.md` — Analyze system/application/security logs with pattern detection and root cause analysis

**📊 Data & Query** (`data-query/`)
- `SQL-ENGINEER.md` — Write optimized SQL queries, analyze execution plans, design schemas
- `ETL-DESIGNER.md` — Design ETL/ELT data pipelines with quality checks and monitoring
- `DATA-MODELER.md` — Design conceptual, logical, and physical data models (ERDs, normalization)
- `GRAPHQL-ARCHITECT.md` — Design GraphQL schemas, resolvers, federation, pagination, authorization
- `TIME-SERIES-ANALYST.md` — Analyze temporal data, design time-series storage, detect anomalies
- `SEARCH-ENGINEER.md` — Design full-text search with Elasticsearch/OpenSearch, autocomplete, relevance tuning

**⚙️ Scripting & Automation** (`scripting-automation/`)
- `TASK-RUNNER.md` — Design task automation with Make, Just, Taskfile (dependency tracking, parallel execution)
- `CI-CD-ENGINEER.md` — Design CI/CD pipelines with testing, deployment strategies, caching, rollback
- `WORKFLOW-AUTOMATOR.md` — Automate workflows and integrations with webhooks, error handling, monitoring
- `CRON-SCHEDULER.md` — Design reliable scheduled tasks (timezone handling, idempotency, overlap prevention)
- `CLI-BUILDER.md` — Build user-friendly CLI tools with argument parsing, help systems, progress indicators
- `TEMPLATE-ENGINE.md` — Design code generation, scaffolding, and template systems

**📝 Config / Markup / Data Formats** (`config-formats/`)
- `YAML-SPECIALIST.md` — Write and validate YAML for Kubernetes, Docker Compose, CI/CD, Ansible, Helm
- `JSON-ARCHITECT.md` — Design JSON structures, JSON Schema definitions, jq transformations
- `TOML-EXPERT.md` — Write TOML configs for Cargo, pyproject.toml, modern CLI tools
- `MARKDOWN-ENGINEER.md` — Write structured Markdown with Mermaid diagrams, tables, cross-references
- `ENV-CONFIG-MANAGER.md` — Design environment configs, .env files, secret management, feature flags
- `XML-HTML-SPECIALIST.md` — Write and validate XML/HTML, schema design (XSD/DTD), XSLT transforms

#### Banners (6 new category banners matching v1.8.0 style)
- `assets/banners/web-frontend.svg` — Indigo/purple accent gradient
- `assets/banners/backend.svg` — Green/emerald accent gradient
- `assets/banners/systems.svg` — Red/rose accent gradient
- `assets/banners/data-query.svg` — Amber/gold accent gradient
- `assets/banners/scripting-automation.svg` — Purple/violet accent gradient
- `assets/banners/config-formats.svg` — Cyan/teal accent gradient
- All banners: 1200×100, dark/light theme support, glassmorphism, animated dots, shimmer line

#### Documentation
- `README.md` — Updated agent count (65 → 101), category count (8 → 14), added 6 new category sections with full agent tables
- `assets/banners/` — 6 new category banners with animated particles and glassmorphism cards

---

## [1.8.0] - 2026-05-06

### Changed

#### SVG Banners — Complete Redesign

All 9 SVG banners redesigned with professional-grade visuals:

**Hero Banner (`assets/banners/hero.svg`)**
- Animated floating particles with pulse animations
- Ambient glow orbs with blur effects
- Grid pattern overlay for depth
- Gradient accent bar (blue → purple → pink → orange)
- Tag pills: 59 Agents, 8 Categories, MIT License, Copy & Paste, Any LLM Ready, Composable
- Glassmorphism card with frosted background
- Animated shimmer on accent underline

**Category Banners (8 files)**
- Theme-aware: `@media (prefers-color-scheme: light/dark)` for automatic dark/light switching
- Glassmorphism cards with translucent backgrounds
- Left accent gradient bar per category
- Agent count badge pills
- Animated floating dots with staggered pulse timing
- Bottom accent shimmer line
- Ambient glow orbs with blur filters

**Files Changed:**
- `assets/banners/hero.svg` — Full redesign with animations (2,133 → 7,589 bytes)
- `assets/banners/evaluation.svg` — Orange/pink gradient theme
- `assets/banners/development.svg` — Green/blue gradient theme
- `assets/banners/content.svg` — Purple/pink gradient theme
- `assets/banners/research.svg` — Blue/green gradient theme
- `assets/banners/operations.svg` — Orange/gold gradient theme
- `assets/banners/communication.svg` — Pink/purple gradient theme
- `assets/banners/github.svg` — Gray/blue gradient theme
- `assets/banners/api.svg` — Green/orange gradient theme

---

## [1.7.0] - 2026-05-06

### Added

- `github/CODE-DOCUMENTATION-STANDARDS.md` — Reference template for writing well-documented, maintainable code
  - File header box-style comment format (Project, Author, License)
  - Section header conventions (`// ===== SECTION NAME =====`)
  - Function-level doc comment standards (Purpose, Params, Returns, Throws, Example)
  - Inline note patterns for non-obvious logic (Rate Limiting, Dedup, State Machines)
  - Feature marker system (`// ---- FEATURE: NAME ----`) for grep-ability
  - Module/class footer format with dependency and export tracking
  - Quick reference table and search examples

---

## [1.6.0] - 2026-05-06

### Added

#### API Agents (NEW CATEGORY)
- `api/API-DESIGNER.md` — Design REST, GraphQL, and gRPC API schemas and contracts
- `api/API-BUILDER.md` — Generate production-ready API server code from specifications
- `api/API-SCRAPER.md` — Scrape websites and data sources to create structured APIs
- `api/API-TESTER.md` — Generate comprehensive API test suites (functional, contract, performance)
- `api/API-MOCK.md` — Create mock API servers with realistic data for development
- `api/API-CLIENT.md` — Generate type-safe SDK/client libraries from API specs
- `api/API-TRANSFORMER.md` — Transform data between API formats, protocols, and schemas
- `api/API-GATEWAY.md` — Design API gateway configurations (Kong, Nginx, AWS)
- `api/API-MIGRATION.md` — Migrate between API versions, formats, and protocols
- `api/API-MONITOR.md` — Design API monitoring, alerting, and observability setups
- `api/API-SECURITY.md` — Audit and harden API security (OWASP API Top 10)
- `api/API-DOCUMENTATION.md` — Generate interactive API documentation (Redoc, Swagger)

#### Documentation
- `README.md` — Added API category with full agent table
- `assets/banners/api.svg` — New category banner

---

## [1.5.0] - 2026-05-06

### Added

#### Development Agents (NEW)
- `development/SECURITY-AUDITOR.md` — Comprehensive security audits for codebases (injection, auth, crypto, config)
- `development/ARCHITECTURE.md` — Architecture Decision Records (ADRs), design docs, and RFCs

#### Operations Agents (NEW)
- `operations/POSTMORTEM.md` — Blameless incident postmortems with root cause analysis and action items

#### Content Agents (NEW)
- `content/SOCIAL-MEDIA.md` — Platform-optimized social media posts (Twitter/X, LinkedIn, Reddit, Discord)

#### Research Agents (NEW)
- `research/COMPETITIVE-ANALYSIS.md` — Competitor analysis with feature comparison, SWOT, and market positioning

#### Evaluation Agents (NEW)
- `evaluation/A-B-TESTER.md` — A/B test design with sample size calculation, metrics, and statistical analysis

#### Documentation
- `README.md` — Updated all category tables with new agents

---

## [1.4.0] - 2026-05-06

### Added

#### GitHub Agents (NEW)
- `github/MARKDOWN-GUIDE.md` — Generate GitHub Flavored Markdown cheatsheets and guides
- `github/PROFILE-OPTIMIZER.md` — Generate optimized GitHub profile READMEs with stats widgets
- `github/API-REFERENCE.md` — Generate comprehensive API reference documentation
- `github/ARCHITECTURE-DIAGRAM.md` — Generate Mermaid diagrams for system architecture and data flows
- `github/OPEN-SOURCE-GUIDE.md` — Generate guides for open source maintainers and communities

#### Documentation
- `README.md` — Updated GitHub category with new agents and documentation sub-section

---

## [1.3.0] - 2026-05-06

### Added

- `assets/banners/hero.svg` — Main header with gradient glow effect and tagline
- `assets/banners/evaluation.svg` — Orange/coral category banner
- `assets/banners/development.svg` — Green/blue category banner
- `assets/banners/content.svg` — Purple/pink category banner
- `assets/banners/research.svg` — Blue/green category banner
- `assets/banners/operations.svg` — Orange/gold category banner
- `assets/banners/communication.svg` — Pink/purple category banner
- `assets/banners/github.svg` — Gray/blue category banner

### Changed
- `README.md` — Integrated SVG banners above each category section

---

## [1.2.0] - 2026-05-06

### Added

#### GitHub Agents (NEW)
- `github/MIGRATION-GUIDE.md` — Generate version migration guides with step-by-step upgrade instructions
- `github/GITHUB-ACTIONS-AUDITOR.md` — Audit existing workflows for security, efficiency, best practices
- `github/REPO-SETUP.md` — Bootstrap new repos with essential config files (.gitignore, .editorconfig, LICENSE, CI)
- `github/LABEL-MANAGER.md` — Design label taxonomies for issues and PRs with colors and descriptions
- `github/FUNDING-SETUP.md` — Generate FUNDING.yml and open source monetization config
- `github/ISSUE-TRIAGER.md` — Automatically categorize, prioritize, and route GitHub issues
- `github/REPO-HEALTH.md` — Score and assess repository health across documentation, code quality, security, community
- `github/CONTRIBUTING-GUIDE.md` — Generate comprehensive contributing guidelines for open source projects
- `github/DEPENDENCY-AUDITOR.md` — Audit dependencies for vulnerabilities, licenses, and staleness
- `github/BADGE-GENERATOR.md` — Generate README badges for build status, coverage, version, and more

#### Documentation
- `README.md` — Updated GitHub category table with all 22 agents

---

## [1.1.0] - 2026-05-06

### Added

#### GitHub Agents (NEW)
- `github/COMMIT-MESSAGE.md` — Generate conventional commit messages from diffs
- `github/CHANGELOG-WRITER.md` — Generate structured changelogs from commits and PRs
- `github/CI-CD-WRITER.md` — Generate GitHub Actions workflows for CI/CD
- `github/SECURITY-POLICY.md` — Generate SECURITY.md and security documentation
- `github/CODEOWNERS-GENERATOR.md` — Generate CODEOWNERS files for review assignment
- `github/DISCUSSION-WRITER.md` — Generate GitHub Discussions posts for community

#### Documentation
- `README.md` — Updated GitHub category table with all 12 agents

---

## [1.0.0] - 2026-05-06

### Added

#### GitHub Agents (NEW)
- `github/README-WRITER.md` — Generate comprehensive README files for repositories
- `github/WIKI-WRITER.md` — Create structured wiki documentation for projects
- `github/DOCS-WRITER.md` — Generate technical documentation for codebases
- `github/RELEASE-WRITER.md` — Create polished release notes from changes and commits
- `github/PR-DESCRIPTION.md` — Generate clear, informative pull request descriptions
- `github/ISSUE-TEMPLATE.md` — Create structured issue templates for bug reports, feature requests, etc.

#### Evaluation Agents
- `evaluation/ANALYZER.md` — Post-hoc Analyzer agent for analyzing blind comparison results and generating improvement suggestions
- `evaluation/COMPARATOR.md` — Blind Comparator agent for unbiased output comparison using structured rubrics
- `evaluation/GRADER.md` — Grader agent for evaluating expectations against execution transcripts

#### Development Agents
- `development/CODER.md` — Coder agent for writing production-ready code from specifications
- `development/REVIEWER.md` — Code Reviewer agent for structured, actionable code reviews
- `development/DEBUGGER.md` — Debugger agent for systematic bug diagnosis and fixing
- `development/TESTER.md` — Test Writer agent for generating comprehensive test suites

#### Content Agents
- `content/WRITER.md` — Content Writer agent for generating high-quality written content
- `content/EDITOR.md` — Content Editor agent for reviewing and improving existing content
- `content/SUMMARIZER.md` — Summarizer agent for creating concise, accurate summaries
- `content/TRANSLATOR.md` — Translator agent for translating content between languages

#### Research Agents
- `research/RESEARCHER.md` — Researcher agent for conducting thorough, structured research
- `research/FACT-CHECKER.md` — Fact-Checker agent for verifying claims and statements
- `research/DATA-ANALYST.md` — Data Analyst agent for analyzing datasets and extracting insights

#### Operations Agents
- `operations/DEPLOYER.md` — Deployer agent for managing deployments with safety checks and rollback
- `operations/MONITOR.md` — Monitor agent for tracking system health and detecting anomalies
- `operations/SCHEDULER.md` — Scheduler agent for task scheduling and resource allocation

#### Communication Agents
- `communication/EMAIL-DRAFTER.md` — Email Drafter agent for composing professional emails
- `communication/MEETING-SUMMARIZER.md` — Meeting Summarizer agent for creating actionable meeting records

#### Documentation
- `README.md` — Complete project overview with category tables and usage guide
- `CONTRIBUTING.md` — Guidelines for adding new agents and improving existing ones
- `CHANGELOG.md` — This file, tracking all notable changes

### Changed
- Replaced minimal `README.md` (single line "# AgentSpace") with comprehensive documentation
- Organized project into 6 category folders: evaluation, development, content, research, operations, communication
- All agent definition files renamed to UPPERCASE for consistency with GitHub conventions (README, LICENSE, CHANGELOG style)

### Structure
```
AgentSpace/
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── evaluation/
│   ├── ANALYZER.md
│   ├── COMPARATOR.md
│   ├── GRADER.md
│   └── A-B-TESTER.md
├── development/
│   ├── CODER.md
│   ├── REVIEWER.md
│   ├── DEBUGGER.md
│   ├── TESTER.md
│   ├── SECURITY-AUDITOR.md
│   └── ARCHITECTURE.md
├── content/
│   ├── WRITER.md
│   ├── EDITOR.md
│   ├── SUMMARIZER.md
│   ├── TRANSLATOR.md
│   └── SOCIAL-MEDIA.md
├── research/
│   ├── RESEARCHER.md
│   ├── FACT-CHECKER.md
│   ├── DATA-ANALYST.md
│   └── COMPETITIVE-ANALYSIS.md
├── operations/
│   ├── DEPLOYER.md
│   ├── MONITOR.md
│   ├── SCHEDULER.md
│   └── POSTMORTEM.md
├── communication/
│   ├── EMAIL-DRAFTER.md
│   └── MEETING-SUMMARIZER.md
├── github/
│   ├── README-WRITER.md
│   ├── WIKI-WRITER.md
│   ├── DOCS-WRITER.md
│   ├── RELEASE-WRITER.md
│   ├── PR-DESCRIPTION.md
│   ├── ISSUE-TEMPLATE.md
│   ├── COMMIT-MESSAGE.md
│   ├── CHANGELOG-WRITER.md
│   ├── CI-CD-WRITER.md
│   ├── SECURITY-POLICY.md
│   ├── CODEOWNERS-GENERATOR.md
│   ├── DISCUSSION-WRITER.md
│   ├── MIGRATION-GUIDE.md
│   ├── GITHUB-ACTIONS-AUDITOR.md
│   ├── REPO-SETUP.md
│   ├── LABEL-MANAGER.md
│   ├── FUNDING-SETUP.md
│   ├── ISSUE-TRIAGER.md
│   ├── REPO-HEALTH.md
│   ├── CONTRIBUTING-GUIDE.md
│   ├── DEPENDENCY-AUDITOR.md
│   ├── BADGE-GENERATOR.md
│   ├── MARKDOWN-GUIDE.md
│   ├── PROFILE-OPTIMIZER.md
│   ├── API-REFERENCE.md
│   ├── ARCHITECTURE-DIAGRAM.md
│   ├── OPEN-SOURCE-GUIDE.md
│   └── CODE-DOCUMENTATION-STANDARDS.md
├── api/
│   ├── API-DESIGNER.md
│   ├── API-BUILDER.md
│   ├── API-SCRAPER.md
│   ├── API-TESTER.md
│   ├── API-MOCK.md
│   ├── API-CLIENT.md
│   ├── API-TRANSFORMER.md
│   ├── API-GATEWAY.md
│   ├── API-MIGRATION.md
│   ├── API-MONITOR.md
│   ├── API-SECURITY.md
│   └── API-DOCUMENTATION.md
└── assets/
    └── banners/
        ├── hero.svg
        ├── evaluation.svg
        ├── development.svg
        ├── content.svg
        ├── research.svg
        ├── operations.svg
        ├── communication.svg
        ├── github.svg
        └── api.svg
```
