# Changelog

All notable changes to this project will be documented in this file.

Newest entries are added at the top.

## [2026-05-06] — Added GitHub Category & Renamed All Files to UPPERCASE

### Added

#### GitHub Agents (NEW)
- `github/README-WRITER.md` — Generate comprehensive README files for repositories
- `github/WIKI-WRITER.md` — Create structured wiki documentation for projects
- `github/DOCS-WRITER.md` — Generate technical documentation for codebases
- `github/RELEASE-WRITER.md` — Create polished release notes from changes and commits
- `github/PR-DESCRIPTION.md` — Generate clear, informative pull request descriptions
- `github/ISSUE-TEMPLATE.md` — Create structured issue templates for bug reports, feature requests, etc.

### Changed

#### File Renames (UPPERCASE)
All agent definition files renamed to UPPERCASE for consistency with GitHub conventions (README, LICENSE, CHANGELOG style):

**Evaluation:**
- `evaluation/analyzer.md` → `evaluation/ANALYZER.md`
- `evaluation/comparator.md` → `evaluation/COMPARATOR.md`
- `evaluation/grader.md` → `evaluation/GRADER.md`

**Development:**
- `development/coder.md` → `development/CODER.md`
- `development/reviewer.md` → `development/REVIEWER.md`
- `development/debugger.md` → `development/DEBUGGER.md`
- `development/tester.md` → `development/TESTER.md`

**Content:**
- `content/writer.md` → `content/WRITER.md`
- `content/editor.md` → `content/EDITOR.md`
- `content/summarizer.md` → `content/SUMMARIZER.md`
- `content/translator.md` → `content/TRANSLATOR.md`

**Research:**
- `research/researcher.md` → `research/RESEARCHER.md`
- `research/fact-checker.md` → `research/FACT-CHECKER.md`
- `research/data-analyst.md` → `research/DATA-ANALYST.md`

**Operations:**
- `operations/deployer.md` → `operations/DEPLOYER.md`
- `operations/monitor.md` → `operations/MONITOR.md`
- `operations/scheduler.md` → `operations/SCHEDULER.md`

**Communication:**
- `communication/email-drafter.md` → `communication/EMAIL-DRAFTER.md`
- `communication/meeting-summarizer.md` → `communication/MEETING-SUMMARIZER.md`

#### Documentation
- `README.md` — Updated with GitHub category table and UPPERCASE file references

---

## [2026-05-06] — Initial Repository Restructuring

### Added

#### Evaluation Agents
- `evaluation/ANALYZER.md` — Post-hoc Analyzer agent for analyzing blind comparison results
- `evaluation/COMPARATOR.md` — Blind Comparator agent for unbiased output comparison
- `evaluation/GRADER.md` — Grader agent for evaluating expectations against transcripts

#### Development Agents
- `development/CODER.md` — Coder agent for writing production-ready code
- `development/REVIEWER.md` — Code Reviewer agent for structured code reviews
- `development/DEBUGGER.md` — Debugger agent for systematic bug diagnosis
- `development/TESTER.md` — Test Writer agent for comprehensive test suites

#### Content Agents
- `content/WRITER.md` — Content Writer agent for generating written content
- `content/EDITOR.md` — Content Editor agent for reviewing and improving content
- `content/SUMMARIZER.md` — Summarizer agent for creating concise summaries
- `content/TRANSLATOR.md` — Translator agent for translating content between languages

#### Research Agents
- `research/RESEARCHER.md` — Researcher agent for structured research
- `research/FACT-CHECKER.md` — Fact-Checker agent for verifying claims
- `research/DATA-ANALYST.md` — Data Analyst agent for dataset analysis

#### Operations Agents
- `operations/DEPLOYER.md` — Deployer agent for deployment management
- `operations/MONITOR.md` — Monitor agent for system health tracking
- `operations/SCHEDULER.md` — Scheduler agent for task scheduling

#### Communication Agents
- `communication/EMAIL-DRAFTER.md` — Email Drafter agent for composing emails
- `communication/MEETING-SUMMARIZER.md` — Meeting Summarizer agent for meeting records

#### Documentation
- `README.md` — Project overview with category tables and usage guide
- `CONTRIBUTING.md` — Guidelines for adding new agents
- `CHANGELOG.md` — This file, tracking all changes

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
│   └── GRADER.md
├── development/
│   ├── CODER.md
│   ├── REVIEWER.md
│   ├── DEBUGGER.md
│   └── TESTER.md
├── content/
│   ├── WRITER.md
│   ├── EDITOR.md
│   ├── SUMMARIZER.md
│   └── TRANSLATOR.md
├── research/
│   ├── RESEARCHER.md
│   ├── FACT-CHECKER.md
│   └── DATA-ANALYST.md
├── operations/
│   ├── DEPLOYER.md
│   ├── MONITOR.md
│   └── SCHEDULER.md
├── communication/
│   ├── EMAIL-DRAFTER.md
│   └── MEETING-SUMMARIZER.md
└── github/
    ├── README-WRITER.md
    ├── WIKI-WRITER.md
    ├── DOCS-WRITER.md
    ├── RELEASE-WRITER.md
    ├── PR-DESCRIPTION.md
    └── ISSUE-TEMPLATE.md
```
