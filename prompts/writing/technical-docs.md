# Technical Documentation

## Description

Generates clear technical documentation (such as a README section, API reference entry, or architecture overview) from code or a brief description of a component.

## Prompt

```
Write {{doc_type}} documentation for the following {{subject_type}}.

**{{subject_type}} name:** {{name}}

**Source / description:**
{{source_or_description}}

**Target audience:** {{audience}}

Documentation requirements:
- Use plain, precise language; avoid jargon unless it is standard in the domain.
- Include an **Overview** section (2–4 sentences).
- Include a **Usage** section with at least one concrete example.
- Include a **Parameters / Options** table if applicable (columns: Name, Type, Required, Description).
- Include a **Notes** section for caveats, limitations, or important behaviour.
- Format the output in Markdown.
```

## Usage notes

- Replace `{{doc_type}}` with the type of documentation, e.g. `README`, `API reference`, `architecture overview`.
- Replace `{{subject_type}}` with what you are documenting, e.g. `function`, `CLI tool`, `REST endpoint`, `module`.
- Replace `{{audience}}` with the intended reader, e.g. `developers integrating this library`, `end users`, `new contributors`.
- For code input, paste the complete function or class signature including docstrings if they exist.

## Example output

### `parseDate(input, options)`

**Overview**

Parses a date string into a `Date` object. Accepts ISO 8601 strings and several common regional formats. Returns `null` for unrecognised input rather than throwing.

**Usage**

```javascript
import { parseDate } from './date-utils';

const date = parseDate('2024-06-15');        // Date object for 15 June 2024
const us   = parseDate('06/15/2024', { locale: 'en-US' }); // same date, US format
```

**Parameters**

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `input` | `string` | Yes | The date string to parse. |
| `options.locale` | `string` | No | BCP 47 locale tag used to resolve ambiguous formats. Defaults to `'en-ISO'`. |

**Notes**

- Two-digit years are interpreted as `2000–2099`.
- Time-zone offsets in the input string are preserved; if absent, the local time zone is assumed.
