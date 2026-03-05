# Commit Messages

## Description

Generates a clear, concise Git commit message from a description of the changes made, following the [Conventional Commits](https://www.conventionalcommits.org/) specification.

## Prompt

```
Write a Git commit message for the following change.

**Summary of changes:**
{{change_description}}

**Files affected (optional):**
{{files_affected}}

Rules:
- Follow the Conventional Commits format: `<type>(<scope>): <short description>`.
- Types: feat, fix, docs, style, refactor, test, chore.
- The subject line must be 72 characters or fewer, written in the imperative mood (e.g. "add", not "adds" or "added").
- If the change needs more context, add a body paragraph after a blank line (wrap at 72 characters).
- If there is a breaking change, append `BREAKING CHANGE: <explanation>` in the footer.

Provide only the commit message text, with no additional commentary.
```

## Usage notes

- Replace `{{change_description}}` with a plain-English description of what was changed and why.
- Replace `{{files_affected}}` with a comma-separated list of changed files, or omit the field if not relevant.
- To turn off the Conventional Commits format, remove the format rule and replace it with your team's convention.

## Example output

```
feat(auth): add OAuth2 login with GitHub provider

Users can now sign in using their GitHub account. The existing
username/password flow is unchanged. A new `OAuthProvider` interface
has been introduced to make adding further providers straightforward.
```
