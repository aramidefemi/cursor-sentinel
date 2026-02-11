STRICT: follow rules.md output types.

# Command: frontend-feature

## Output Rules
- Orchestrated flow, not narrative.
- Reports in Markdown only.
- Code may be produced only by `@implementer-frontend`.
- Severity tags required: `Blocker` / `Major` / `Minor`.

## Workflow
1. Run `feature-guardian`.
2. If no `Blocker` and no open questions:
   - Call `@implementer-frontend`.
3. If `Blocker` exists or questions remain:
   - STOP and request human clarification/approval.
