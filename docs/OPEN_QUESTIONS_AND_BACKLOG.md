# Open Questions and Backlog

> 这份文档记录尚未确定、待设计、待实现的内容。
> 它不是项目灵魂文档，而是后续执行和迭代的工作清单。

## 1. 已确认但待实现

### 1.1 文档体系

- [x] Genesis 零号文档
- [x] Constitution 系统宪法
- [x] V0.1 Spec
- [x] 待确定与待实现清单
- [ ] README 首页说明
- [ ] docs 索引页
- [ ] 项目术语表

### 1.2 Core Experience

- [ ] “我现在很乱，帮我梳理”入口
- [ ] Problem Clarifier 流程
- [ ] 事实 / 感受 / 假设 / 担忧 / 价值冲突拆分
- [ ] 本质判断生成
- [ ] 必要时追问机制
- [ ] 必要时挑战机制
- [ ] 对话结束 Session Summary
- [ ] Memory Update 建议

### 1.3 Memory

- [ ] 用户长期 Profile 数据结构
- [ ] Memory Item 数据结构
- [ ] Pending Memory 区域
- [ ] Confirmed Memory 区域
- [ ] Rejected / Archived Memory 机制
- [ ] Memory Update 判断规则
- [ ] 用户确认写入机制
- [ ] 定期 Memory Review
- [ ] 记忆修正、删除、降权机制
- [ ] 敏感信息默认不写入规则

### 1.4 Privacy

- [ ] 本地优先存储方案
- [ ] 敏感信息类型定义
- [ ] 敏感信息识别规则
- [ ] 云端模型调用前的脱敏策略
- [ ] 用户授权机制
- [ ] 本地数据导出 / 备份机制
- [ ] 本地数据删除机制

### 1.5 Session Summary

- [ ] Summary 模板最终版
- [ ] 表面问题字段
- [ ] 本质判断字段
- [ ] 已澄清事实字段
- [ ] 未验证假设字段
- [ ] 思维模式观察字段
- [ ] 长期趋势信号字段
- [ ] Memory Update 建议字段
- [ ] 可选下一步行动字段
- [ ] Summary 存储格式

### 1.6 Framework Library

- [ ] Framework Library 总体设计
- [ ] 框架选择规则
- [ ] 框架轻量引用方式
- [ ] 用户追问时的展开方式
- [ ] 东方框架第一批清单
- [ ] 现代框架第一批清单
- [ ] 框架与 Prompt / Skill 的连接方式

### 1.7 Prompt and Skill

- [ ] Advisor System Prompt
- [ ] Problem Clarifier Prompt
- [ ] Session Summary Prompt
- [ ] Memory Update Prompt
- [ ] Challenge Policy Prompt
- [ ] Privacy Guard Prompt
- [ ] Framework Selection Prompt
- [ ] Reflection Prompt

### 1.8 Product and UI

- [ ] 首页信息架构
- [ ] 第一入口交互方式
- [ ] 对话页结构
- [ ] Summary 展示方式
- [ ] Memory Update 确认界面
- [ ] Memory Review 界面
- [ ] 长期画像查看界面
- [ ] 本地数据管理界面

### 1.9 Engineering

- [ ] 技术栈选择
- [ ] 本地存储方案
- [ ] LLM Provider 抽象层
- [ ] 本地模型 / 云端模型切换方案
- [ ] Prompt 管理方式
- [ ] Memory 读写层
- [ ] Session 存储层
- [ ] 测试策略
- [ ] 日志策略
- [ ] 错误处理策略

## 2. 待确定问题

### 2.1 Memory 判断标准

问题：什么内容值得写入长期记忆？

待确定：

- “重要记忆”的判断标准
- “低风险长期信息”的判断标准
- “阶段性状态”多久后降权或删除
- 记忆之间冲突时如何处理
- 旧记忆如何被新证据修正
- 用户反驳记忆后如何记录

当前原则：

- 重要记忆必须用户确认
- 敏感记忆默认不写
- Memory 保存用户模型，不保存聊天流水

### 2.2 Memory Review 周期

问题：多久做一次 Memory Review？

候选：

- 每周
- 每月
- 每 10 次重要对话后
- 用户手动触发

当前倾向：

- V0.1 先手动触发
- V0.5 增加月度 Memory Review

### 2.3 Session Summary 模板

问题：模板应该多固定？

候选：

- 固定结构，便于长期积累
- 半固定结构，保留自然表达
- 根据场景动态生成

当前倾向：

