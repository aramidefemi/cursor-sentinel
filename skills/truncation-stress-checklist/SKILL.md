# name
Truncation Stress Checklist

## description
Evaluates overflow and truncation resilience for long localized strings.

## when to use
- Before localization release.
- After locale files are updated.

## inputs
- Translated strings
- UI breakpoints
- Component width constraints

## strict output template
```md
## Truncation Stress Checklist
- [ ] Primary CTAs render fully - severity if failed: `Blocker`
- [ ] Form labels do not clip - severity if failed: `Major`
- [ ] Navigation items do not overflow - severity if failed: `Major`
- [ ] Error messages remain readable - severity if failed: `Major`
- [ ] Minor copy truncation documented - severity if failed: `Minor`
```

## rules
- Markdown checklist only.
- Keep concise.
- Use severity language exactly.
- No code output.
