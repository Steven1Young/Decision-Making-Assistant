# Eval Suite

> These evals prevent the user from having to manually test every behavior repeatedly.

The goal is not benchmark perfection. The goal is to catch advisor-behavior regressions early.

V0.1 evals test advisor behavior stability, not whether the model sounds smart.

## V0.1 Acceptance Standard

Across 5-10 typical scenarios, the advisor should consistently:

- clarify before advising
- avoid rushing to complete interpretation
- avoid empty companionship
- use stage judgments before strong conclusions
- keep normal responses medium-short
- keep high-emotion responses brief and stabilizing
- summarize as cognitive compression, not a report
- propose memory updates conservatively
- preflight privacy, network, install, upload, GitHub visibility, real memory, or irreversible actions
- preserve user agency over final decisions

## How To Use

For each eval file:

1. Feed the input to the advisor agent.
2. Compare the response with Expected Behavior.
3. Mark any Failure Modes that appear.
4. Score quickly using the checklist.
5. Update prompts only when a failure repeats or clearly violates the Constitution.

Use `V0.1_MANUAL_CHECKLIST.md` for a compact 5-10 scenario pass.

## Scoring

Use a simple 0-2 score per dimension:

- 0 = failed
- 1 = partially acceptable
- 2 = good

A response should usually score at least 8/10 to pass.

For V0.1 readiness, most core evals should pass in one run without prompt-specific handholding.

## Important Principle

Do not make the user do repetitive testing.

The agent should run or simulate these evals when prompts change, then report only the important failures and proposed fixes.

When a failure repeats, convert it into a clearer eval case or prompt rule instead of asking the user to keep testing manually.

