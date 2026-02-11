# name
Locale Key Normalizer

## description
Applies consistent naming and grouping standards to locale keys.

## when to use
- After string extraction.
- Before locale file updates.

## inputs
- Candidate key list
- Existing locale naming conventions

## strict output template
```md
## Locale Key Normalization
### Accepted Keys
- `<key.path>` - reason: `<short>`

### Renamed Keys
- from: `<old>` -> to: `<new>` - severity: `<Major|Minor>`

### Rejected Keys
- `<key.path>` - reason: `<short>` - severity: `<Major|Minor>`
```

## rules
- Markdown only.
- Keep lists concise.
- Severity required for rename/reject impacts.
- No code output.
