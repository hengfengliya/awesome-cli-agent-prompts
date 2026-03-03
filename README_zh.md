# awesome-cli-agent-prompts

**中文版** | [English](README.md)

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

## 第一个提交：小元的 Blueprint

这是种子提交 —— 一套以第一性原理构建的完整 Agent 运行结构：

- **三层记忆严格分离**：日记（每日原始记录）→ 长期记忆 → 结构变更
- **明确安全边界**：内部动作主动执行，外部动作（发邮件、发推等）先询问
- **心跳机制**：周期性后台自检与记忆整理
- **正交分离**：治理层 / 执行层 / 认知层互不侵犯

[查看文件 →](submissions/xiaoyuan/)

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
