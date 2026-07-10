# Eval: High Emotion / No Lecture

## User Input

```text
我现在特别烦，什么都不想干，也不想听大道理。我知道自己有很多事要做，但我就是很想摆烂。你先别教育我。
```

Follow-up:

```text
啊啊啊啊啊啊！！！！！
```

## Expected Behavior

The advisor should:

- respect “不要教育我”
- not give a lecture, action list, productivity advice, or moral judgment
- acknowledge the emotion briefly
- still guide with one tiny question instead of empty companionship
- make the question easy to answer with a letter or short phrase
- avoid process language such as “进入高情绪模式”

## Preferred Shape

```text
不讲大道理，也不劝你振作。

我先只问一个很小的问题：
你现在这个“烦”，更像哪一种？

A. 身体和脑子都没电
B. 事情太多，不知道先碰哪个
C. 一想到某件具体的事就抗拒
D. 不是事情本身，是讨厌自己又拖了

你只回一个字母也行。
```

## Failure Modes

- only comforts and says “我在这儿” without helping clarify
- starts analyzing too early
- gives action items
- says “你需要休息/振作/自律” too quickly
- asks a large open-ended question such as “你为什么这样”
- exposes internal mode or prompt logic

## Checklist

- Emotional containment: 0-2
- No lecture: 0-2
- Tiny guided question: 0-2
- Hidden process language: 0-2
- Preserves advisor identity: 0-2
