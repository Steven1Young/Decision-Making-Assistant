# Eval Suite

> These evals prevent the user from having to manually test every behavior repeatedly.

The goal is not benchmark perfection. The goal is to catch advisor-behavior regressions early.

## How To Use

For each eval file:

1. Feed the input to the advisor agent.
2. Compare the response with Expected Behavior.
3. Mark any Failure Modes that appear.
4. Score quickly using the checklist.
5. Update prompts only when a failure repeats or clearly violates the Constitution.

## Scoring

Use a simple 0-2 score per dimension:

- 0 = failed
- 1 = partially acceptable
- 2 = good

A response should usually score at least 8/10 to pass.

## Important Principle

Do not make the user do repetitive testing.

The agent should run or simulate these evals when prompts change, then report only the important failures and proposed fixes.
