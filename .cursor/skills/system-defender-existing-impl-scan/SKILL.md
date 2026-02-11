# name
System Defender Existing Implementation Scan

## description
Finds reusable implementation paths and avoids duplicate logic.

## when to use
- During early feature scoping.
- When similar behavior may already exist.

## inputs
- Feature intent
- Candidate files/modules

## strict output template
```md
## Existing Implementation Scan
### Reuse Candidates
- `<module/path>` - relevance: `<high|medium|low>` - severity if ignored: `<Major|Minor>`

### Extension Path
- Primary extension target: `<module/path>`
- Minimal change rationale: `<one line>`

### Gaps
- `<gap>` - severity: `<Blocker|Major|Minor>`
```

## rules
- Markdown only.
- Short bullets only.
- Severity required for each gap/risk.
- No code output.
