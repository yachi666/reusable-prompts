# Question & Answer

## Description

Prompts an AI assistant to answer a specific question based solely on a provided reference document or knowledge base excerpt, minimising hallucination by grounding the response in the supplied text.

## Prompt

```
Answer the following question using only the information provided in the reference text below.
If the answer cannot be found in the reference text, say "The provided text does not contain enough information to answer this question."

**Question:**
{{question}}

**Reference text:**
{{reference_text}}

Format your answer as:
- **Answer:** A direct, concise response to the question.
- **Supporting quote:** The exact sentence(s) from the reference text that support the answer (or "N/A" if not applicable).
- **Confidence:** High / Medium / Low — based on how explicitly the reference text addresses the question.
```

## Usage notes

- Replace `{{question}}` with the specific question to answer.
- Replace `{{reference_text}}` with the document, article, or knowledge base excerpt to use as the sole source of truth.
- This prompt is particularly useful in retrieval-augmented generation (RAG) pipelines where the context window contains retrieved chunks.
- For multi-hop questions (where the answer requires combining several facts), increase the reference text size or chain multiple calls.

## Example output

**Answer:** The project uses a Redis cluster with three nodes and a configurable TTL per endpoint.

**Supporting quote:** "A Redis cluster (3 nodes) is used; cache TTL is configurable per endpoint via environment variable."

**Confidence:** High
