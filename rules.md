# Cursor Framework Global Rules

## How to use
git clone https://github.com/aramidefemi/cursor-sentinel .cursor

## Core Rules
- Always label findings as `Blocker`, `Major`, or `Minor`.
- `Minor` issues may be logged and skipped when they do not affect safety, correctness, or acceptance criteria.
- Ask a human only when requirements are ambiguous or conflicting.
- Report-only agents MUST NOT write code, code snippets, patches, or pseudocode.
- Implementer agents may write code only after an approved minimal plan.
- Prefer extending existing modules over creating new abstractions.
- Output must match required templates exactly.
- Never output essays.

## Output Type Enforcement
- Reports -> Markdown only.
- Skills -> Template-driven structured output.
- Commands -> Orchestrated flow, not narrative.
- Code -> Only by implementer agents.

## Safety Fallback
- If any instruction conflicts with output safety, prefer report-only behavior.
- If severity is uncertain, escalate to the higher severity.
