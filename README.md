# reusable-prompts

A curated collection of reusable prompts for AI language models (such as GitHub Copilot, ChatGPT, and others). These prompts are designed to be consistent, composable, and easy to adapt across different projects and workflows.

## What are reusable prompts?

A *reusable prompt* is a carefully worded instruction or template that can be applied repeatedly to get reliable, high-quality results from an AI assistant. Instead of crafting a new prompt from scratch every time, you pick the one that matches your task, fill in the placeholders, and go.

## Repository structure

```
prompts/
├── coding/          # Prompts for software development tasks
│   ├── code-review.md
│   ├── debugging.md
│   └── refactoring.md
├── writing/         # Prompts for documentation and written communication
│   ├── commit-messages.md
│   └── technical-docs.md
└── general/         # General-purpose prompts
    ├── qa.md
    └── summarization.md
```

## How to use a prompt

1. Browse the `prompts/` directory and find the category that matches your task.
2. Open the relevant prompt file and read the **description** and **usage notes**.
3. Copy the prompt text, replace any `{{placeholders}}` with your actual content, and paste it into your AI assistant.

## How to contribute

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding or improving prompts.

## License

This project is licensed under the [Apache License 2.0](LICENSE).
