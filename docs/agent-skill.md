# Agent Skill — Arkiv × Puna Tech Builder Challenge

Speed up development by installing Arkiv's official agent skill into your AI coding assistant. It gives your agent instant knowledge of the SDK, best practices, and common integration patterns — useful especially in a short build window.

## What is a skill?

A **skill** is a set of instructions and domain knowledge that you install into your AI coding agent (Claude Code, Cursor, GitHub Copilot, Cline, Windsurf, etc.). Once installed, the agent can reference it automatically whenever you ask about the relevant topic — no copy-pasting docs into the chat.

## The Arkiv skill

Arkiv publishes an official skill called **arkiv-best-practices**. It teaches your agent:

- How the Arkiv SDK works (clients, queries, mutations, events)
- Best practices (project attributes, security, data modelling, error handling)
- Integration patterns (backend, React, wagmi)
- Common pitfalls and how to avoid them

Install it in your project:

```bash
npx skills add https://github.com/arkiv-network/skills --skill arkiv-best-practices
```

**Tip:** The skill is published on [skills.sh/arkiv-network/skills/arkiv-best-practices](https://skills.sh/arkiv-network/skills/arkiv-best-practices).

## What to try

Once installed, open your AI agent and try prompts like:

- *"Build a feature that lets users create and list posts stored on Arkiv"*
- *"Audit my project — am I following Arkiv best practices?"*
- *"Set up a React hook that reads Arkiv entities with TanStack Query"*

---

## Reporting bugs and suggesting features

Arkiv also publishes an **arkiv-feedback** skill. It walks you through an interactive bug report or feature request form and files the result directly to the public [`Arkiv-Network/reported-issues`](https://github.com/Arkiv-Network/reported-issues) repo on GitHub.

Install it alongside `arkiv-best-practices`:

```bash
npx skills add https://github.com/arkiv-network/skills --skill arkiv-feedback
```

Once installed, invoke it in your AI agent:

```
/arkiv-feedback
```

The skill prompts you for the relevant details (what you expected, what happened, reproduction steps, SDK version), then opens or files the issue on your behalf. The Arkiv team monitors the repo throughout the build window.
