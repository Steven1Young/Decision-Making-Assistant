# Build vs Buy Strategy

> Principle: buy or reuse infrastructure; build and maintain the cognitive methodology.

This project should not become a full-stack AI product too early.

Its core asset is not a chat UI, a vector database, a model wrapper, or a memory SDK.

Its core asset is:

> A tested methodology that helps the user improve cognitive quality over time.

## 1. Strategic Position

The system should be portable across different shells:

- Codex / Claude Code / ChatGPT-style agents
- Open WebUI / LibreChat-style chat interfaces
- LangGraph / Letta-style agent runtimes
- Mem0 / local JSON / database-backed memory layers
- Obsidian / Markdown / local files as long-term notes

The project should avoid being locked into one runtime unless that runtime clearly improves the cognitive advisor experience.

## 2. What To Reuse

### Chat Interface

Reuse existing chat shells whenever possible.

Candidates:

- Open WebUI: self-hosted AI interface; useful for local-first chat, OpenAI-compatible APIs, and Ollama-style local models.
- LibreChat: self-hosted ChatGPT-like web app; useful for multi-model chat and assistant configuration.
- Existing agent shells: Codex, Claude, ChatGPT, Cursor, or similar tools.

Do not build a custom chat UI in V0.1 unless existing shells clearly block the core workflow.

### Model And API Layer

Reuse model providers and OpenAI-compatible APIs.

Do not write a custom model router early.

V0.1 may use:

- OpenAI API
- OpenRouter or another OpenAI-compatible gateway
- local model endpoints if needed later

Real API keys must remain outside the repository.

### Agent Runtime

Reuse mature agent runtimes only when the workflow needs them.

Candidates:

- LangGraph for stateful workflow, human-in-the-loop, and explicit graph control.
- Letta for stateful agents and memory-centric runtime.
- Existing coding/agent environments for manual V0.1 operation.

Do not introduce a runtime just because it is powerful. Introduce it only when the prompt-only workflow becomes hard to maintain.

### Memory Infrastructure

Reuse memory infrastructure later, but do not outsource memory judgment.

Candidates:

- local JSON / Markdown in V0.1
- Mem0 if persistent AI memory becomes painful to manage manually
- Letta or similar systems if stateful agent memory becomes necessary
- Obsidian or Markdown vault if the system evolves into a second-brain archive

Important distinction:

- Infrastructure can store and retrieve memory.
- This project must decide what deserves to become memory.

Memory policy is part of the system soul and should not be delegated blindly to a third-party tool.

### Knowledge / RAG / File Parsing

Reuse mature tools if needed.

Do not build custom RAG in V0.1.

The Framework Library is not a generic knowledge base. It is a reasoning tool library. It should participate in thinking, not merely provide citations.

## 3. What To Build Ourselves

The following are the project’s real assets and should remain under our control:

- Genesis: why the project exists
- Constitution: principles and boundaries
- Advisor system prompt
- Problem clarification method
- High-emotion handling method
- Session summary compression rules
- Memory update policy
- Reasoning framework selection rules
- Eval cases and scoring standards
- Long-term review method
- Personal methodology accumulated through use

These are not replaceable by open-source infrastructure.

## 4. Open-Source Adoption Rule

Before adopting a tool, ask only these questions:

1. Does it reduce engineering work without changing the advisor identity?
2. Does it support local-first or privacy-sensitive use?
3. Does it allow us to control system prompts and memory rules?
4. Does it make evaluation easier, not harder?
5. Can we leave it later without losing the project soul?

If the answer is unclear, do not spend much time testing it.

## 5. V0.1 Recommendation

V0.1 should remain agent-native.

Use existing agent shells to test the methodology:

```text
Existing Agent Shell
↓
Advisor Prompt
↓
Local Memory Files
↓
Session Summary
↓
Memory Update Proposal
↓
User Confirmation
```

Do not install and compare many tools manually.

The agent should perform lightweight tool research and make a recommendation. The user should only review decisions that affect privacy, cost, lock-in, or workflow direction.

## 6. Likely Adoption Path

### V0.1: Agent-Native

Use Codex / existing agents as the shell.

Focus on:

- prompt behavior
- memory policy
- summary format
- eval cases
- build-vs-buy principles

### V0.2: Reused Chat Shell

Try one chat shell, not five.

Default candidates:

1. Open WebUI if local-first and self-hosted operation matter most.
2. LibreChat if multi-model ChatGPT-like behavior matters most.

The goal is not to pick the perfect tool. The goal is to see whether our advisor prompt survives inside a normal chat UI.

### V0.3: Memory / Workflow Layer

Only after manual memory becomes painful:

- consider Mem0 for persistent memory infrastructure
- consider LangGraph for explicit workflow orchestration
- consider Letta if stateful agent architecture becomes central

## 7. Anti-Patterns

Avoid:

- building a custom UI before the advisor behavior is stable
- installing many frameworks just to compare them
- letting a memory framework decide personal memory without confirmation
- turning the project into a generic chatbot platform
- confusing more features with better cognition
- spending more time on infrastructure than on evals and methodology

## 8. Core Sentence

> The vehicle can be borrowed. The driving method must be ours.

Or in Chinese:

> 底层车可以换，驾驶方法必须是自己的。

## 9. Current External References

These references are candidates, not commitments:

- Open WebUI documentation: https://docs.openwebui.com/
- Open WebUI GitHub: https://github.com/open-webui/open-webui
- LibreChat documentation: https://www.librechat.ai/docs
- LangGraph persistence docs: https://docs.langchain.com/oss/python/langgraph/persistence
- Mem0 documentation: https://docs.mem0.ai/introduction
- Mem0 GitHub: https://github.com/mem0ai/mem0

Keep references lightweight. Do not over-optimize tool selection before the advisor behavior is stable.
