# Decision-Making Assistant

> Agent-native Personal Cognitive System for long-term growth, problem clarification, and better thinking.

这个项目不是聊天机器人，不是心理咨询师，也不是人生导师。

它是一个只服务于用户个人、拥有长期记忆和独立思考能力的 Personal Cognitive Advisor。

更准确地说，它首先是：

> 陪用户长期成长的第二大脑。

## Mission

帮助用户持续提高认知质量，形成越来越好的思考与决策能力。

遇到难办的问题、难以分析的事情、难以安放的自己时，系统不替用户做决定，而是陪伴用户一步步走到那个能够自己做决定的位置。

## North Star

项目唯一真正的成功标准是：

> 每一次对话结束后，用户都比开始时更清楚问题、更理解自己、更接近事实。

如果长期做到这一点，项目就是成功的。

## Current Shape

V0.1 不是传统 App，不先做 Web、桌面端或完整 CLI。

V0.1 是：

> Agent-native local workspace.

也就是说，第一版先让 Agent 能进入这个仓库，读取项目宪法、Prompt 和本地 Memory 骨架，然后按既定方法和用户对话。

## Core Idea

系统的核心能力不是 Problem Solver，而是 Problem Clarifier。

它不急着给答案，而是帮助用户：

- 澄清问题
- 区分事实、感受、假设、担忧和价值冲突
- 提炼本质
- 形成更清楚的判断条件
- 更新长期认知画像

最终答案仍然属于用户。

## Start Here

For agents:

1. Read `AGENTS.md` first.
2. Then read `docs/CONSTITUTION.md`.
3. Then read `docs/GENESIS.md`.
4. Then follow `docs/AGENT_NATIVE_V0.1.md` and `docs/V0.1_OPERATION_FLOW.md`.

For humans:

1. Read `docs/GENESIS.md` to understand why this exists.
2. Read `docs/CONSTITUTION.md` to understand what the system must never violate.
3. Read `docs/V0.1_SPEC.md` to understand the first version.
4. Read `docs/OPEN_QUESTIONS_AND_BACKLOG.md` to see what remains undecided or unbuilt.

## Current Documents

- `AGENTS.md`：Agent 进入仓库后的工作规则。
- `docs/GENESIS.md`：项目零号文档，记录项目为什么诞生、灵魂是什么。
- `docs/CONSTITUTION.md`：系统宪法，规定 AI 永远不能违背的原则。
- `docs/AGENT_NATIVE_V0.1.md`：说明第一版为什么采用 Agent-native 形态。
- `docs/V0.1_SPEC.md`：第一版规格，明确 V0.1 做什么、不做什么。
- `docs/V0.1_OPERATION_FLOW.md`：V0.1 具体运行流程。
- `docs/OPEN_QUESTIONS_AND_BACKLOG.md`：待确定问题、待实现清单和后续优先级。
- `prompts/`：核心 Prompt 初稿。
- `memory/`：本地 Memory 骨架和维护政策。

## V0.1 Direction

V0.1 的第一核心入口是：

> 我现在很乱，帮我梳理。

核心链路：

```text
混乱输入
↓
澄清问题
↓
区分事实、感受、假设、担忧和价值冲突
↓
提炼本质
↓
形成初步观点
↓
生成 Session Summary
↓
提出 Memory Update 建议
```

## Environment

Real API keys must not be committed.

Use:

- `.env.example` as the committed template
- `.env` for local secrets if needed later

V0.1 defaults are conservative:

- local-first
- no sensitive upload by default
- no automatic confirmed memory writes

## Design Principles

- 真诚高于迎合
- 事实高于立场
- 长期成长高于短期舒服
- 推理过程高于直接答案
- 可以挑战用户，但不能羞辱用户
- 可以有观点，但必须给出证据和不确定性
- 重要记忆必须经过用户确认
- 本地优先，敏感信息默认不上传

## Current Status

当前处于 Agent-native V0.1 奠基阶段。

已完成：

- 项目原点整理
- 系统定位确认
- Constitution 初版
- V0.1 方向确认
- Agent-native 路线确认
- 核心 Prompt 初稿
- 本地 Memory 骨架
- 待确定与待实现清单

下一步：

1. 用真实对话测试 Agent-native 流程
2. 根据测试修正 Prompt 和 Memory Policy
3. 再决定是否实现 local CLI / local Web 原型
