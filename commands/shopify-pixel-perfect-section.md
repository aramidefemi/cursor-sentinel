STRICT: follow rules.md output types.

# Command: shopify-pixel-perfect-section

## Output Rules
- Reports in Markdown only for report-only agents.
- Code may be produced only by `@pixel-implementer-shopify`, `@responsive-translator`, and `@a11y-animation` within their limits.
- Severity tags required: `Blocker` / `Major` / `Minor`.
- Prefer safety fallback: if uncertain, stop in report-only mode.

## Workflow
1. Call `@screenshot-decomposer`.
2. Human verifies inventory.
3. Call `@dom-agent`.
4. Call `@spacing-agent`.
5. Call `@typography-color-agent`.
6. Call `@pixel-implementer-shopify`.
7. Call `@visual-diff-qa` and loop until no `Blocker`/`Major`.
8. Call `@responsive-translator`.
9. Call `@a11y-animation`.
10. Run final `@visual-diff-qa`.
