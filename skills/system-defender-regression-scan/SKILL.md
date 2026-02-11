# name
System Defender Regression Scan

## description
Assesses regression risk from dependencies, shared modules, and side effects.

## when to use
- After a draft minimal plan exists.
- Before any implementer agent runs.

## inputs
- Proposed change path
- Shared module map
- Critical flows

## strict output template
```md
## Regression Scan
### Shared Modules At Risk
- `<module>` - severity: `<Blocker|Major|Minor>` - reason: `<short>`

### Side Effects
- `<effect>` - severity: `<Blocker|Major|Minor>`

### Mitigations
- `<mitigation>` mapped to `<risk>`
```

## rules
- Markdown only.
- Use compact sections exactly.
- Severity tag on every risk.
- No code output.
