# Changelog

All notable changes to this project will be documented in this file.

Newest entries are added at the top.

## [2026-05-06] — Initial Repository Restructuring

### Added

#### Evaluation Agents
- `evaluation/analyzer.md` — Post-hoc Analyzer agent for analyzing blind comparison results and generating improvement suggestions
- `evaluation/comparator.md` — Blind Comparator agent for unbiased output comparison using structured rubrics
- `evaluation/grader.md` — Grader agent for evaluating expectations against execution transcripts

#### Development Agents
- `development/coder.md` — Coder agent for writing production-ready code from specifications
- `development/reviewer.md` — Code Reviewer agent for structured, actionable code reviews
- `development/debugger.md` — Debugger agent for systematic bug diagnosis and fixing
- `development/tester.md` — Test Writer agent for generating comprehensive test suites

#### Content Agents
- `content/writer.md` — Content Writer agent for generating high-quality written content
- `content/editor.md` — Content Editor agent for reviewing and improving existing content
- `content/summarizer.md` — Summarizer agent for creating concise, accurate summaries
- `content/translator.md` — Translator agent for translating content between languages

#### Research Agents
- `research/researcher.md` — Researcher agent for conducting thorough, structured research
- `research/fact-checker.md` — Fact-Checker agent for verifying claims and statements
- `research/data-analyst.md` — Data Analyst agent for analyzing datasets and extracting insights

#### Operations Agents
- `operations/deployer.md` — Deployer agent for managing deployments with safety checks and rollback
- `operations/monitor.md` — Monitor agent for tracking system health and detecting anomalies
- `operations/scheduler.md` — Scheduler agent for task scheduling and resource allocation

#### Communication Agents
- `communication/email-drafter.md` — Email Drafter agent for composing professional emails
- `communication/meeting-summarizer.md` — Meeting Summarizer agent for creating actionable meeting records

#### Documentation
- `README.md` — Complete project overview with category tables and usage guide
- `CONTRIBUTING.md` — Guidelines for adding new agents and improving existing ones
- `CHANGELOG.md` — This file, tracking all notable changes

### Changed
- Replaced minimal `README.md` (single line "# AgentSpace") with comprehensive documentation
- Organized project into 6 category folders: evaluation, development, content, research, operations, communication

### Structure
```
AgentSpace/
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── evaluation/
│   ├── analyzer.md
│   ├── comparator.md
│   └── grader.md
├── development/
│   ├── coder.md
│   ├── reviewer.md
│   ├── debugger.md
│   └── tester.md
├── content/
│   ├── writer.md
│   ├── editor.md
│   ├── summarizer.md
│   └── translator.md
├── research/
│   ├── researcher.md
│   ├── fact-checker.md
│   └── data-analyst.md
├── operations/
│   ├── deployer.md
│   ├── monitor.md
│   └── scheduler.md
└── communication/
    ├── email-drafter.md
    └── meeting-summarizer.md
```
