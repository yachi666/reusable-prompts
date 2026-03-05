# Contributing to reusable-prompts

Thank you for helping grow this collection! Follow these guidelines to keep prompts consistent and easy to use.

## Adding a new prompt

1. **Choose the right category** — place the file under `prompts/coding/`, `prompts/writing/`, or `prompts/general/`. If none fits, propose a new category in your pull request.
2. **Name the file clearly** — use lowercase kebab-case, e.g. `unit-test-generation.md`.
3. **Use the standard template** — every prompt file must include the sections shown below.
4. **Use `{{placeholders}}`** — wrap variable parts of the prompt in double curly braces so users know exactly what to replace.
5. **Keep prompts focused** — one prompt per file; break large, multi-step workflows into separate files.
6. **Test your prompt** — run it against at least one AI assistant and include a representative example in the *Example output* section.

## Prompt file template

```markdown
# <Prompt title>

## Description

One or two sentences explaining what this prompt is for and when to use it.

## Prompt

```
<the full prompt text, with {{placeholders}} for variable parts>
```

## Usage notes

- Bullet points explaining any important options, model-specific behaviour, or tips.

## Example output

A brief, representative example of the output you can expect.
```

## Pull request checklist

- [ ] File is placed in the correct category directory.
- [ ] File name is lowercase kebab-case and ends in `.md`.
- [ ] All sections from the template are present.
- [ ] Placeholders use `{{double curly braces}}`.
- [ ] An example output is included.

## Code of conduct

Be respectful and constructive. Prompts that generate harmful, deceptive, or illegal content will not be accepted.
