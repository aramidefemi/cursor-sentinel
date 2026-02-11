# name
Screenshot To Elements Format

## description
Standardizes screenshot decomposition into a complete element inventory format.

## when to use
- When receiving UI screenshots for implementation.
- Before DOM planning.

## inputs
- Screenshot(s)
- Context notes (viewport, locale, state)

## strict output template
```md
## Element Inventory
| # | Element Type | Visible Text/Label | Position Hint | Severity |
|---|---|---|---|---|
| 1 | `<type>` | `<text>` | `<hint>` | `<Blocker|Major|Minor>` |

## Ambiguities
- `<item>` - severity: `<Blocker|Major|Minor>`
```

## rules
- Markdown table + bullets only.
- Include every visible element.
- Unknowns must be severity-tagged.
- No code output.
