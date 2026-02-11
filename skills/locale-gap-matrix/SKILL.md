# name
Locale Gap Matrix

## description
Builds a per-locale coverage matrix for all required translation keys.

## when to use
- Before filling locale files.
- During translation QA and release checks.

## inputs
- Canonical key set
- Supported locale list
- Current locale files

## strict output template
```md
## Locale Gap Matrix
| Key | Locale | Status (Present/Missing/Stale) | Severity |
|---|---|---|---|
| `<key.path>` | `<locale>` | `<status>` | `<Blocker|Major|Minor>` |

## Coverage Summary
- `<locale>`: `<x>/<y>` complete
```

## rules
- Markdown table only plus summary bullets.
- Missing core-flow keys are `Blocker`.
- Severity required for each missing/stale entry.
- No code output.
