# name
System Defender Feature Checklist

## description
Creates a reuse-first readiness checklist for a requested feature.

## when to use
- Before any implementation planning.
- When validating if existing modules can be extended.

## inputs
- Feature request
- Acceptance criteria
- Known touched modules

## strict output template
```md
## Feature Checklist
- [ ] Existing module candidate identified (`Blocker` if none)
- [ ] Extension path defined
- [ ] New abstraction necessity justified
- [ ] Shared dependency impact noted
- [ ] Open questions listed
```

## rules
- Markdown only.
- Keep to checklist format only.
- Tag any failed item as `Blocker`/`Major`/`Minor`.
- No code output.
