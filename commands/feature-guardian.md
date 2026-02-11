STRICT: follow rules.md output types.

# Command: feature-guardian

## Output Rules
- Report-only flow.
- Markdown output only.
- Severity tags required: `Blocker` / `Major` / `Minor`.
- No code output.

## Workflow
1. Run skill: `system-defender-feature-checklist`.
2. Call `@system-defender`.
3. Call `@regression-guardian`.
4. Call `@code-tester`.
5. Call `@feature-readability`.
6. If open questions exist -> STOP and ask human.
7. Output final consolidated plan with:
   - Reuse path
   - Minimal change plan
   - Risk notes
   - Test checklist
   - Minor items to skip
