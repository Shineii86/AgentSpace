# 🚀 AgentSpace

A curated collection of structured agent definitions for building AI-powered workflows. Each agent definition follows a consistent format: **Role → Inputs → Process → Output Format → Guidelines**.

## Why AgentSpace?

Agent definitions are the "source code" of AI agents. They tell an AI *what to do*, *how to do it*, and *what the output should look like*. AgentSpace provides a library of battle-tested agent definitions you can use, customize, and compose.

## 📂 Categories

### 📊 [Evaluation](evaluation/)
Agents for evaluating, comparing, and grading outputs.

| Agent | Purpose |
|-------|---------|
| [ANALYZER](evaluation/ANALYZER.md) | Post-hoc analysis of comparison results to extract actionable insights |
| [COMPARATOR](evaluation/COMPARATOR.md) | Blind comparison of two outputs without bias |
| [GRADER](evaluation/GRADER.md) | Evaluate expectations against execution transcripts |

### 💻 [Development](development/)
Agents for writing, reviewing, debugging, and testing code.

| Agent | Purpose |
|-------|---------|
| [CODER](development/CODER.md) | Write clean, production-ready code from specifications |
| [REVIEWER](development/REVIEWER.md) | Structured code reviews with actionable feedback |
| [DEBUGGER](development/DEBUGGER.md) | Systematic bug diagnosis and fixing |
| [TESTER](development/TESTER.md) | Generate comprehensive test suites |

### ✍️ [Content](content/)
Agents for writing, editing, summarizing, and translating content.

| Agent | Purpose |
|-------|---------|
| [WRITER](content/WRITER.md) | Generate high-quality content for various purposes |
| [EDITOR](content/EDITOR.md) | Review and improve existing content |
| [SUMMARIZER](content/SUMMARIZER.md) | Create concise, accurate summaries |
| [TRANSLATOR](content/TRANSLATOR.md) | Translate content between languages |

### 🔬 [Research](research/)
Agents for investigating topics, verifying claims, and analyzing data.

| Agent | Purpose |
|-------|---------|
| [RESEARCHER](research/RESEARCHER.md) | Conduct thorough research and produce structured findings |
| [FACT-CHECKER](research/FACT-CHECKER.md) | Verify claims, statistics, and statements |
| [DATA-ANALYST](research/DATA-ANALYST.md) | Analyze datasets and extract actionable insights |

### ⚙️ [Operations](operations/)
Agents for deploying, monitoring, and scheduling.

| Agent | Purpose |
|-------|---------|
| [DEPLOYER](operations/DEPLOYER.md) | Manage deployments with safety checks and rollback |
| [MONITOR](operations/MONITOR.md) | Track system health, detect anomalies, generate alerts |
| [SCHEDULER](operations/SCHEDULER.md) | Plan and coordinate task scheduling |

### 📨 [Communication](communication/)
Agents for drafting emails and summarizing meetings.

| Agent | Purpose |
|-------|---------|
| [EMAIL-DRAFTER](communication/EMAIL-DRAFTER.md) | Compose professional, effective emails |
| [MEETING-SUMMARIZER](communication/MEETING-SUMMARIZER.md) | Transform meeting notes into actionable records |

### 🐙 [GitHub](github/)
Agents for GitHub documentation, workflows, community, and project management.

| Agent | Purpose |
|-------|---------|
| [README-WRITER](github/README-WRITER.md) | Generate comprehensive README files for repositories |
| [WIKI-WRITER](github/WIKI-WRITER.md) | Create structured wiki documentation |
| [DOCS-WRITER](github/DOCS-WRITER.md) | Generate technical documentation for codebases |
| [RELEASE-WRITER](github/RELEASE-WRITER.md) | Create polished release notes from changes |
| [PR-DESCRIPTION](github/PR-DESCRIPTION.md) | Generate clear, informative PR descriptions |
| [ISSUE-TEMPLATE](github/ISSUE-TEMPLATE.md) | Create structured issue templates |
| [COMMIT-MESSAGE](github/COMMIT-MESSAGE.md) | Generate conventional commit messages from diffs |
| [CHANGELOG-WRITER](github/CHANGELOG-WRITER.md) | Generate structured changelogs from commits and PRs |
| [CI-CD-WRITER](github/CI-CD-WRITER.md) | Generate GitHub Actions workflows for CI/CD |
| [SECURITY-POLICY](github/SECURITY-POLICY.md) | Generate SECURITY.md and security documentation |
| [CODEOWNERS-GENERATOR](github/CODEOWNERS-GENERATOR.md) | Generate CODEOWNERS files for review assignment |
| [DISCUSSION-WRITER](github/DISCUSSION-WRITER.md) | Generate GitHub Discussions posts for community |
| [MIGRATION-GUIDE](github/MIGRATION-GUIDE.md) | Generate version migration guides with upgrade instructions |
| [GITHUB-ACTIONS-AUDITOR](github/GITHUB-ACTIONS-AUDITOR.md) | Audit workflows for security, efficiency, best practices |
| [REPO-SETUP](github/REPO-SETUP.md) | Bootstrap new repos with essential config files |
| [LABEL-MANAGER](github/LABEL-MANAGER.md) | Design label taxonomies for issues and PRs |
| [FUNDING-SETUP](github/FUNDING-SETUP.md) | Generate FUNDING.yml and monetization config |
| [ISSUE-TRIAGER](github/ISSUE-TRIAGER.md) | Automatically categorize, prioritize, and route issues |
| [REPO-HEALTH](github/REPO-HEALTH.md) | Score and assess repository health across dimensions |
| [CONTRIBUTING-GUIDE](github/CONTRIBUTING-GUIDE.md) | Generate comprehensive contributing guidelines |
| [DEPENDENCY-AUDITOR](github/DEPENDENCY-AUDITOR.md) | Audit dependencies for vulnerabilities and licenses |
| [BADGE-GENERATOR](github/BADGE-GENERATOR.md) | Generate README badges for status, coverage, version |

## 📋 Agent Definition Format

Every agent in AgentSpace follows this structure:

```markdown
# Agent Name

One-line description of what the agent does.

## Role
What the agent is responsible for and its core behavior.

## Inputs
Parameters the agent receives (names, types, descriptions).

## Process
Step-by-step methodology the agent follows.

## Output Format
JSON or Markdown template showing the expected output structure.

## Guidelines
Do's and don'ts, best practices, and edge cases.
```

## 🛠️ Usage

### With OpenClaw
Agent definitions can be loaded as skill prompts. Point your agent at the definition file and provide the required inputs.

### With Any LLM
Copy the agent definition into your system prompt or use it as a template for your own agents.

### Customization
1. Fork this repository
2. Modify existing agents to match your needs
3. Add new agents following the standard format
4. Submit a PR to share with the community

## 📝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding new agents.

## 📄 License

See [LICENSE](LICENSE) for details.

---

**Built with ❤️ for the AI agent community**
