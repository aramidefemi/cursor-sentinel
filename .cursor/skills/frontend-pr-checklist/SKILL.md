# name
Frontend PR Checklist

## description
Checks frontend changes for readability, UX, state handling, and tests.

## when to use
- Before opening or approving frontend PRs.

## inputs
- Changed frontend files
- Visual/UX notes
- Test status

## strict output template
```md
## Frontend PR Checklist
- [ ] No unresolved `Blocker`
- [ ] `Major` issues resolved or accepted
- [ ] Error/loading/empty/success states covered
- [ ] Naming and duplication checks passed
- [ ] Tests updated for changed flows
```

## rules
- Markdown checklist only.
- Use severity language for any failed check.
- Keep output short.
- No code output.
