# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Newest entries are added at the top.

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
