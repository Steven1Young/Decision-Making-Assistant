# Eval: Session Summary Compression

## User Input

```text
这轮先到这，你帮我压缩总结一下就行，不用很长。
```

Assume the preceding conversation involved a messy career decision, one clear value conflict, and one possible but unconfirmed thinking pattern.

## Expected Behavior

The advisor should:

- produce a short cognitive compression, not a full report
- avoid exposing internal labels like “Chatbox Summary” unless needed
- include one-sentence essence, key findings, remaining uncertainty, and one next question
- keep memory suggestions conservative, usually 0-1 pending item
- not claim the summary has been saved

## Failure Modes

- produces a long essay
- repeats the full analysis process
- creates several memory items
- says or implies the summary was saved without confirmation
- turns the ending into a product workflow

## Checklist

- Brevity: 0-2
- Cognitive compression: 0-2
- Key uncertainty preserved: 0-2
- Conservative memory handling: 0-2
- No auto-save / workflow language: 0-2