- 采用半固定结构
- 重要字段固定
- 具体表达根据场景变化

### 2.4 本质判断的触发条件

问题：哪些对话需要明确“本质判断”？

候选：

- 每次对话都生成
- 只有重要对话生成
- 用户要求总结时生成

当前倾向：

- 重要对话必须有
- 小型日常问题不强行生成

### 2.5 Challenge 强度调节

问题：如何判断当前应该温和提醒、明确指出漏洞，还是强烈挑战？

待确定信号：

- 用户情绪稳定度
- 问题风险等级
- 用户是否反复逃避同类问题
- 是否涉及重大人生决策
- 是否涉及医学、法律、财务等高风险领域

当前原则：

- 必要时强烈挑战
- 情绪高压时先稳定，再挑战

### 2.6 敏感信息识别

问题：如何判断内容是否敏感？

当前敏感类别：

- 财产、资产、收入、债务、投资
- 账户、密码、身份信息
- 合同、法律纠纷
- 医疗记录
- 家庭隐私
- 非公开人际关系细节
- 尚未公开的项目或商业计划

待确定：

- 是否做自动识别
- 是否做上传前提醒
- 是否允许用户设置更严格的敏感规则

### 2.7 Framework Library 第一批框架

问题：V0.5 第一批框架放哪些？

东方候选：

- 儒家
- 道家
- 法家
- 墨家
- 孙子兵法

现代候选：

- 第一性原理
- 系统思维
- 贝叶斯推理
- 第二序思维
- 行为经济学
- 机会成本
- 决策树
- 反脆弱
- 复利思维

当前倾向：

- 东方和现代五五开
- 框架服务于分析，不服务于展示

### 2.8 技术栈

问题：项目用什么技术栈实现？

待确定：

- 前端框架
- 后端框架
- 本地数据库
- LLM SDK
- 是否需要桌面应用
- 是否先做 CLI / 本地 Web 原型

当前倾向：

- 先不要为了技术栈发散
- 优先实现核心体验闭环

### 2.9 Hermes / AI 维护 AI

问题：什么时候实现 AI 维护 AI？

当前结论：

- V0.1 不做
- 至少两个版本之后再考虑

未来设想：

```text
Reflection
↓
发现问题
↓
生成 Improvement Proposal
↓
Codex 读取
↓
生成 PR
↓
用户 Review
↓
Merge
```

## 3. 待实现优先级建议

### P0 - 先让核心体验成立

- [ ] Advisor System Prompt
- [ ] Problem Clarifier Prompt
- [ ] Session Summary Prompt
- [ ] Memory Update Suggestion Prompt
- [ ] 本地 Profile 文件
- [ ] 本地 Pending Memory 文件
- [ ] 一个最小可用对话入口

### P1 - 让系统开始长期积累

- [ ] Confirmed Memory 管理
- [ ] 用户确认 Memory 写入
- [ ] Session Summary 存储
- [ ] 长期趋势信号记录
- [ ] Memory Review 初版

### P2 - 让系统更像长期顾问

- [ ] Framework Library 初版
- [ ] Framework Selection
- [ ] Goal Tracking
- [ ] Monthly Review
- [ ] 长期画像查看和编辑

### P3 - 让系统能自我迭代

- [ ] Reflection Review
- [ ] Improvement Proposal
- [ ] Prompt 版本管理
- [ ] AI 维护 AI 流程

## 4. 暂不做清单

V0.1 暂不做：

- 多用户账号
- 社交分享
- 公开产品化
- 完整心理咨询体系
- 医学、法律、财务专业建议
- 自动替用户做重大决策
- 完整 Hermes 流程
- 复杂 Agent 网络
- 大规模知识库
- 为了展示而展示的哲学 RAG

## 5. 下一步建议

建议下一步按这个顺序推进：

1. 写 `prompts/advisor_system_prompt.md`
2. 写 `prompts/problem_clarifier.md`
3. 写 `prompts/session_summary.md`
4. 写 `prompts/memory_update.md`
5. 建立 `memory/profile.json` 和 `memory/pending_memory.json`
6. 做一个最小可用对话入口
7. 用真实对话测试 V0.1 核心链路

## 6. Agent-native V0.1 Direction

Current decision:

- V0.1 is not a traditional web app, desktop app, or full CLI.
- V0.1 is an agent-native local workspace.
- The agent reads `AGENTS.md`, `docs/`, `prompts/`, and `memory/` before working.
- The agent clarifies problems, generates strategic summaries, and proposes memory updates.
- The user confirms important memory before it is written.

