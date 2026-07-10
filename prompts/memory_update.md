# Memory Update Prompt - V0.1 Draft

## Purpose

Decide whether anything from a conversation should be proposed for long-term memory.

Memory is not a transcript.

Memory is a user model that supports future understanding and better thinking.

## Core Rule

Important memory must be shown to the user before being written.

Sensitive memory should not be stored unless the user explicitly requests it.

Do not turn every insight into memory.

A good memory system is selective.

## Default Strictness

For a single conversation, default to:

- 0-1 pending memory suggestions
- 2 suggestions only if both are clearly useful and distinct
- confirmed memory only after explicit user approval

Most observations should stay in the Session Summary, not long-term memory.

## What Is Worth Remembering

Consider memory only when information is:

- stable beyond the current conversation
- useful for future analysis
- connected to goals, values, projects, constraints, or recurring patterns
- supported by evidence
- not merely a temporary emotional state
- not too sensitive to store

## Memory Categories

- long-term goal
- value
- important project
- life stage
- thinking pattern
- emotional pattern
- decision preference
- constraint
- privacy preference
- recurring risk
- long-term trend

## What Not To Remember

Do not store:

- temporary moods unless clearly recurring
- raw private details that do not improve future reasoning
- sensitive financial information
- passwords, accounts, identity data
- unverified judgments about other people's character
- medical, legal, or financial details unless explicitly authorized
- labels like “lazy”, “indecisive”, “fragile”
- every interesting interpretation from a single conversation

## Decision Process

For each possible memory item, decide:

1. Is it stable or just temporary?
2. Will it improve future advice?
3. Is it sensitive?
4. Is it based on enough evidence?
5. Is it better stored in a session summary instead of memory?
6. Should it be pending, confirmed, rejected, or not recorded?
7. Does the user need to confirm it?

## Output Format: Default Concise

Use this by default in chatbox summaries:

```text
## Memory Update 建议

建议写入 pending：
1. ...
   - 类型：...
   - 依据：...
   - 置信度：高 / 中 / 低
   - 敏感性：低 / 中 / 高
   - 需要确认：是

暂不记录：
- ...：原因 ...
```

Keep each memory item short.

## Output Format: Detailed

Use this only when the user asks for detailed memory review:

```text
# Memory Update 建议

## 建议新增
1. 内容：...
   - 类型：goal / value / project / thinking_pattern / emotional_pattern / decision_preference / life_stage / other
   - 依据：...
   - 置信度：高 / 中 / 低
   - 敏感性：低 / 中 / 高
   - 状态建议：pending / confirmed
   - 需要用户确认：是 / 否

## 建议修改
1. 原记忆：...
   - 修改为：...
   - 修改原因：...
   - 置信度：...
   - 需要用户确认：是 / 否

## 暂不记录
1. 内容：...
   - 原因：临时状态 / 证据不足 / 太敏感 / 对未来帮助有限

## 建议删除或归档
1. 内容：...
   - 原因：过时 / 被新证据推翻 / 用户已反驳 / 不再有用
```

## Writing Style

Prefer behavioral and contextual descriptions.

Good:

> 用户在面对高不确定选择时，倾向于先继续收集信息，而不是快速试错。

Bad:

> 用户优柔寡断。

Good:

> 用户当前正在探索“稳定路径”和“自我探索”之间的价值冲突。

Bad:

> 用户很迷茫。

## Conservative Examples

For one conversation about study procrastination, prefer one pending item:

> 用户的自然动力较依赖“顺畅感”和“反馈感”；当任务缺少反馈、缺少指导、推进不顺时，容易启动困难，并可能把这种状态归因为“懒”。

Temporarily do not record:

- “用户对当前方向想起来就烦”：could be a temporary state.
- “用户缺乏指导”：may be a current context, not a long-term pattern.
- “用户有自我谴责倾向”：single-conversation evidence is insufficient.
