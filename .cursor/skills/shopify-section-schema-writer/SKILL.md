# name
Shopify Section Schema Writer

## description
Produces section schema plans aligned to approved UI structure and naming.

## when to use
- Before creating a new Shopify section.
- When validating schema/settings completeness.

## inputs
- Verified element inventory
- DOM map and style constraints
- Merchant config requirements

## strict output template
```md
## Shopify Section Schema Plan
### Section Identity
- name: `<section name>`
- handle: `<section handle>`

### Settings Model
- `<setting_key>` - type: `<type>` - purpose: `<short>`

### Block Model
- `<block_type>` - fields: `<comma list>`

### Risks
- `<risk>` - severity: `<Blocker|Major|Minor>`
```

## rules
- Markdown only.
- Structured plan only, no prose.
- Severity required for each risk.
- No code output.
