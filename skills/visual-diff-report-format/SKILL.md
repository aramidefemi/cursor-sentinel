# name
Visual Diff Report Format

## description
Enforces a consistent severity-based visual diff reporting structure.

## when to use
- Any screenshot vs implementation comparison.
- QA gate before sign-off.

## inputs
- Baseline screenshot
- Current screenshot
- Optional approved specs

## strict output template
```md
## Diff Report
### Severity Summary
- Blocker: `<count>`
- Major: `<count>`
- Minor: `<count>`

### Findings
- `<location>` - `<difference>` - severity: `<Blocker|Major|Minor>`

### Gate
- Status: `<PASS|FAIL>`
- Reason: `<short>`
```

## rules
- Markdown only.
- Every finding must include severity.
- `PASS` requires zero `Blocker` and zero `Major`.
- No code output.
