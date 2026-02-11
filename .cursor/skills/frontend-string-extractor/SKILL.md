# name
Frontend String Extractor

## description
Extracts frontend-facing English strings into a canonical key candidate list.

## when to use
- Before translation work starts.
- When hardcoded UI copy is suspected.

## inputs
- Frontend source files
- Existing locale key patterns

## strict output template
```md
## Frontend String Extraction
### New String Candidates
- text: `<english text>` - suggested_key: `<key.path>` - severity: `<Blocker|Major|Minor>`

### Existing Key Matches
- text: `<english text>` - key: `<key.path>`

### Conflicts
- `<issue>` - severity: `<Blocker|Major|Minor>`
```

## rules
- Markdown only.
- Keep output short and structured.
- Severity required for conflicts and risky candidates.
- No code output.
