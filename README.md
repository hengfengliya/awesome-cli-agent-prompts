# awesome-cli-agent-prompts

**[中文版](README_zh.md)** | English

---

OpenClaw has been making waves lately. Like most developers, my first reaction was "I get it" — until I actually sat down and built with it.

What caught me was the *system design thinking* behind it: treating an agent's runtime structure as an engineering problem, not a collection of prompt tricks. That, combined with my own experience building with CLI agents, pushed me to rethink how I configure my own agent from scratch.

This repo is the result. I'm sharing my `AGENTS.md` design to start — not as a best practice, but as a genuine working config that's been running for months. **I'm opening this up as a co-creation project.** Submit yours. Vote on others. Let's build the reference library for CLI agent architecture that doesn't exist yet.

---

> A community collection of complete AI Agent Runtime Blueprints.
> **Not just prompts — full operational systems.**

Most "agent prompts" are one-liners. This repo is different.

A **Blueprint** is everything your agent needs to run consistently across sessions:
identity, memory, behavioral boundaries, tool config, workspace governance, and heartbeat tasks.
Think of it as a *home* for your agent — a structure it returns to every time it wakes up.

---

## Browse Submissions

→ **[Open Gallery](https://hengfengliya.github.io/awesome-cli-agent-prompts/)**

Sort by votes. Filter by file type. See what others have built.

---

## Submit Your Blueprint

Got your own agent setup? **Share it.**

The community votes on what's useful. Your design might be exactly what someone else needs.

**Minimum requirements:**
- `README.md` — your philosophy, design decisions, author credit, license
- At least 2 recognized file types (see below)

**Recognized file types:**

| File | What it defines |
|------|----------------|
| `IDENTITY.md` | Name, persona, style |
| `SOUL.md` | Core principles, behavioral limits |
| `USER.md` | User preferences, communication conventions |
| `MEMORY.md` | Long-term memory structure |
| `TOOLS.md` | Tool & environment configuration |
| `AGENTS.md` | Workspace governance rules |
| `HEARTBEAT.md` | Periodic check tasks |
| `BOOTSTRAP.md` | First-run initialization guide |
| `PRODUCT.md` | Product context |
| `PLAN.md` | Planning structure |
| `TASK.md` | Task tracking approach |
| `CHANGE.md` | Change log structure |

**How to submit:**
1. Fork this repo
2. Create `submissions/YOUR_HANDLE/`
3. Add your files (`README.md` required)
4. Update `registry.json` with your entry
5. Open a Pull Request

Full details → [CONTRIBUTING.md](CONTRIBUTING.md)

---

## First Submission: xiaoyuan's Blueprint

The seed submission — a complete runtime system built on first-principles thinking:

- Strict three-layer memory: daily notes → long-term memory → structural changes
- Explicit safety boundaries: internal actions automatic, external actions ask first
- Heartbeat mechanism: periodic background self-maintenance
- Orthogonal separation: governance / execution / cognition never bleed into each other

[View files →](submissions/xiaoyuan/)

---

## What This Is Not

- Not a collection of leaked commercial system prompts
- Not a generic "awesome list" of AI resources
- Not a single-prompt showcase

---

## Works With

Any CLI agent or tool that supports system prompts or instruction files:

| Tool | How to use |
|------|-----------|
| **Claude Code** | Place files in workspace; `CLAUDE.md` auto-loads, others via `@file` or session start |
| **Gemini CLI** | Pass as system prompt file or include in context |
| **OpenClaw** | Configure as system prompt in session settings |
| **Codex CLI** | Use `.codex/instructions.md` or system prompt config |
| **Any LLM CLI** | Drop files in workspace, reference at session start |

The structure is model-agnostic. The concepts (identity, memory, boundaries, heartbeat) apply to any stateful agent.

---

## Design Principles

- Agent is a system, not a prompt
- Structure over language
- Behavior boundaries must be explicit
- All changes must be traceable
- Long-term maintenance is encouraged

---

## License

MIT — see [LICENSE](LICENSE)
