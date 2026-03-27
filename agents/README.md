# Agents

Agent templates are specialized personas your AI can adopt for specific tasks.

They are optional. Use them when a task benefits from a tighter role and clearer rules.

---

## Included In This Kit

| Agent | Purpose |
|-------|---------|
| `research-agent` | Find reliable, current sources and summarize them clearly |
| `code-explainer` | Explain code in plain language for non-technical users |

---

## How To Use

### Claude Code

If your tool supports agent-like workflows, load the relevant file and follow it.

### Cursor / VS Code / other chat tools

Say:

> Read `agents/research-agent/research-agent.md` and use that role.

Or:

> Read `agents/code-explainer/code-explainer.md` and explain this code for a non-technical founder.

---

## Folder Structure

```text
agents/
├── README.md
├── code-explainer/
│   └── code-explainer.md
└── research-agent/
    └── research-agent.md
```

---

## When To Create A New Agent

Create a new agent when:

- the work type repeats often
- the task benefits from a clear persona
- the workflow needs tighter rules than your default AI behavior

Examples:

- legal reviewer
- customer-interview synthesizer
- bug triage specialist

---

## Rule Of Thumb

Use a skill for a workflow.

Use an agent for a role.
