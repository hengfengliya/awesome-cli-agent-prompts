# cli_best · Minimal Traceable Agent Blueprint

> A compact agent runtime centered on a high-scoring `AGENTS.md` prompt.
> The focus is strict loading boundaries, minimal writes, and traceable memory updates.

## Core Idea

This submission keeps the runtime small on purpose.

Instead of a large identity stack, it uses one governance file plus one toolbox file to define:

- what the agent should load by default
- when deeper context should be pulled in
- how memory and tool knowledge should be separated
- which files can be rewritten and which must stay append-only

## What Makes It Different

1. **Minimal context loading**
Only `AGENTS.md` and current-project files are loaded by default. Global files are pulled in only when the task actually needs them.

2. **Traceability first**
Every write follows a read-before-write rule, and log-style memory files stay append-only.

3. **Project-relative memory**
Project `tools.md` and `memory.md` travel with the current working directory instead of being forced under `life_mark/`.

4. **Practical operating boundary**
The blueprint is designed for execution work: do less, read less, and only expand context with a reason.

## Included Files

| File | Purpose |
|------|---------|
| `AGENTS.md` | Runtime rules, loading order, write policy, and memory triggers |
| `TOOLS.md` | Shared concepts plus memory templates for global and project logs |

## Author

- Handle: cli_best
- GitHub: [hengfengliya](https://github.com/hengfengliya)

## License

MIT
