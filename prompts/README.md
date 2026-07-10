# Prompts

> This directory contains V0.1 prompt drafts for the Personal Cognitive System.

These prompts are not final production prompts. They are design contracts for how the advisor should think, respond, summarize, and propose memory updates.

## Files

- `advisor_system_prompt.md`: The top-level identity, constitution, behavior rules, privacy rules, and response style.
- `problem_clarifier.md`: The flow for turning messy input into a clearer problem structure.
- `session_summary.md`: The strategic memo / personal review format after important conversations.
- `memory_update.md`: The rules for deciding whether something should be proposed for long-term memory.

## V0.1 Invocation Order

For the first core entry, “我现在很乱，帮我梳理”, use this order:

```text
1. advisor_system_prompt.md
   ↓
2. problem_clarifier.md
   ↓
3. user conversation / clarification
   ↓
4. session_summary.md
   ↓
5. memory_update.md
   ↓
6. user confirms or rejects memory updates
```

## Important Rules

### Do Not Auto-Write Important Memory

Important memory must be proposed to the user first.

Write to `memory/pending_memory.json` only when the system has a structured suggestion that still needs review.

Write to `memory/confirmed_memory.json` only after explicit user confirmation.

### Do Not Force Action Items

Some conversations should end with clearer understanding rather than a task list.

Only include next steps when they naturally help.

### Do Not Overuse Frameworks

Frameworks should serve analysis.

Do not show off frameworks. Mention the framework lightly when it helps. Expand only if the user asks.

### Do Not Confuse Emotion With Identity

Temporary emotion should not become permanent user memory.

Prefer:

> The user is currently under pressure around a specific decision.

Avoid:

> The user is anxious.

### Do Not Upload Sensitive Information By Default

Sensitive content should remain local unless the user explicitly authorizes otherwise.

## Minimal Runtime Contract

A minimal implementation should support:

1. Load `advisor_system_prompt.md` as the system-level instruction.
2. Choose `problem_clarifier.md` for messy or ambiguous inputs.
3. Generate a response that clarifies rather than solves too early.
4. When the user says the conversation is complete, generate a session summary.
5. Generate memory update suggestions separately from confirmed memory.
6. Ask the user to confirm memory updates before writing them into confirmed memory.

## Future Prompt Files

Likely future additions:

- `challenge_policy.md`
- `privacy_guard.md`
- `framework_selection.md`
- `monthly_review.md`
- `memory_review.md`
- `goal_tracking.md`
