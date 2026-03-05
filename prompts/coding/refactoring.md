# Refactoring

## Description

Asks an AI assistant to refactor existing code to improve its structure, readability, or maintainability without changing its observable behaviour.

## Prompt

```
Please refactor the following {{language}} code to improve {{refactoring_goals}}.

**Original code:**
```{{language}}
{{code}}
```

Requirements:
- Do not change the public interface or observable behaviour.
- Prefer small, well-named functions or methods over large blocks.
- Add or update inline comments only where the intent is non-obvious.
- {{additional_constraints}}

After the refactored code, provide a brief summary of the changes made and why each change improves the code.
```

## Usage notes

- Replace `{{refactoring_goals}}` with one or more goals, for example: `readability and testability`, `performance`, `separation of concerns`.
- Replace `{{additional_constraints}}` with project-specific constraints, e.g. `Keep the code compatible with Python 3.8` or leave the placeholder blank.
- Ask the model to produce the refactored code in a diff format (`{{output_format}}: unified diff`) if you want to review changes more easily.
- Run your existing tests after applying the refactored code to verify behaviour is unchanged.

## Example output

**Refactored code:**
```python
def calculate_discount(price: float, rate: float) -> float:
    """Return the discounted price."""
    return price * (1 - rate)
```

**Summary of changes:**
- Extracted the discount calculation into a dedicated function (`calculate_discount`) to make it independently testable.
- Added a type-annotated signature to clarify expected inputs and output.
- Removed the magic number `0.1` by having the caller supply the rate explicitly.
