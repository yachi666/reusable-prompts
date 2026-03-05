# Summarization

## Description

Condenses a long piece of text (article, document, meeting notes, etc.) into a concise summary at a level of detail you choose.

## Prompt

```
Summarize the following text.

**Text:**
{{text}}

**Desired length:** {{desired_length}}
**Audience:** {{audience}}
**Format:** {{format}}

Guidelines:
- Retain all key facts, decisions, and action items.
- Use the audience's vocabulary; avoid unexplained jargon if the audience is non-technical.
- Do not add information that is not present in the original text.
- If the format is "bullet points", use a maximum of {{max_bullets}} bullets.
- If the format is "paragraph", aim for {{desired_length}} words.
```

## Usage notes

- Replace `{{desired_length}}` with a target length such as `3 bullet points`, `one paragraph (~100 words)`, or `executive summary (200 words)`.
- Replace `{{audience}}` with a description of the reader, e.g. `engineering team`, `non-technical stakeholders`, `project manager`.
- Replace `{{format}}` with `bullet points` or `paragraph`.
- Omit `{{max_bullets}}` or `{{desired_length}}` if the corresponding format is not chosen.

## Example output

**Summary (3 bullet points, engineering audience):**

- The new caching layer reduced average API response time by 42% in load tests.
- A Redis cluster (3 nodes) is used; cache TTL is configurable per endpoint via environment variable.
- Action item: update the deployment runbook to document Redis connection string requirements before the next release.
