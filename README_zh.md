# awesome-cli-agent-prompts

**中文版** | [English](README.md)

---

最近 OpenClaw 很火。程序员大多眼高手低，我也一样——看到新工具第一反应是"这有什么"，然后真正用起来才发现自己根本没搞明白。

OpenClaw 让我觉得真正有意思的，不是它的功能列表，是它**对 system 层的设计思路**：把 Agent 的运行结构当作工程问题来处理，而不是 prompt 技巧的堆砌。结合我之前使用 CLI Agent 的积累，我把自己的 Agent 配置重新设计了一遍，整理出了一套 `AGENTS.md`。

这不是什么最佳实践，是**我自己真实在跑的设计，拿出来抛砖引玉**。

这个仓库是一个**共创项目**——每个人提交自己的 Agent 运行结构，互相看、互相投票，慢慢形成这个领域里真正有价值的参考库。你的设计不需要完美，只需要真实在跑。

---

> 一个社区共建的 AI Agent 完整运行结构合集。
> **不是 Prompt，是系统。**

大多数"Agent Prompt"是一两行指令。这个仓库不一样。

**Blueprint（蓝图）** 是 Agent 跨会话稳定运行所需的一切：
身份设定、记忆结构、行为边界、工具配置、工作区治理、心跳机制。
把它想象成 Agent 的*家* —— 每次启动，它回到这里，知道自己是谁、要做什么。

---

## 浏览提交

→ **[打开展示页](https://hengfengliya.github.io/awesome-cli-agent-prompts/)**

按点赞排序，按文件类型筛选，看看别人都构建了什么。

---

## 提交你的 Blueprint

你有自己的 Agent 配置体系吗？**分享出来。**

社区会投票选出有价值的设计。你的方案，可能正好是别人需要的。

**最低要求：**
- `README.md` —— 你的理念、设计思路、作者署名、License
- 至少 2 个已知文件类型（见下表）

**已知文件类型：**

| 文件 | 定义内容 |
|------|---------|
| `IDENTITY.md` | 名字、人格、风格 |
| `SOUL.md` | 核心原则、行为边界 |
| `USER.md` | 用户偏好、沟通约定 |
| `MEMORY.md` | 长期记忆结构 |
| `TOOLS.md` | 工具与环境配置 |
| `AGENTS.md` | 工作区治理规则 |
| `HEARTBEAT.md` | 周期性心跳任务 |
| `BOOTSTRAP.md` | 首次启动引导 |
| `PRODUCT.md` | 产品上下文 |
| `PLAN.md` | 规划结构 |
| `TASK.md` | 任务追踪方式 |
| `CHANGE.md` | 变更记录结构 |

**提交步骤：**
1. Fork 本仓库
2. 创建 `submissions/你的名字/`
3. 添加你的文件（`README.md` 必须有）
4. 在 `registry.json` 中添加你的 entry
5. 提 Pull Request

完整规范 → [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 推荐提交

### xiaoyuan / yuan

这是当前的种子提交版本，已经从单纯的提示词集合升级成更完整的工作区运行结构：

- **`life_mark` 作为 Agent 的家**：长期记忆、系统规则、通用知识统一锚定
- **PARA + CODE 目录语义**：不仅分目录，还定义内容如何流转
- **双层治理**：根目录负责系统层，项目目录负责执行层
- **可追溯记录体系**：`memory`、`MEMORY.md`、`change.md`、`CHANGE.md` 分层留痕

[查看文件 →](submissions/xiaoyuan/)

### cli_best

这是一个更克制的治理型 Blueprint，核心是那份 GPT 评分 `99.5` 的 `AGENTS.md`：

- **默认少加载**：只加载必要文件，其他上下文按需展开
- **写入可追溯**：所有写入先读后写，日志类记忆坚持仅追加
- **项目就近协作**：`tools.md` / `memory.md` 绑定当前工作目录，而不是强制绑定根目录

[查看文件 →](submissions/cli_best/)

---

## 适用平台

任何支持 system prompt 或 instruction 文件的 CLI Agent：

| 工具 | 使用方式 |
|------|---------|
| **Claude Code** | 放在工作区，`CLAUDE.md` 自动加载，其他文件通过 `@file` 引用 |
| **Gemini CLI** | 作为 system prompt 文件传入，或在上下文中引用 |
| **OpenClaw** | 在会话设置中配置为 system prompt |
| **Codex CLI** | 使用 `.codex/instructions.md` 或 system prompt 配置 |
| **任意 LLM CLI** | 放入工作区，会话启动时引用 |

这套结构与模型无关。身份、记忆、边界、心跳这些概念适用于任何有状态的 Agent。

---

## 不做什么

- 不收集泄露的商业 System Prompt
- 不做泛资源列表
- 不做单条 Prompt 示例合集

---

## 设计原则

- Agent 是系统，不是 Prompt
- 结构优先于语言
- 行为边界必须清晰
- 所有变更可追溯
- 鼓励长期维护

---

## License

MIT — 见 [LICENSE](LICENSE)
