STRICT: follow rules.md output types.

# Command: screenshot-breakdown

## Output Rules
- Report-only flow.
- Markdown output only.
- No code output.
- Severity tags required: `Blocker` / `Major` / `Minor`.

## Workflow
1. Call `@screenshot-decomposer`.
2. Call `@dom-agent`.
3. Output only:
   - Element Inventory
   - DOM Map
