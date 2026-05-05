# Contributing to AgentSpace

Thanks for your interest in contributing! Here's how to add new agents or improve existing ones.

## Adding a New Agent

### 1. Choose the Right Category

Place your agent in the appropriate category folder:

- `evaluation/` — For agents that judge, compare, or assess outputs
- `development/` — For agents that write, review, or fix code
- `content/` — For agents that create or edit written content
- `research/` — For agents that investigate, verify, or analyze
- `operations/` — For agents that deploy, monitor, or schedule
- `communication/` — For agents that draft messages or summarize discussions

If no category fits, create a new folder with a brief description in the README.

### 2. Follow the Standard Format

Every agent must include these sections:

```markdown
# Agent Name

One-line description.

## Role
What the agent does and its core responsibility.

## Inputs
List of parameters with names, types, and descriptions.

## Process
Step-by-step methodology (numbered steps).

## Output Format
Template showing expected output structure (JSON or Markdown).

## Guidelines
Best practices, do's and don'ts, edge cases.
```

### 3. Quality Checklist

Before submitting:

- [ ] **Role** is clear and specific (not "does everything")
- [ ] **Inputs** are well-defined with types and descriptions
- [ ] **Process** has actionable steps (not vague instructions)
- [ ] **Output Format** includes a concrete template
- [ ] **Guidelines** cover edge cases and common mistakes
- [ ] The agent definition is self-contained (doesn't assume hidden knowledge)
- [ ] Examples in the output format are realistic

### 4. Naming Conventions

- File names: `lowercase-with-hyphens.md`
- Agent titles: Title Case ("Code Reviewer Agent")
- Keep file names descriptive but concise

## Improving Existing Agents

1. Open an issue describing the improvement
2. Submit a PR with the changes
3. Explain *why* the change improves the agent

## Agent Design Principles

1. **Specificity over generality**: An agent that does one thing well is better than one that does everything poorly
2. **Explicit over implicit**: Don't assume the AI knows context — spell it out
3. **Structured output**: Always define what the output should look like
4. **Error awareness**: Include guidance for handling edge cases and failures
5. **Actionable guidelines**: "Be specific" is vague; "Include line numbers in feedback" is actionable

## Pull Request Process

1. Fork the repository
2. Create a branch: `git checkout -b add-agent-name`
3. Add your agent file(s)
4. Update the README.md table with your new agent
5. Add an entry to CHANGELOG.md
6. Submit the PR with a clear description

## Questions?

Open an issue if you have questions about contributing.
