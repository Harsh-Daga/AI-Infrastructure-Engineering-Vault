---
type: "week"
week: 2
phase: "Phase 1 — Foundations"
status: "in-progress"
start: 2026-06-13
end: 
objective: "Tokenization, embeddings, and context-window memory cost."
concepts: ["[[Tokenization]]", "[[Embeddings]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: 
tags: ["week", "phase/1"]
---

# Week 02 — Tokenization, embeddings, context windows

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Tokenization, embeddings, and context-window memory cost.  
**Concepts:** [[Tokenization]], [[Embeddings]]
**Project:** [[Level 1 — Run local LLMs]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Karpathy tokenizer video (finish it); Hugging Face NLP course, tokenization chapter.

1. Finish Karpathy's tokenizer video; pause to run the byte-pair-encoding examples yourself.
2. Read the HF tokenization chapter; note how BPE / WordPiece / Unigram differ.
3. Write why a token (not a word or character) is the model's atomic unit of cost.

## Read (15m)
A model card (Llama / Qwen / DeepSeek) — read it as an infra spec sheet (params, context, precision).

1. Open one model card (Llama/Qwen/DeepSeek) and read it as an infra spec sheet.
2. Extract params, context length, and precision; ignore benchmark tables.
3. Note the context length — you'll multiply it into KV-cache cost next week.

## Build (20m)
Use `tiktoken`/HF tokenizers to count tokens for varied inputs; chart tokens vs characters across languages/code.

## Step-by-step
1. `pip install tiktoken transformers`; load a tokenizer (`tiktoken.get_encoding('cl100k_base')` and an HF tokenizer).
2. Tokenize the same paragraph in English, a non-Latin language, JSON, and source code.
3. Compute tokens-per-character for each and chart it (matplotlib or a quick table).
4. Open a model card (Llama/Qwen/DeepSeek) and note params, context length, and precision as a spec sheet.
5. Estimate KV-cache bytes for the full context: `2 * layers * kv_heads * head_dim * ctx * dtype_bytes`.

## Reflect (5m)
> Why is the token (not the request) the right unit for cost and rate-limiting?

## Done when
- [ ] You have a tokens-vs-characters comparison across languages/code.
- [ ] You can explain why code and non-English text cost more tokens.
- [ ] You computed the memory cost of a full context window for one model.

## Common pitfalls
- Different model families use different tokenizers — don't compare token counts across them naively.
- Whitespace and special tokens count; the chat template adds tokens you didn't type.

## Resources
- [[Karpathy — Neural Networks Zero to Hero]]
- [[Hugging Face NLP Course]]
- [[Llama, DeepSeek & Qwen Technical Reports]]

## Go deeper
- Hugging Face NLP course, tokenization chapter (BPE/WordPiece/Unigram).
- tiktoken README — encoding differences across OpenAI model generations.

## Tasks
- [ ] Study/open [[Karpathy — Neural Networks Zero to Hero]]
- [ ] Study/open [[Hugging Face NLP Course]]
- [ ] Study/open [[Llama, DeepSeek & Qwen Technical Reports]]
- [ ] **Build:** Use `tiktoken`/HF tokenizers to count tokens for varied inputs; chart tokens vs characters across languages/code.
- [ ] You have a tokens-vs-characters comparison across languages/code.
- [ ] You can explain why code and non-English text cost more tokens.
- [ ] You computed the memory cost of a full context window for one model.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
