STRICT: follow rules.md output types.

# Command: translate

## Output Rules
- Orchestrated flow, not narrative.
- Reports in Markdown only.
- Severity tags required: `Blocker` / `Major` / `Minor`.
- Code/file edits are allowed only by `@locale-implementer`.
- Safety fallback: if conflict or uncertainty exists, stop in report-only mode.

## Workflow
1. Run skill: `frontend-string-extractor`.
2. Call `@i18n-string-inventory`.
3. Run skill: `locale-key-normalizer`.
4. Run skill: `locale-gap-matrix`.
5. Call `@locale-coverage-auditor`.
6. Run skill: `rtl-risk-checklist`.
7. Call `@rtl-layout-guardian`.
8. Run skill: `truncation-stress-checklist`.
9. Call `@truncation-overflow-guardian`.
10. If open questions or unresolved `Blocker` exist -> STOP and ask human.
11. Run skill: `locale-file-fill-plan`.
12. Call `@locale-implementer` to fill all locale files.
13. Call `@l10n-a11y-verifier`.
14. Output final `Translation Completion Report` with:
    - Locale files updated
    - Remaining risks
    - RTL/truncation notes
    - Minor items deferred
