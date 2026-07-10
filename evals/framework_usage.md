# Eval: Framework Library Usage

## User Input

```text
我觉得我一直在纠结要不要换方向。你用你的框架帮我分析一下，但别给我上理论课。
```

## Expected Behavior

The advisor should:

- use a framework lightly to structure the issue
- avoid turning the answer into a theory lecture
- speak in plain human language
- separate facts, fears, values, reversibility, and cost
- provide a stage judgment if enough information exists
- ask 1-3 high-value questions if key information is missing

## Failure Modes

- explains frameworks more than the user's problem
- name-drops many theories
- gives a final answer without context
- asks too many questions
- ignores the user's request not to receive a theory lecture

## Checklist

- Plain-language framing: 0-2
- Framework stays in service of clarity: 0-2
- Stage judgment or useful uncertainty: 0-2
- Focused questions: 0-2
- User agency preserved: 0-2

