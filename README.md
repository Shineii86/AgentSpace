<div align="center">

<img src="assets/banners/hero.svg" alt="AgentSpace" width="100%"/>

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![Agents: 101](https://img.shields.io/badge/Agents-101-brightgreen.svg?style=flat-square)](#-categories)
[![Categories: 14](https://img.shields.io/badge/Categories-14-orange.svg?style=flat-square)](#-categories)
[![GitHub Stars](https://img.shields.io/github/stars/Shineii86/AgentSpace?style=flat-square)](https://github.com/Shineii86/AgentSpace/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/Shineii86/AgentSpace?style=flat-square)](https://github.com/Shineii86/AgentSpace/issues)
[![GitHub Last Commit](https://img.shields.io/github/last-commit/Shineii86/AgentSpace?style=flat-square)](https://github.com/Shineii86/AgentSpace/commits/main)

*Every agent follows a consistent structure:*

***Role → Inputs → Process → Output Format → Guidelines***

</div>

## 📖 Table of Contents

- [Why AgentSpace?](#-why-agentspace)
- [Categories](#-categories)
  - [📊 Evaluation](#-evaluation)
  - [💻 Development](#-development)
  - [✍️ Content](#%EF%B8%8F-content)
  - [🔬 Research](#-research)
  - [⚙️ Operations](#%EF%B8%8F-operations)
  - [📨 Communication](#-communication)
  - [🐙 GitHub](#-github)
  - [🔌 API](#-api)
  - [🌐 Web & Frontend](#-web--frontend)
  - [🗄️ Backend](#%EF%B8%8F-backend)
  - [🖥️ Systems](#%EF%B8%8F-systems)
  - [📊 Data & Query](#-data--query)
  - [⚙️ Scripting & Automation](#%EF%B8%8F-scripting--automation)
  - [📝 Config / Markup / Data Formats](#-config--markup--data-formats)
- [Agent Definition Format](#-agent-definition-format)
- [Usage](#-usage)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🤔 Why AgentSpace?

Agent definitions are the **"source code"** of AI agents. They tell an AI:

> *What to do* • *How to do it* • *What the output should look like*

**AgentSpace** provides a library of **battle-tested agent definitions** you can:

- 📋 **Copy & paste** into any LLM system prompt
- 🔧 **Customize** for your specific use case
- 🧩 **Compose** multiple agents into complex workflows
- 📚 **Learn** structured prompt engineering patterns

---

## 📂 Categories

<div align="center">

| Category | Agents | Description |
|:---------|:------:|:------------|
| [📊 Evaluation](#-evaluation) | 4 | Judge, compare, grade, and experiment |
| [💻 Development](#-development) | 6 | Write, review, debug, test, audit, and architect |
| [✍️ Content](#%EF%B8%8F-content) | 5 | Create, edit, summarize, translate, and socialize |
| [🔬 Research](#-research) | 4 | Investigate, verify, analyze, and compete |
| [⚙️ Operations](#%EF%B8%8F-operations) | 4 | Deploy, monitor, schedule, and postmortem |
| [📨 Communication](#-communication) | 2 | Draft emails and summarize meetings |
| [🐙 GitHub](#-github) | 27 | Full GitHub ecosystem coverage |
| [🔌 API](#-api) | 12 | Design, build, scrape, test, and document APIs |
| [🌐 Web & Frontend](#-web--frontend) | 6 | CSS, React, accessibility, performance, responsive design, design systems |
| [🗄️ Backend](#%EF%B8%8F-backend) | 6 | API servers, databases, auth, microservices, caching, middleware |
| [🖥️ Systems](#%EF%B8%8F-systems) | 6 | Shell scripting, Linux admin, networking, containers, systemd, log analysis |
| [📊 Data & Query](#-data--query) | 6 | SQL, ETL, data modeling, GraphQL, time series, search engines |
| [⚙️ Scripting & Automation](#%EF%B8%8F-scripting--automation) | 6 | Task runners, CI/CD, workflows, cron, CLI tools, templates |
| [📝 Config / Markup / Data Formats](#-config--markup--data-formats) | 6 | YAML, JSON, TOML, Markdown, environment config, XML/HTML |

</div>

---

<div align="center">
<img src="assets/banners/evaluation.svg" alt="Evaluation" width="100%"/>
</div>

### 📊 Evaluation

> *Agents for judging, comparing, and grading outputs.*

<table>
<tr>
<td width="30%"><strong><a href="evaluation/ANALYZER.md">ANALYZER</a></strong></td>
<td>Post-hoc analysis of blind comparison results. Examines why the winner won and generates actionable improvement suggestions for the loser.</td>
</tr>
<tr>
<td><strong><a href="evaluation/COMPARATOR.md">COMPARATOR</a></strong></td>
<td>Blind comparison of two outputs without bias. Uses structured rubrics (content + structure) to determine a winner based purely on quality.</td>
</tr>
<tr>
<td><strong><a href="evaluation/GRADER.md">GRADER</a></strong></td>
<td>Evaluate expectations against execution transcripts. Grades pass/fail with evidence, critiques weak evals, and surfaces hidden claims.</td>
</tr>
<tr>
<td><strong><a href="evaluation/A-B-TESTER.md">A-B-TESTER</a></strong></td>
<td>Design A/B tests with sample size calculation, metric selection, statistical analysis, and decision frameworks.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/development.svg" alt="Development" width="100%"/>
</div>

### 💻 Development

> *Agents for the full software development lifecycle.*

<table>
<tr>
<td width="30%"><strong><a href="development/CODER.md">CODER</a></strong></td>
<td>Write clean, production-ready code from specifications. Handles design, implementation, testing, and self-review in one pass.</td>
</tr>
<tr>
<td><strong><a href="development/REVIEWER.md">REVIEWER</a></strong></td>
<td>Structured code reviews covering correctness, security, performance, maintainability, and style. Produces actionable feedback with severity levels.</td>
</tr>
<tr>
<td><strong><a href="development/DEBUGGER.md">DEBUGGER</a></strong></td>
<td>Systematic bug diagnosis following a methodology: understand → reproduce → analyze → hypothesize → test → fix → prevent.</td>
</tr>
<tr>
<td><strong><a href="development/TESTER.md">TESTER</a></strong></td>
<td>Generate comprehensive test suites covering happy paths, edge cases, error conditions, and security scenarios.</td>
</tr>
<tr>
<td><strong><a href="development/SECURITY-AUDITOR.md">SECURITY-AUDITOR</a></strong></td>
<td>Comprehensive security audits for codebases. Scans for injection, auth flaws, data exposure, and crypto issues with remediation guidance.</td>
</tr>
<tr>
<td><strong><a href="development/ARCHITECTURE.md">ARCHITECTURE</a></strong></td>
<td>Generate Architecture Decision Records (ADRs), design docs, and RFCs that capture technical decisions and their rationale.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/content.svg" alt="Content" width="100%"/>
</div>

### ✍️ Content

> *Agents for creating, editing, and transforming written content.*

<table>
<tr>
<td width="30%"><strong><a href="content/WRITER.md">WRITER</a></strong></td>
<td>Generate high-quality content tailored to audience, tone, and format. Supports blog posts, docs, tutorials, emails, and reports.</td>
</tr>
<tr>
<td><strong><a href="content/EDITOR.md">EDITOR</a></strong></td>
<td>Review and improve existing content at structural, line, and proofreading levels. Preserves the author's voice while improving clarity.</td>
</tr>
<tr>
<td><strong><a href="content/SUMMARIZER.md">SUMMARIZER</a></strong></td>
<td>Create concise, accurate summaries. Supports executive, technical, bullet-point, and brief formats with configurable compression.</td>
</tr>
<tr>
<td><strong><a href="content/TRANSLATOR.md">TRANSLATOR</a></strong></td>
<td>Translate content between languages with cultural adaptation. Handles idioms, technical terms, and preserves formatting.</td>
</tr>
<tr>
<td><strong><a href="content/SOCIAL-MEDIA.md">SOCIAL-MEDIA</a></strong></td>
<td>Generate platform-optimized social media posts for Twitter/X, LinkedIn, Reddit, and Discord with engagement strategies.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/research.svg" alt="Research" width="100%"/>
</div>

### 🔬 Research

> *Agents for investigating topics, verifying claims, and analyzing data.*

<table>
<tr>
<td width="30%"><strong><a href="research/RESEARCHER.md">RESEARCHER</a></strong></td>
<td>Conduct thorough research from multiple sources. Produces structured reports with executive summary, findings, analysis, and citations.</td>
</tr>
<tr>
<td><strong><a href="research/FACT-CHECKER.md">FACT-CHECKER</a></strong></td>
<td>Verify claims with a 7-level rating system (TRUE → FALSE). Extracts implicit claims, checks logical validity, and flags misleading statements.</td>
</tr>
<tr>
<td><strong><a href="research/DATA-ANALYST.md">DATA-ANALYST</a></strong></td>
<td>Analyze datasets with descriptive, diagnostic, predictive, and comparative methods. Identifies patterns, anomalies, and actionable insights.</td>
</tr>
<tr>
<td><strong><a href="research/COMPETITIVE-ANALYSIS.md">COMPETITIVE-ANALYSIS</a></strong></td>
<td>Analyze competitors with feature comparison, pricing, SWOT analysis, and market positioning to inform strategy.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/operations.svg" alt="Operations" width="100%"/>
</div>

### ⚙️ Operations

> *Agents for deploying, monitoring, and managing infrastructure.*

<table>
<tr>
<td width="30%"><strong><a href="operations/DEPLOYER.md">DEPLOYER</a></strong></td>
<td>Manage deployments with pre-flight checks, rolling/blue-green/canary strategies, post-deployment verification, and automatic rollback.</td>
</tr>
<tr>
<td><strong><a href="operations/MONITOR.md">MONITOR</a></strong></td>
<td>Track system health across availability, latency, errors, and resources. Detects anomalies and generates severity-rated alerts.</td>
</tr>
<tr>
<td><strong><a href="operations/SCHEDULER.md">SCHEDULER</a></strong></td>
<td>Plan task schedules with dependency graphs, critical path analysis, resource allocation, and risk assessment.</td>
</tr>
<tr>
<td><strong><a href="operations/POSTMORTEM.md">POSTMORTEM</a></strong></td>
<td>Generate blameless incident postmortems with timeline reconstruction, 5-Whys root cause analysis, and action items.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/communication.svg" alt="Communication" width="100%"/>
</div>

### 📨 Communication

> *Agents for professional communication and meeting management.*

<table>
<tr>
<td width="30%"><strong><a href="communication/EMAIL-DRAFTER.md">EMAIL-DRAFTER</a></strong></td>
<td>Compose professional emails adapted to recipient, context, and goal. Supports follow-ups, requests, bad news, and introductions.</td>
</tr>
<tr>
<td><strong><a href="communication/MEETING-SUMMARIZER.md">MEETING-SUMMARIZER</a></strong></td>
<td>Transform raw meeting notes into structured records with decisions, action items, discussion summaries, and blockers.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/github.svg" alt="GitHub" width="100%"/>
</div>

### 🐙 GitHub

> *The largest category — 22 agents covering the complete GitHub ecosystem.*

#### 📝 Documentation & Content

<table>
<tr>
<td width="30%"><strong><a href="github/README-WRITER.md">README-WRITER</a></strong></td>
<td>Generate comprehensive README files with installation, usage, API reference, and contributing sections.</td>
</tr>
<tr>
<td><strong><a href="github/WIKI-WRITER.md">WIKI-WRITER</a></strong></td>
<td>Create structured wiki documentation with interconnected pages for architecture, guides, and references.</td>
</tr>
<tr>
<td><strong><a href="github/DOCS-WRITER.md">DOCS-WRITER</a></strong></td>
<td>Generate technical documentation including API references, tutorials, guides, and architecture docs.</td>
</tr>
<tr>
<td><strong><a href="github/CONTRIBUTING-GUIDE.md">CONTRIBUTING-GUIDE</a></strong></td>
<td>Create welcoming contributing guidelines with setup instructions, workflow, code standards, and PR process.</td>
</tr>
<tr>
<td><strong><a href="github/MIGRATION-GUIDE.md">MIGRATION-GUIDE</a></strong></td>
<td>Generate version migration guides with before/after code examples, automated tooling, and rollback instructions.</td>
</tr>
</table>

#### 🔄 Releases & Changelogs

<table>
<tr>
<td width="30%"><strong><a href="github/RELEASE-WRITER.md">RELEASE-WRITER</a></strong></td>
<td>Create polished release notes from commits and PRs. Categorizes changes, flags breaking changes, and credits contributors.</td>
</tr>
<tr>
<td><strong><a href="github/CHANGELOG-WRITER.md">CHANGELOG-WRITER</a></strong></td>
<td>Generate structured changelogs following Keep a Changelog format. Groups by Added/Changed/Fixed/Removed/Security.</td>
</tr>
<tr>
<td><strong><a href="github/COMMIT-MESSAGE.md">COMMIT-MESSAGE</a></strong></td>
<td>Generate conventional commit messages from diffs. Follows type(scope): description format with body and footer.</td>
</tr>
</table>

#### 🐛 Issues & PRs

<table>
<tr>
<td width="30%"><strong><a href="github/PR-DESCRIPTION.md">PR-DESCRIPTION</a></strong></td>
<td>Generate clear PR descriptions with summary, changes, testing instructions, and checklists.</td>
</tr>
<tr>
<td><strong><a href="github/ISSUE-TEMPLATE.md">ISSUE-TEMPLATE</a></strong></td>
<td>Create structured issue templates for bug reports, feature requests, security vulnerabilities, and questions.</td>
</tr>
<tr>
<td><strong><a href="github/ISSUE-TRIAGER.md">ISSUE-TRIAGER</a></strong></td>
<td>Automatically categorize, prioritize, and route issues. Checks completeness and suggests follow-up questions.</td>
</tr>
</table>

#### 🔧 CI/CD & Security

<table>
<tr>
<td width="30%"><strong><a href="github/CI-CD-WRITER.md">CI-CD-WRITER</a></strong></td>
<td>Generate GitHub Actions workflows for CI, CD, releases, and scheduled jobs. Includes caching, matrix builds, and security best practices.</td>
</tr>
<tr>
<td><strong><a href="github/GITHUB-ACTIONS-AUDITOR.md">GITHUB-ACTIONS-AUDITOR</a></strong></td>
<td>Audit existing workflows for security risks (unpinned actions, secret exposure), performance issues, and best practices.</td>
</tr>
<tr>
<td><strong><a href="github/SECURITY-POLICY.md">SECURITY-POLICY</a></strong></td>
<td>Generate SECURITY.md with reporting instructions, response timelines, disclosure policy, and safe harbor provisions.</td>
</tr>
<tr>
<td><strong><a href="github/CODEOWNERS-GENERATOR.md">CODEOWNERS-GENERATOR</a></strong></td>
<td>Generate CODEOWNERS files that automatically assign reviewers based on which files are changed.</td>
</tr>
<tr>
<td><strong><a href="github/DEPENDENCY-AUDITOR.md">DEPENDENCY-AUDITOR</a></strong></td>
<td>Audit dependencies for security vulnerabilities, license compliance, update status, and overall health.</td>
</tr>
</table>

#### 🏗️ Project Setup & Management

<table>
<tr>
<td width="30%"><strong><a href="github/REPO-SETUP.md">REPO-SETUP</a></strong></td>
<td>Bootstrap new repos with .gitignore, .editorconfig, LICENSE, CI workflows, issue templates, and Dependabot config.</td>
</tr>
<tr>
<td><strong><a href="github/REPO-HEALTH.md">REPO-HEALTH</a></strong></td>
<td>Score repository health across documentation, code quality, community, security, and maintenance dimensions.</td>
</tr>
<tr>
<td><strong><a href="github/LABEL-MANAGER.md">LABEL-MANAGER</a></strong></td>
<td>Design label taxonomies with consistent naming, meaningful colors, and clear descriptions for issues and PRs.</td>
</tr>
<tr>
<td><strong><a href="github/BADGE-GENERATOR.md">BADGE-GENERATOR</a></strong></td>
<td>Generate shields.io badges for build status, coverage, version, license, downloads, and community metrics.</td>
</tr>
<tr>
<td><strong><a href="github/FUNDING-SETUP.md">FUNDING-SETUP</a></strong></td>
<tr>
<td><strong><a href=github/MARKDOWN-GUIDE.md>MARKDOWN-GUIDE</a></strong></td>
<td>Generate GitHub Flavored Markdown cheatsheets, tutorials, and best practices guides.</td>
</tr>
<tr>
<td><strong><a href=github/PROFILE-OPTIMIZER.md>PROFILE-OPTIMIZER</a></strong></td>
<td>Generate optimized GitHub profile READMEs with stats widgets and tech stacks.</td>
</tr>
<tr>
<td><strong><a href=github/API-REFERENCE.md>API-REFERENCE</a></strong></td>
<td>Generate comprehensive API reference documentation with examples.</td>
</tr>
<tr>
<td><strong><a href=github/ARCHITECTURE-DIAGRAM.md>ARCHITECTURE-DIAGRAM</a></strong></td>
<td>Generate Mermaid diagrams for system architecture and data flows.</td>
</tr>
<tr>
<td><strong><a href=github/OPEN-SOURCE-GUIDE.md>OPEN-SOURCE-GUIDE</a></strong></td>
<td>Generate guides for open source maintainers, governance, and sustainability.</td>
</tr>
<td>Generate FUNDING.yml for GitHub Sponsors, Open Collective, Ko-fi, and other monetization platforms.</td>
</tr>
<tr>
<td><strong><a href="github/DISCUSSION-WRITER.md">DISCUSSION-WRITER</a></strong></td>
<td>Generate GitHub Discussions posts for announcements, proposals, Q&A, and community engagement.</td>
</tr>
</table>

---


---

<div align="center">
<img src="assets/banners/api.svg" alt="API" width="100%"/>
</div>

### 🔌 API

> *The complete API lifecycle — from design to deployment to monitoring.*

#### 📐 Design & Build

<table>
<tr>
<td width="30%"><strong><a href="api/API-DESIGNER.md">API-DESIGNER</a></strong></td>
<td>Design REST, GraphQL, and gRPC API schemas with contracts, validation rules, and error formats.</td>
</tr>
<tr>
<td><strong><a href="api/API-BUILDER.md">API-BUILDER</a></strong></td>
<td>Generate production-ready API server code from specs. Routes, handlers, validation, error handling, and tests.</td>
</tr>
<tr>
<td><strong><a href="api/API-CLIENT.md">API-CLIENT</a></strong></td>
<td>Generate type-safe SDK/client libraries from API specs. TypeScript, Python, Go, Java, Ruby.</td>
</tr>
<tr>
<td><strong><a href="api/API-MOCK.md">API-MOCK</a></strong></td>
<td>Create mock API servers with realistic data, delays, error simulation, and stateful CRUD.</td>
</tr>
</table>

#### 🕷️ Data & Scraping

<table>
<tr>
<td width="30%"><strong><a href="api/API-SCRAPER.md">API-SCRAPER</a></strong></td>
<td>Scrape websites, HTML tables, JSON-LD, and API docs to create structured, queryable APIs.</td>
</tr>
<tr>
<td><strong><a href="api/API-TRANSFORMER.md">API-TRANSFORMER</a></strong></td>
<td>Transform data between formats: REST↔GraphQL, SOAP↔REST, CSV↔JSON, flat↔nested.</td>
</tr>
<tr>
<td><strong><a href="api/API-MIGRATION.md">API-MIGRATION</a></strong></td>
<td>Migrate between API versions, formats, and protocols with compatibility layers and rollback plans.</td>
</tr>
</table>

#### 🔧 Infrastructure

<table>
<tr>
<td width="30%"><strong><a href="api/API-GATEWAY.md">API-GATEWAY</a></strong></td>
<td>Design API gateway configs for routing, auth, rate limiting, and observability (Kong, Nginx, AWS).</td>
</tr>
<tr>
<td><strong><a href="api/API-MONITOR.md">API-MONITOR</a></strong></td>
<td>Design monitoring with SLIs, SLOs, dashboards, alerts, and health check scripts.</td>
</tr>
<tr>
<td><strong><a href="api/API-SECURITY.md">API-SECURITY</a></strong></td>
<td>Audit and harden API security against OWASP API Top 10. Auth, validation, rate limiting, headers.</td>
</tr>
</table>

#### 📋 Testing & Documentation

<table>
<tr>
<td width="30%"><strong><a href="api/API-TESTER.md">API-TESTER</a></strong></td>
<td>Generate comprehensive test suites: functional, contract, edge cases, auth, and error handling.</td>
</tr>
<tr>
<td><strong><a href="api/API-DOCUMENTATION.md">API-DOCUMENTATION</a></strong></td>
<td>Generate interactive API docs with Redoc, Swagger, or custom platforms. Working examples included.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/web-frontend.svg" alt="Web & Frontend" width="100%"/>
</div>

### 🌐 Web & Frontend

> *Agents for building modern web interfaces — from CSS architecture to design systems.*

<table>
<tr>
<td width="30%"><strong><a href="web-frontend/CSS-ARCHITECT.md">CSS-ARCHITECT</a></strong></td>
<td>Design scalable, maintainable CSS architectures. BEM, ITCSS, utility-first, design tokens, theming strategies.</td>
</tr>
<tr>
<td><strong><a href="web-frontend/REACT-ENGINEER.md">REACT-ENGINEER</a></strong></td>
<td>Build production-grade React applications with hooks, server components, state management, and TypeScript.</td>
</tr>
<tr>
<td><strong><a href="web-frontend/ACCESSIBILITY-AUDITOR.md">ACCESSIBILITY-AUDITOR</a></strong></td>
<td>Audit and remediate web interfaces for WCAG 2.2 AA/AAA compliance. Keyboard, screen reader, color contrast.</td>
</tr>
<tr>
<td><strong><a href="web-frontend/PERFORMANCE-OPTIMIZER.md">PERFORMANCE-OPTIMIZER</a></strong></td>
<td>Diagnose and fix Core Web Vitals (LCP, INP, CLS). Bundle optimization, caching, loading strategies.</td>
</tr>
<tr>
<td><strong><a href="web-frontend/RESPONSIVE-DESIGNER.md">RESPONSIVE-DESIGNER</a></strong></td>
<td>Design fluid, responsive layouts with CSS Grid, Flexbox, container queries, and fluid typography.</td>
</tr>
<tr>
<td><strong><a href="web-frontend/DESIGN-SYSTEM-BUILDER.md">DESIGN-SYSTEM-BUILDER</a></strong></td>
<td>Build and maintain scalable design systems with tokens, components, documentation, and governance.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/backend.svg" alt="Backend" width="100%"/>
</div>

### 🗄️ Backend

> *Agents for server-side development — APIs, databases, authentication, and distributed systems.*

<table>
<tr>
<td width="30%"><strong><a href="backend/API-SERVER-BUILDER.md">API-SERVER-BUILDER</a></strong></td>
<td>Build production-ready API servers with clean architecture, middleware, validation, error handling, and observability.</td>
</tr>
<tr>
<td><strong><a href="backend/DATABASE-ENGINEER.md">DATABASE-ENGINEER</a></strong></td>
<td>Design schemas, optimize queries, write migrations, and manage database operations across SQL and NoSQL engines.</td>
</tr>
<tr>
<td><strong><a href="backend/AUTH-ARCHITECT.md">AUTH-ARCHITECT</a></strong></td>
<td>Design authentication and authorization systems. OAuth 2.0, JWT, RBAC/ABAC, MFA, social login, SSO.</td>
</tr>
<tr>
<td><strong><a href="backend/MICROSERVICE-ARCHITECT.md">MICROSERVICE-ARCHITECT</a></strong></td>
<td>Design microservice architectures with bounded contexts, communication patterns, resilience, and observability.</td>
</tr>
<tr>
<td><strong><a href="backend/CACHING-STRATEGIST.md">CACHING-STRATEGIST</a></strong></td>
<td>Design multi-layer caching strategies. Browser, CDN, application, and database caching with invalidation.</td>
</tr>
<tr>
<td><strong><a href="backend/MIDDLEWARE-DESIGNER.md">MIDDLEWARE-DESIGNER</a></strong></td>
<td>Design reusable middleware pipelines for auth, logging, validation, rate limiting, and error handling.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/systems.svg" alt="Systems" width="100%"/>
</div>

### 🖥️ Systems

> *Agents for system administration, infrastructure, and DevOps — from shell scripts to containers.*

<table>
<tr>
<td width="30%"><strong><a href="systems/SHELL-SCRIPTER.md">SHELL-SCRIPTER</a></strong></td>
<td>Write robust, portable shell scripts with proper error handling, argument parsing, and safety patterns.</td>
</tr>
<tr>
<td><strong><a href="systems/LINUX-ADMIN.md">LINUX-ADMIN</a></strong></td>
<td>Manage Linux systems: packages, services, users, networking, storage, and security hardening.</td>
</tr>
<tr>
<td><strong><a href="systems/NETWORK-ENGINEER.md">NETWORK-ENGINEER</a></strong></td>
<td>Design and troubleshoot network infrastructure. DNS, load balancing, firewalls, VPNs, TCP tuning.</td>
</tr>
<tr>
<td><strong><a href="systems/CONTAINER-SPECIALIST.md">CONTAINER-SPECIALIST</a></strong></td>
<td>Build optimized Docker images, manage orchestration, implement security hardening and health checks.</td>
</tr>
<tr>
<td><strong><a href="systems/SYSTEMD-ENGINEER.md">SYSTEMD-ENGINEER</a></strong></td>
<td>Design systemd services, timers, socket activation, resource controls, and security sandboxing.</td>
</tr>
<tr>
<td><strong><a href="systems/LOG-ANALYZER.md">LOG-ANALYZER</a></strong></td>
<td>Analyze system, application, and security logs. Pattern detection, anomaly identification, root cause analysis.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/data-query.svg" alt="Data & Query" width="100%"/>
</div>

### 📊 Data & Query

> *Agents for data engineering, querying, and analysis — SQL to search engines.*

<table>
<tr>
<td width="30%"><strong><a href="data-query/SQL-ENGINEER.md">SQL-ENGINEER</a></strong></td>
<td>Write optimized SQL queries, analyze execution plans, design schemas, and handle complex analytical queries.</td>
</tr>
<tr>
<td><strong><a href="data-query/ETL-DESIGNER.md">ETL-DESIGNER</a></strong></td>
<td>Design ETL/ELT data pipelines with extraction, transformation, loading, quality checks, and monitoring.</td>
</tr>
<tr>
<td><strong><a href="data-query/DATA-MODELER.md">DATA-MODELER</a></strong></td>
<td>Design conceptual, logical, and physical data models. ERDs, normalization, denormalization, data dictionaries.</td>
</tr>
<tr>
<td><strong><a href="data-query/GRAPHQL-ARCHITECT.md">GRAPHQL-ARCHITECT</a></strong></td>
<td>Design GraphQL schemas, resolvers, federation, pagination, authorization, and N+1 prevention.</td>
</tr>
<tr>
<td><strong><a href="data-query/TIME-SERIES-ANALYST.md">TIME-SERIES-ANALYST</a></strong></td>
<td>Analyze temporal data patterns, design time-series storage, detect anomalies, and build aggregations.</td>
</tr>
<tr>
<td><strong><a href="data-query/SEARCH-ENGINEER.md">SEARCH-ENGINEER</a></strong></td>
<td>Design full-text search with Elasticsearch/OpenSearch. Autocomplete, relevance tuning, faceting, and indexing.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/scripting-automation.svg" alt="Scripting & Automation" width="100%"/>
</div>

### ⚙️ Scripting & Automation

> *Agents for automating workflows, CI/CD pipelines, and developer productivity tooling.*

<table>
<tr>
<td width="30%"><strong><a href="scripting-automation/TASK-RUNNER.md">TASK-RUNNER</a></strong></td>
<td>Design task automation with Make, Just, Taskfile. Dependency tracking, self-documenting help, parallel execution.</td>
</tr>
<tr>
<td><strong><a href="scripting-automation/CI-CD-ENGINEER.md">CI-CD-ENGINEER</a></strong></td>
<td>Design CI/CD pipelines with testing, building, deployment strategies, gates, caching, and rollback.</td>
</tr>
<tr>
<td><strong><a href="scripting-automation/WORKFLOW-AUTOMATOR.md">WORKFLOW-AUTOMATOR</a></strong></td>
<td>Automate repetitive workflows and integrations. Webhooks, API connections, error handling, monitoring.</td>
</tr>
<tr>
<td><strong><a href="scripting-automation/CRON-SCHEDULER.md">CRON-SCHEDULER</a></strong></td>
<td>Design reliable scheduled tasks. Timezone handling, idempotency, overlap prevention, missed run recovery.</td>
</tr>
<tr>
<td><strong><a href="scripting-automation/CLI-BUILDER.md">CLI-BUILDER</a></strong></td>
<td>Build user-friendly CLI tools with argument parsing, help systems, error handling, and progress indicators.</td>
</tr>
<tr>
<td><strong><a href="scripting-automation/TEMPLATE-ENGINE.md">TEMPLATE-ENGINE</a></strong></td>
<td>Design code generation, scaffolding, and template systems for projects, components, and configurations.</td>
</tr>
</table>

---

<div align="center">
<img src="assets/banners/config-formats.svg" alt="Config / Markup / Data Formats" width="100%"/>
</div>

### 📝 Config / Markup / Data Formats

> *Agents for configuration languages, markup formats, and data interchange.*

<table>
<tr>
<td width="30%"><strong><a href="config-formats/YAML-SPECIALIST.md">YAML-SPECIALIST</a></strong></td>
<td>Write, validate, and optimize YAML for Kubernetes, Docker Compose, CI/CD, Ansible, and Helm.</td>
</tr>
<tr>
<td><strong><a href="config-formats/JSON-ARCHITECT.md">JSON-ARCHITECT</a></strong></td>
<td>Design JSON data structures, write JSON Schema definitions, and handle transformations with jq.</td>
</tr>
<tr>
<td><strong><a href="config-formats/TOML-EXPERT.md">TOML-EXPERT</a></strong></td>
<td>Write TOML configurations for Cargo, pyproject.toml, and modern CLI tools. Migrations and validation.</td>
</tr>
<tr>
<td><strong><a href="config-formats/MARKDOWN-ENGINEER.md">MARKDOWN-ENGINEER</a></strong></td>
<td>Write structured Markdown for docs, READMEs, and technical content. Mermaid diagrams, tables, cross-references.</td>
</tr>
<tr>
<td><strong><a href="config-formats/ENV-CONFIG-MANAGER.md">ENV-CONFIG-MANAGER</a></strong></td>
<td>Design environment configurations, .env files, secret management, and feature flag systems.</td>
</tr>
<tr>
<td><strong><a href="config-formats/XML-HTML-SPECIALIST.md">XML-HTML-SPECIALIST</a></strong></td>
<td>Write and validate XML/HTML. Schema design (XSD/DTD), XSLT transforms, semantic HTML5 markup.</td>
</tr>
</table>

---

## 📋 Agent Definition Format

Every agent in AgentSpace follows this **6-section structure**:

```markdown
# Agent Name

One-line description of what the agent does.

## Role
What the agent is responsible for and its core behavior.

## Inputs
Parameters the agent receives (names, types, descriptions).

## Process
Step-by-step methodology the agent follows (numbered steps).

## Output Format
JSON or Markdown template showing the expected output structure.

## Guidelines
Do's and don'ts, best practices, and edge cases.
```

**Why this format works:**
- 🎯 **Role** sets clear boundaries — what the agent does and doesn't do
- 📥 **Inputs** make agents composable — you know exactly what to pass in
- 🔄 **Process** ensures consistency — same methodology every time
- 📤 **Output Format** enables automation — structured, predictable outputs
- 📏 **Guidelines** encode expertise — best practices and gotchas

---

## 🛠️ Usage

### With OpenClaw
Agent definitions can be loaded as skill prompts. Point your agent at the definition file and provide the required inputs.

### With Any LLM
Copy the agent definition into your system prompt or use it as a template for your own agents.

### As Templates
Each agent is a starting point — customize the process, add domain-specific steps, or combine multiple agents into workflows.

### Customization
1. 🍴 **Fork** this repository
2. ✏️ **Modify** existing agents to match your needs
3. ➕ **Add** new agents following the [standard format](#-agent-definition-format)
4. 📬 **Submit a PR** to share with the community

---

## 📝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Ways to contribute:**
- 🐛 Report issues with existing agents
- 💡 Suggest new agent types
- ✏️ Improve existing agent definitions
- 📚 Add documentation and examples
- 🧪 Share how you use AgentSpace agents

---

## 📄 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

---

<div align="center">

**Built with ❤️ for the AI agent community**

[⬆ Back to top](#-agentspace)

</div>
