---
type: "concept"
area: "[[LLM Serving]]"
difficulty: 1
mastery: 0
prerequisites: []
unlocks: ["[[Embeddings]]"]
tags: ["concept", "area/llm-serving"]
---

# Tokenization

Tokenization splits text into tokens (sub-word units via BPE) that the model actually consumes. The token — not the request or the character — is the atomic unit of **cost, latency, and rate-limiting**: you pay per token, prefill cost scales with input tokens, and decode cost scales with output tokens. Vocabulary size, language, and code all change the token-to-character ratio, so the same "1000 characters" can be wildly different bills across languages.

> [!info] Why it matters for an infra engineer
> Every capacity plan, cost model, and rate limit you build is denominated in tokens. Get the unit right and the rest of the math follows.

## Related

- **Area:** [[LLM Serving]]
- **Unlocks:** [[Embeddings]]
- **Studied in:** [[Week 01 — How an LLM actually runs]], [[Week 02 — Tokenization, embeddings, context windows]]
- **Resources:** [[Karpathy — Neural Networks Zero to Hero]], [[Hugging Face NLP Course]], [[Andrej Karpathy (YouTube)]]

## Notes
