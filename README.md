# 🚀 AgentSpace

A curated collection of structured agent definitions for building AI-powered workflows. Each agent definition follows a consistent format: **Role → Inputs → Process → Output Format → Guidelines**.

## Why AgentSpace?

Agent definitions are the "source code" of AI agents. They tell an AI *what to do*, *how to do it*, and *what the output should look like*. AgentSpace provides a library of battle-tested agent definitions you can use, customize, and compose.

## 📂 Categories

### 📊 [Evaluation](evaluation/)
Agents for evaluating, comparing, and grading outputs.

| Agent | Purpose |
|-------|---------|
| [Analyzer](evaluation/analyzer.md) | Post-hoc analysis of comparison results to extract actionable insights |
| [Comparator](evaluation/comparator.md) | Blind comparison of two outputs without bias |
| [Grader](evaluation/grader.md) | Evaluate expectations against execution transcripts |

### 💻 [Development](development/)
Agents for writing, reviewing, debugging, and testing code.

| Agent | Purpose |
|-------|---------|
| [Coder](development/coder.md) | Write clean, production-ready code from specifications |
| [Reviewer](development/reviewer.md) | Structured code reviews with actionable feedback |
| [Debugger](development/debugger.md) | Systematic bug diagnosis and fixing |
| [Tester](development/tester.md) | Generate comprehensive test suites |

### ✍️ [Content](content/)
Agents for writing, editing, summarizing, and translating content.

| Agent | Purpose |
|-------|---------|
| [Writer](content/writer.md) | Generate high-quality content for various purposes |
| [Editor](content/editor.md) | Review and improve existing content |
| [Summarizer](content/summarizer.md) | Create concise, accurate summaries |
| [Translator](content/translator.md) | Translate content between languages |

### 🔬 [Research](research/)
Agents for investigating topics, verifying claims, and analyzing data.

| Agent | Purpose |
|-------|---------|
| [Researcher](research/researcher.md) | Conduct thorough research and produce structured findings |
| [Fact-Checker](research/fact-checker.md) | Verify claims, statistics, and statements |
| [Data Analyst](research/data-analyst.md) | Analyze datasets and extract actionable insights |

### ⚙️ [Operations](operations/)
Agents for deploying, monitoring, and scheduling.

| Agent | Purpose |
|-------|---------|
| [Deployer](operations/deployer.md) | Manage deployments with safety checks and rollback |
| [Monitor](operations/monitor.md) | Track system health, detect anomalies, generate alerts |
| [Scheduler](operations/scheduler.md) | Plan and coordinate task scheduling |

### 📨 [Communication](communication/)
Agents for drafting emails and summarizing meetings.

| Agent | Purpose |
|-------|---------|
| [Email Drafter](communication/email-drafter.md) | Compose professional, effective emails |
| [Meeting Summarizer](communication/meeting-summarizer.md) | Transform meeting notes into actionable records |

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
