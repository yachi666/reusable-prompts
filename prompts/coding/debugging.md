# Debugging

## Description

Guides an AI assistant to systematically diagnose a bug given code and an error message or unexpected behaviour.

## Prompt

```
I have a bug in the following {{language}} code. Please help me identify and fix it.

**Code:**
```{{language}}
{{code}}
```

**Error message / unexpected behaviour:**
{{error_or_behaviour}}

**Steps to reproduce (optional):**
{{steps_to_reproduce}}

Please:
1. Identify the root cause of the issue.
2. Explain why it causes the observed error or behaviour.
3. Provide a corrected version of the code.
4. Suggest any defensive coding practices that would prevent similar bugs in the future.
```

## Usage notes

- Replace `{{language}}` with the programming language (e.g. `JavaScript`, `Rust`).
- Replace `{{code}}` with the minimal code that reproduces the bug; a [minimal reproducible example](https://stackoverflow.com/help/minimal-reproducible-example) gets the best results.
- Replace `{{error_or_behaviour}}` with the full error message or a clear description of the wrong behaviour.
- The `{{steps_to_reproduce}}` field is optional but improves diagnosis for environment-specific or timing-related bugs.

## Example output

> **Root cause:** On line 8, `parseInt` is called without a radix argument. When the input string starts with `"0"`, some engines interpret it as octal, returning `0` instead of the expected decimal value.
>
> **Fix:** Change `parseInt(value)` to `parseInt(value, 10)`.
>
> **Defensive practice:** Enable ESLint's `radix` rule to catch missing radix arguments automatically.