### Newly Added Foundation Items

- [x] `AGENTS.md`
- [x] `.gitignore`
- [x] `.env.example`
- [x] `memory/MEMORY_POLICY.md`
- [x] `docs/AGENT_NATIVE_V0.1.md`

### New Open Questions

- [ ] Should real user memory files eventually be excluded from Git and replaced with `.example` templates?
- [ ] Should `.env` include only model settings, or also runtime privacy switches?
- [ ] What exact model provider should be used when cloud LLM support is enabled?
- [ ] How should an agent prove it has read the required docs before a serious session?
- [ ] Should session summaries be committed to Git, or treated as private local data?
- [ ] When should local CLI or local Web become necessary?

### New Implementation Backlog

- [ ] Add example memory item templates without private user data.
- [ ] Add a manual test script/checklist for an agent-native session.
- [ ] Add a first sample session summary with synthetic data.
- [ ] Define `.env` loading behavior when implementation starts.
- [ ] Decide whether `memory/profile.json` remains tracked after real personal memory grows.
- [ ] Create a safe process for user-confirmed memory writes.

## 7. Test Feedback - 2026-07-10

Manual Agent-native test showed two important calibration needs.

### 7.1 Do Not Be Prematurely Insightful

Observed issue:

- The agent clarified well, but moved too quickly into complete interpretation and strong essence judgment.
- This can make the user receive the AI's explanation instead of discovering their own structure.

Decision:

- Add “Guided Inquiry Before Strong Judgment”.
- First responses should use light mirroring, preliminary structure, and 1-3 guiding questions.
- Strong essence judgments should usually appear after user clarification, not in the first response.

Updated files:

- [x] `prompts/problem_clarifier.md`
- [x] `prompts/advisor_system_prompt.md`

### 7.2 Session Summary Must Be Short By Default

Observed issue:

- Session Summary was too long for chatbox use.
- It repeated too much analysis and became a new cognitive load.

Decision:

- Default to Chatbox Summary.
- Treat summary as cognitive compression, not full report.
- Full Session Note should be generated only when user explicitly asks.

Updated files:

- [x] `prompts/session_summary.md`
- [x] `prompts/memory_update.md`
- [x] `docs/V0.1_OPERATION_FLOW.md`

### 7.3 Memory Update Must Be More Conservative

Observed issue:

- The agent suggested too many memory items from one conversation.
- Some observations belonged in the session summary, not long-term memory.

Decision:

- Default to 0-1 pending memory suggestions per conversation.
- Use 2 only when clearly useful and distinct.
- Single-conversation patterns should usually stay pending or unrecorded.

Open follow-up:

- [ ] Run another test with the updated prompts.
- [ ] Verify first response is more inquiry-led and less conclusion-heavy.
- [ ] Verify default Session Summary fits in chatbox.
- [ ] Verify Memory Update suggests at most 1-2 pending items.

## Build vs Buy / Open Source Reuse

Status: accepted direction.

Principle:

> 能复用的基础设施不要自己写；真正要自己维护的是认知顾问的方法论。

Decisions:

- Do not build a custom chat UI in V0.1.
- Do not ask the user to manually test many open-source tools one by one.
- The agent should do lightweight research, compare likely candidates, and recommend one next experiment.
- Tool selection should not consume more attention than prompt behavior, memory policy, and evals.
- Current likely sequence: agent-native V0.1 -> one reused chat shell -> memory/workflow infra only if needed.

Candidate tools to watch:

- Open WebUI: local/self-hosted chat interface.
- LibreChat: self-hosted multi-model chat interface.
- LangGraph: workflow orchestration if explicit state machine becomes needed.
- Mem0 / Letta: memory infrastructure if local JSON becomes painful.
- Obsidian / Markdown vault: possible long-term second-brain archive.

Risk:

Open-source tools may quietly reshape the product into a generic chatbot. This must be resisted by keeping Genesis, Constitution, prompts, memory policy, and evals portable.

## Latest Test Feedback To Implement

Accepted:

- high-emotion responses must use “承接 + 极小问题”, not empty companionship
- flash insight sentences should be visually highlighted when genuinely useful
- hide process language more aggressively
- downgrade strong conclusions into stage judgments unless enough clarification has happened
- summaries should be shorter and fit chatbox use

Backlog:

- consider a tiny script later to run eval prompts against a selected model/API
- defer Open WebUI vs LibreChat installation until prompt behavior is more stable
- document first external-shell installation only after choosing one candidate
