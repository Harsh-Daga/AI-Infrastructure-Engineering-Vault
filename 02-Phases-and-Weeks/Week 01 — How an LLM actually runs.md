---
type: week
week: 1
phase: Phase 1 — Foundations
status: done
start: 2026-06-09
end: 13/06/2026
objective: "Build the 10,000-ft systems view of how an LLM runs: tokens, prefill → decode, where GPU time goes."
concepts:
  - "[[Tokenization]]"
  - "[[Prefill vs Decode]]"
  - "[[TTFT vs ITL]]"
project:
  - "[[Level 1 — Run local LLMs]]"
deliverable:
tags:
  - week
  - phase/1
---

# Week 01 — How an LLM actually runs

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Build the 10,000-ft systems view of how an LLM runs: tokens, prefill → decode, where GPU time goes.  
**Concepts:** [[Tokenization]], [[Prefill vs Decode]], [[TTFT vs ITL]]
**Project:** [[Level 1 — Run local LLMs]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Andrej Karpathy "Let's build the GPT Tokenizer" + "Intro to LLMs" (1hr talk) — watch the systems-relevant parts.

1. Watch the runtime-relevant parts of Karpathy's "Intro to LLMs" (1hr); skip the training-loop internals.
2. While watching, write a one-line definition for each: token, prefill, decode, context window.
3. From memory, sketch the prefill→decode pipeline and where the GPU spends time.

## Read (15m)
Jay Alammar, "The Illustrated Transformer" (skim for shapes, not math).

1. Skim the Illustrated Transformer for tensor shapes (Q/K/V, embeddings), not the gradient math.
2. Mark where the sequence-length dimension shows up — that's your future memory cost.
3. Write the one shape that grows with context length.

## Build (20m)
Install Ollama; run a small model (e.g. Llama 3.x 8B). Time first-token vs full-response. Log GPU/CPU/RAM.

## Step-by-step
1. Install Ollama (`curl -fsSL https://ollama.com/install.sh | sh`) and pull a small model: `ollama pull llama3.1:8b`.
2. Run one short prompt and one long-generation prompt with `ollama run --verbose` to capture timing fields.
3. In a second terminal watch the hardware: `nvidia-smi -l 1` (NVIDIA) or `asitop` / Activity Monitor (Apple Silicon).
4. Record `prompt_eval_duration` (prefill) vs `eval_duration` (decode) and tokens/sec for each prompt.
5. Repeat with a much longer prompt and note how TTFT changes while inter-token time stays roughly flat.

## Reflect (5m)
> Where does latency come from before the first token vs between tokens? Why?

## Done when
- [x] You measured time-to-first-token separately from total generation time. ✅ 2026-06-13
- [x] You logged GPU/CPU/RAM during a run. ✅ 2026-06-13
- [x] You can state which phase (prefill vs decode) dominated each prompt and why. ✅ 2026-06-13

## Common pitfalls
- The first run includes model load from disk — warm up once before timing.
- On Apple Silicon there is no `nvidia-smi`; the GPU is Metal — use `asitop`.
- Don't confuse prompt-eval rate (prefill) with token-generation rate (decode).

## Resources
- [[Karpathy — Neural Networks Zero to Hero]]
- [[Andrej Karpathy (YouTube)]]
- [[Jay Alammar — The Illustrated Transformer]]
- [[ollama]]

## Go deeper
- Karpathy, "Deep Dive into LLMs like ChatGPT" (3hr) — the complete mental model.
- Ollama API docs: the `prompt_eval_count` / `eval_count` / `*_duration` fields you just used.

## Tasks
- [x] Study/open [[Karpathy — Neural Networks Zero to Hero]] ✅ 2026-06-13
- [x] Study/open [[Andrej Karpathy (YouTube)]] ✅ 2026-06-13
- [x] Study/open [[Jay Alammar — The Illustrated Transformer]] ✅ 2026-06-13
- [x] Study/open [[ollama]] ✅ 2026-06-13
- [x] **Build:** Install Ollama; run a small model (e.g. Llama 3.x 8B). Time first-token vs full-response. Log GPU/CPU/RAM. ✅ 2026-06-13
- [x] You measured time-to-first-token separately from total generation time. ✅ 2026-06-13
- [x] You logged GPU/CPU/RAM during a run. ✅ 2026-06-13
- [x] You can state which phase (prefill vs decode) dominated each prompt and why. ✅ 2026-06-13
- [x] **Reflect:** answer the week's question in the learning log ✅ 2026-06-13

## Notes
