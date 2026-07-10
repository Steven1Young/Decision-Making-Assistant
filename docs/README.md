# Docs Index

This directory contains the foundational documents for the Personal Cognitive System.

## Reading Order

1. `CONSTITUTION.md`
   - Defines the principles the system must never violate.
   - Use this to judge future features, prompts, and model behavior.

2. `GENESIS.md`
   - Explains why the project exists and what soul it must preserve.

3. `AGENT_NATIVE_V0.1.md`
   - Explains why the first version is an agent-native local workspace instead of a traditional app.

4. `V0.1_SPEC.md`
   - Defines what the first version should and should not do.
   - Focuses on the first core entry: “我现在很乱，帮我梳理”.

5. `V0.1_OPERATION_FLOW.md`
   - Converts the V0.1 spec into a concrete operating flow.
   - Use this when building or testing the first prototype.

6. `OPEN_QUESTIONS_AND_BACKLOG.md`
   - Tracks undecided questions, implementation backlog, and future work.

## Related Root Files

- `../AGENTS.md`: Operating contract for agents working in this repository.
- `../README.md`: Human-facing project entry.
- `../.env.example`: Local environment template with no secrets.

## Related Directories

- `../prompts/`: Prompt drafts and invocation order.
- `../memory/`: Local memory skeleton and memory policy.

## Decision Rule

When documents conflict, use this priority:

1. User safety and privacy
2. `CONSTITUTION.md`
3. `GENESIS.md`
4. `AGENT_NATIVE_V0.1.md`
5. `V0.1_SPEC.md`
6. `V0.1_OPERATION_FLOW.md`
7. `OPEN_QUESTIONS_AND_BACKLOG.md`

The Constitution protects principles.

Genesis protects the soul.

Agent-native V0.1 defines the first operating shape.

The Spec and Operation Flow guide implementation.

The Backlog records work still in motion.

- BUILD_VS_BUY.md — build-vs-buy strategy: what to reuse, what to build ourselves, and how to avoid reinventing infrastructure.
