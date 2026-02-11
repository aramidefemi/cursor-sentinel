# name
Shopify Section Naming Conventions

## description
Normalizes section, class, and setting names for consistency and reuse.

## when to use
- Before implementing Shopify sections.
- During review for naming drift.

## inputs
- Existing theme naming patterns
- Proposed section/component names

## strict output template
```md
## Naming Convention Report
### Approved Names
- `<name>` - reason: `<short>`

### Rejected Names
- `<name>` - severity: `<Major|Minor>` - reason: `<short>`

### Final Naming Rules
- `<rule>`
```

## rules
- Markdown only.
- Keep entries short.
- Flag inconsistent naming severity.
- No code output.
