# Code Review

## Description

Asks an AI assistant to perform a thorough code review of a given snippet or file, covering correctness, readability, security, and performance.

## Prompt

```
Please review the following {{language}} code and provide structured feedback.

Code:
```{{language}}
{{code}}
```

Evaluate the code across these dimensions and list concrete, actionable suggestions for each:
1. **Correctness** — logic errors, edge cases, off-by-one errors.
2. **Readability** — naming, structure, comments, and clarity.
3. **Security** — potential vulnerabilities or unsafe practices.
4. **Performance** — inefficiencies or unnecessary resource usage.
5. **Best practices** — adherence to idiomatic {{language}} conventions.

For each issue, include: a short description, the relevant line(s), the severity (low / medium / high), and a suggested fix.
```

## Usage notes

- Replace `{{language}}` with the programming language (e.g. `Python`, `TypeScript`, `Go`).
- Replace `{{code}}` with the actual code to review.
- For large files, consider breaking the review into logical sections.
- Specify a style guide (e.g. PEP 8, Google Style Guide) in the prompt if your project follows one.

## Example output

> **Correctness (high)** — Line 12: The loop condition uses `<=` instead of `<`, causing an off-by-one error when iterating over the array. Suggested fix: change `i <= arr.length` to `i < arr.length`.
>
> **Security (medium)** — Line 27: User input is interpolated directly into the SQL query string. Use a parameterised query instead to prevent SQL injection.
