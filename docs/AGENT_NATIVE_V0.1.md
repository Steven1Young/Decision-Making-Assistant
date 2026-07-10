# Agent-native V0.1

> V0.1 is not a traditional app.
> V0.1 is an agent-native local workspace.

## 1. Why Agent-native First

The current risk is not that the project lacks a UI.

The current risk is that the system loses its soul before its method is clear.

This project depends more on:

- Constitution
- Genesis
- Prompt design
- Memory policy
- Reflection flow
- Long-term user model

than on a specific frontend.

Therefore V0.1 should first prove that an agent can follow the method:

> messy input → problem clarification → essence judgment → strategic summary → memory update suggestion

## 2. What Agent-native Means

Agent-native means the first usable version is a structured workspace for an agent.

The agent reads:

- `AGENTS.md`
- `docs/`
- `prompts/`
- `memory/`

Then it uses those files to guide conversations with the user.

The agent does not need a dedicated UI at V0.1.

The project directory itself is the operating environment.

## 3. Expected Use

A typical V0.1 session:

```text
User opens an agent in this repository
↓
Agent reads AGENTS.md and required docs
↓
User says: 我现在很乱，帮我梳理
↓
Agent uses problem_clarifier.md
↓
Agent clarifies facts, feelings, assumptions, fears, and value conflicts
↓
Agent forms an essence judgment and tentative view
↓
User continues the conversation
↓
Agent generates Session Summary when appropriate
↓
Agent proposes Memory Update suggestions
↓
User confirms, rejects, or edits memory suggestions
```

## 4. What V0.1 Should Produce

For important sessions, V0.1 should produce:

- clearer problem structure
- essence judgment
- tentative advisor view
- uncertainty list
- strategic session summary
- memory update suggestions

It should not necessarily produce action items every time.

## 5. What V0.1 Does Not Do

V0.1 does not:

- build a full web app
- build a desktop app
- implement multi-user accounts
- auto-write important memory
- upload sensitive content by default
- pretend to be a therapist, lawyer, doctor, or financial advisor
- implement Hermes-style self-improvement
- run autonomous background reflection

## 6. API Key Strategy

API keys are local secrets.

Rules:

- Keep real keys in `.env` only.
- Do not commit `.env`.
- Commit `.env.example` only.
- Default `ALLOW_CLOUD_LLM=false` until cloud behavior is explicitly designed.
- Do not upload sensitive memory by default.

## 7. Memory Strategy

V0.1 memory is manual-confirmation first.

The agent may suggest memory updates.

The user decides whether to:

- confirm
- edit
- reject
- leave pending

Confirmed memory should be written only after explicit approval.

## 8. Future Evolution

Possible path:

```text
Agent-native V0.1
↓
Local CLI or local Web V0.2
↓
Memory Review and Goal Tracking V0.5
↓
Personal Cognitive System V1.0
↓
Hermes-style self-improvement after the core system is stable
```

## 9. Success Criteria

Agent-native V0.1 succeeds if:

- an agent can enter the repo and understand the project identity
- the agent follows the Constitution
- the agent clarifies before advising
- the agent produces useful strategic summaries
- the agent proposes memory updates without auto-confirming them
- the user feels clearer after important conversations
