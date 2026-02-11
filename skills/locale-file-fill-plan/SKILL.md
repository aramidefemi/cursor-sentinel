# name
Locale File Fill Plan

## description
Creates an ordered, minimal plan to fill missing locale keys safely.

## when to use
- After coverage and risk reports are complete.
- Before `locale-implementer` runs.

## inputs
- Locale gap matrix
- Approved key conventions
- Glossary and translation source

## strict output template
```md
## Locale File Fill Plan
### Preconditions
- unresolved_blockers: `<yes|no>`
- open_questions: `<yes|no>`

### Ordered Fill Steps
1. `<locale file>` - keys: `<count>` - severity: `<Blocker|Major|Minor>`
2. `<locale file>` - keys: `<count>` - severity: `<Blocker|Major|Minor>`

### Validation
- parity_check: `<required>`
- stale_key_check: `<required>`
```

## rules
- Markdown only.
- Stop plan if unresolved blockers/open questions are `yes`.
- Keep output structured and brief.
- No code output.
