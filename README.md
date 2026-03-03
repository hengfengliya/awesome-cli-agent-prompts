# awesome-cli-agent-prompts

**[中文版](README_zh.md)** | English

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

## Design Principles

- Agent is a system, not a prompt
- Structure over language
- Behavior boundaries must be explicit
- All changes must be traceable
- Long-term maintenance is encouraged

---

## License

MIT — see [LICENSE](LICENSE)
