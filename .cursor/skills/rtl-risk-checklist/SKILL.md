# name
RTL Risk Checklist

## description
Identifies directional and layout risks when enabling RTL locales.

## when to use
- During locale rollout planning.
- Before QA sign-off for RTL support.

## inputs
- UI flow list
- Components with directional behavior
- Locale set including RTL languages

## strict output template
```md
## RTL Risk Checklist
- [ ] Direction-sensitive layout validated - severity if failed: `Blocker`
- [ ] Text alignment rules mapped - severity if failed: `Major`
- [ ] Icon direction reviewed - severity if failed: `Major`
- [ ] Input/cursor direction reviewed - severity if failed: `Major`
- [ ] Motion direction reviewed - severity if failed: `Minor`
```

## rules
- Markdown checklist only.
- No narrative paragraphs.
- Keep output compact.
- No code output.
