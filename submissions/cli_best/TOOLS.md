# Concepts
<!-- 核心概念、术语解释 -->

# Tools
<!-- 工具用法、命令、API -->

# Patterns
<!-- 可复用的解决方案模式 -->

# Pitfalls
<!-- 踩过的坑，避免重蹈覆辙 -->

---

# Memory Templates

## `{project}/memory.md`（项目记忆）

按日期倒序追加，只记录本项目相关内容。

```markdown
# {项目名} Memory

## [YYYY-MM-DD]
- **Events**：发生了什么（事实，不评价）
- **Changes**：变更了什么（文件、配置、决策）
- **Insights**：可沉淀的点（无则省略）
- **Next**：下一步（无则省略）
```

---

## `memory/YYYY-MM-DD.md`（每日全局日志）

按项目 / 类型分组，Events 只记事实，省略空字段。

```markdown
# YYYY-MM-DD

## [Project: {项目名}]
- **Events**：
- **Changes**：
- **Insights**：
- **Next**：

## [Global]
- **Events**：
- **Changes**：
- **Insights**：
- **Next**：

## [Learning]
- **Events**：
- **Insights**：

## [Decision]
- **Context**：决策背景
- **Choice**：做了什么选择
- **Reason**：为什么
```

---

## `life_mark/MEMORY.md`（长期记忆）

可整理重写，但不删除「已废弃」条目，每条注明首次发现日期。

```markdown
# Memory

## 关于用户
<!-- 工作方式、偏好、习惯 -->

## 关于协作方式
<!-- 哪些模式有效，哪些无效 -->

## 持续有效的规律
- YYYY-MM-DD：{规律描述}

## 已废弃的认知
<!-- 曾经有效但已失效，保留以防回退 -->
```
