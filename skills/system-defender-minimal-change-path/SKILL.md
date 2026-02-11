# name
System Defender Minimal Change Path

## description
Converts analysis into a minimal approved execution path.

## when to use
- After reuse and regression scans.
- Before calling implementers.

## inputs
- Reuse report
- Regression report
- Test/gap report

## strict output template
```md
## Minimal Change Path
### Approved Reuse Path
- `<path/module>`

### Ordered Steps
1. `<step>`
2. `<step>`

### Risk Notes
- `<risk>` - severity: `<Blocker|Major|Minor>`

### Minor Items To Skip
- `<item>`
```

## rules
- Markdown only.
- Keep under 12 bullets/lines excluding headings.
- No narrative paragraphs.
- No code output.
