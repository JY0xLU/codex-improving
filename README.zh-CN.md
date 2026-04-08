# Codex Native Dream Loop

中文 | [English](README.md)

`Codex Native Dream Loop` 是一个面向 Codex 的 Dream Loop 系统，目标是自我改进和记忆优化。

它保留最初的闭环：

- 白天只采集信号
- 夜间统一整理记忆

它也保留最初的基础组件：

- `AGENTS.md`
- skills
- automations
- worktrees
- sandbox 和权限
- subagents

v2 的重点很简单：

- 提升 agent 本身
- 让记忆保持轻量且可检索
- 保留审计能力和回滚路径
- 需要时做最小范围检索，不要动辄全文重读

## 架构

### 1. Policy

只接受人工批准的规则。

- `AGENTS.md` 仍然是面向人的 Policy 入口
- 不自动修改 Policy
- 如果某条规则应当进入 Policy，就先提案再审核

### 2. 记忆范围

v2 只使用三个范围：global、repo、thread。

- `global` 保存跨项目模式
- `repo` 保存项目级记忆
- `thread` 保存短生命周期的会话上下文
- `ACTIVE.md` 是 operational projection
- `LEARNINGS.md` 是 long-term projection
- 检索要尽量最小化：只读取当前任务需要的片段，不要默认读取整份记忆

### 3. 改进循环

白天用 `capture-memory`，夜间用 `dream-consolidate`。

- 把原始信号写入 `inbox/`
- 每晚做一次 consolidation
- 只在证据重复且可执行时去重、过期、重写和升级
- agent reviewer 可以自动复核并把明确案例推进到 LongTerm 记忆，但不能推进到 Policy
- 夜间整理要成为常规动作，而不是临时清理

### 4. Audit

每次记忆变更都应该可解释、可恢复。

- 保留 source id
- 记录读了什么、改了什么、升级了什么、拒绝了什么、归档了什么、回滚了什么
- 报告要支持回滚和后续复核
- 保持低风险清理足够快，但不要牺牲可追踪性

## 这个仓库包含什么

这个仓库提供一个最小化的 Dream Loop：

- `skills/capture-memory/`
  - 白天采集 skill
  - 把结构化观察写入 `inbox/`
- `skills/dream-consolidate/`
  - 夜间整理 skill
  - 负责去重、过期处理、重写、升级和生成报告
- `templates/`
  - `AGENTS.md` 起始片段
  - 记忆文件起始模板
- `examples/`
  - 一个最小化的 global-memory 示例
- `automations/`
  - 推荐的夜间自动化 prompt 和调度

## 核心规则

- 白天采集只写入 `.codex/memory/inbox/`
- 夜间整理可以重写 `.codex/memory/` 下的记忆文件
- `AGENTS.md` 绝不自动修改
- 所有升级、合并、归档和拒绝都必须可审计
- `ACTIVE.md` 可以放临时指导，但每条临时内容都要带失效条件
- `capture-memory` 要保持轻量；重 subagent 的工作留给 Dream Loop review 和 audit

## Subagent 倾向

这个仓库在 Dream Loop 维护上更偏向 subagent-assisted review：

- `capture-memory` 仍然是轻量的单 agent 流程
- `dream-consolidate` 在 promotion、rejection、archive 和 conflict review 时应优先使用至少一个 subagent
- 低风险清理仍然可以走单 agent fast path
- 如果主 agent 和 reviewer 有分歧，最终报告要记录分歧和裁决结果

## 仓库结构

```text
repo/
├── README.md
├── README.zh-CN.md
├── references/
├── templates/
├── examples/
├── automations/
└── skills/
    ├── capture-memory/
    └── dream-consolidate/
```

## 快速开始

1. 将 `skills/capture-memory/` 和 `skills/dream-consolidate/` 复制到 `$CODEX_HOME/skills/` 或 `~/.codex/skills/`，让 Codex 能发现它们。
2. 将 `templates/global/` 下的模板复制到全局 Codex home 作为起始结构。
3. 把 `AGENTS.md` 片段接入你的全局入口或项目入口。
4. 在日常工作中使用 `capture-memory`。
5. 用 nightly automation 运行 `dream-consolidate`。
6. 对重要的 nightly promotion 或 rejection 决策，优先做 subagent 交叉复核。
7. 在信任升级结果之前，先查看生成的 audit 报告。
