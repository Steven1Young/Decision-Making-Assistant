# Eval: Learning Procrastination / Guided Clarification

## User Input

```text
我现在很乱，帮我梳理。

我最近总觉得自己应该努力学习，但又很难真正开始。一方面我知道自己还有很多事情要做，另一方面我又总是在拖延、刷东西、逃避。我不确定这是懒，还是目标不清楚，还是我其实对现在的方向没那么相信。

先不要给我行动清单，帮我把这件事拆清楚。
```

## Expected Behavior

The advisor should:

- clarify before advising
- separate facts, feelings, assumptions, fears, and value conflicts lightly
- ask 1-3 high-value questions before making strong claims
- treat “懒” as a hypothesis, not a conclusion
- form only a stage judgment after user answers
- avoid rushing into a complete interpretation
- avoid long Session Summary unless requested

## Strong Signals To Probe

- “应该努力学习” vs “想要学习”
- direction belief vs execution friction
- lack of guidance / feedback
- what previous natural投入 looked like
- whether the problem is content, feedback, or self-blame

## Failure Modes

- gives a full final diagnosis in the first response
- asks too many questions
- overuses “本质就是” too early
- ignores the user’s request to avoid action lists
- transitions abruptly into “Chatbox Summary” or exposes internal workflow language

## Checklist

- Clarification before advice: 0-2
- Guided inquiry quality: 0-2
- Stage judgment instead of final diagnosis: 0-2
- Summary compression if ending: 0-2
- Hidden process language: 0-2

## V0.1 Alignment

This is the main clarify-first eval. First response should use light mirroring, small decomposition, 1-3 questions, and no full productivity plan unless requested.

