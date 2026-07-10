# Memory Policy - V0.1

> Memory is the most valuable and most dangerous part of this project.
> It must be maintained deliberately.

## 1. Definition

Memory is not a chat archive.

Memory is a user model that helps the Personal Cognitive System understand the user over time.

It should preserve stable, useful, evidence-backed information that improves future thinking, clarification, and decision support.

## 2. Current Stage

V0.1 memory is manually maintained.

The agent may:

- read confirmed memory when relevant
- propose memory updates
- write pending memory only with clear structure
- write confirmed memory only after explicit user confirmation

The agent must not:

- auto-confirm memory
- store raw conversations by default
- store sensitive information by default
- convert temporary emotions into permanent identity claims

## 3. File Responsibilities

### `profile.json`

A high-level local profile of the user.

Use for stable, user-approved profile-level information:

- long-term goals
- values
- life stage
- important projects
- thinking patterns
- emotional patterns
- decision preferences
- knowledge background
- constraints
- privacy preferences

### `pending_memory.json`

Structured memory suggestions waiting for user review.

Use when an item may be useful but has not yet been confirmed.

### `confirmed_memory.json`

User-approved long-term memory.

Do not write here without explicit confirmation.

### `rejected_memory.json`

Items the user rejected, or items the system decided should not be retained.

Use this to avoid repeatedly suggesting the same bad memory.

### `session_summaries/`

Strategic memo style summaries for important conversations.

Do not store full transcripts here by default.

## 4. What Can Be Remembered

A memory item is worth considering when it is:

- stable beyond the current conversation
- useful for future analysis
- connected to goals, values, projects, constraints, or recurring patterns
- supported by evidence
- not too sensitive to store

Possible categories:

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

## 5. What Should Not Be Remembered

Do not store:

- temporary moods unless they clearly recur
- raw private details that do not improve future reasoning
- unverified judgments about other people’s motives or character
- passwords, accounts, tokens, identity numbers
- sensitive financial details
- medical, legal, tax, or contract details unless explicitly authorized
- labels such as lazy, weak, fragile, indecisive, broken

Avoid turning a moment into an identity.

## 6. Memory Item Quality Standard

A good memory item should include:

- content
- type
- evidence
- confidence
- sensitivity
- status
- created_at
- updated_at if modified
- review_at if relevant

A good memory is phrased as a pattern, preference, constraint, or project state.

Good:

> The user tends to need explicit tradeoff framing before making high-uncertainty choices.

Bad:

> The user cannot make decisions.

## 7. Write Flow

### Step 1: Propose

At the end of an important session, propose memory updates in a separate section.

### Step 2: Classify

Classify each proposal as:

- suggested add
- suggested modify
- do not record
- sensitive, do not record by default
- archive/delete candidate

### Step 3: Ask For Confirmation

Important memory requires user confirmation.

### Step 4: Write Conservatively

After confirmation:

- profile-level stable facts may go to `profile.json`
- specific approved memory may go to `confirmed_memory.json`
- unconfirmed suggestions may go to `pending_memory.json`
- rejected suggestions may go to `rejected_memory.json`

### Step 5: Review Later

Memory should be reviewed periodically.

V0.1: manual review.

V0.5 target: monthly Memory Review.

## 8. Modification And Deletion

Memory must be revisable.

Modify or delete memory when:

- the user says it is wrong
- new evidence contradicts it
- it was a temporary phase
- it becomes too sensitive to retain
- it no longer improves future reasoning

Do not treat old memory as permanently true.

## 9. Sensitivity Levels

Use these levels:

- low: safe project context or general preference
- medium: personal but not highly sensitive
- high: private, financial, medical, legal, relationship, family, or identity-related

High sensitivity items should not be stored by default.

## 10. Manual Review Checklist

Before confirming memory, ask:

- Is this stable?
- Is this useful later?
- Is it supported by evidence?
- Is it too sensitive?
- Is it phrased without harmful labels?
- Would the user agree with this wording?
- Could this become misleading if read months later?

If unsure, keep it pending or do not record it.
