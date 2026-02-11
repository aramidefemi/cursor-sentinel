# name
Backend PR Checklist

## description
Validates backend changes for safety, tests, and regression coverage.

## when to use
- Before opening or approving backend PRs.

## inputs
- Changed backend files
- Test results
- Risk reports

## strict output template
```md
## Backend PR Checklist
- [ ] No unresolved `Blocker`
- [ ] `Major` issues addressed or documented
- [ ] Tests added/updated for changed behavior
- [ ] Shared dependency impact reviewed
- [ ] Rollback/risk note included
```

## rules
- Markdown checklist only.
- Keep concise.
- Escalate missing tests on critical paths to `Blocker`.
- No code output.
