# Cursor Reusable Framework

This `.cursor/` framework is designed to be copied into any repository and used as a reusable agent system.

## Includes
- Global rules in `.cursor/rules.md`
- Report-only and implementer subagents in `.cursor/subagents/`
- Structured skills in `.cursor/skills/`
- Command orchestrators in `.cursor/commands/`

## Severity Model
- `Blocker`: must be resolved before implementation
- `Major`: should be resolved before merge or release
- `Minor`: log and optionally defer

## Output Contracts
- Report-only agents output Markdown reports only and never output code.
- Implementer agents are the only agents allowed to write code.
- Skills use strict templates and short structured output.
- Commands orchestrate steps and restate output type rules.

## Agent Classes
- Report-only agents: `system-defender`, `regression-guardian`, `code-tester`, `feature-readability`, `ux-friction-sniffer`, `failure-messaging`, `screenshot-decomposer`, `dom-agent`, `spacing-agent`, `typography-color-agent`, `visual-diff-qa`, `i18n-string-inventory`, `locale-coverage-auditor`, `rtl-layout-guardian`, `truncation-overflow-guardian`, `l10n-a11y-verifier`.
- Implementer agents: `pixel-implementer-shopify`, `responsive-translator` (patch-only), `a11y-animation` (patch-only), `implementer-backend`, `implementer-frontend`, `locale-implementer` (locale files only).

## Translation Workflow (shopify only)
Use `.cursor/commands/translate.md` to:
1. Extract frontend English strings.
2. Normalize keys and build locale gap matrix.
3. Audit locale coverage.
4. Run RTL + truncation edge-case checks.
5. Fill all locale files via `locale-implementer`.
6. Run localized accessibility verification.

## Tutorials
### Tutorial 1: Safe Backend Feature Delivery
Goal: ship a backend feature with minimal regression risk.
1. Run `.cursor/commands/backend-feature.md`.
2. Ensure report agents return no unresolved `Blocker`.
3. Resolve open questions with a human if present.
4. Let `implementer-backend` execute minimal approved changes.
5. Re-run report checks and verify tests.

### Tutorial 2: Safe Frontend Feature Delivery
Goal: ship a frontend feature with readability and UX guardrails.
1. Run `.cursor/commands/frontend-feature.md`.
2. Review reuse path, regression notes, test gaps, readability findings.
3. Stop if open questions or `Blocker` exists.
4. Let `implementer-frontend` apply minimal plan.
5. Validate tests and any UX/failure-state notes.

### Tutorial 3: Pixel-Perfect Shopify Section
Goal: reproduce a screenshot accurately with QA loops.
1. Run `.cursor/commands/shopify-pixel-perfect-section.md`.
2. Verify inventory from `screenshot-decomposer`.
3. Approve `dom-agent`, `spacing-agent`, `typography-color-agent` specs.
4. Let `pixel-implementer-shopify` implement section files.
5. Loop `visual-diff-qa` until no `Blocker`/`Major`.
6. Apply responsive + a11y patch agents and run final diff QA.

### Tutorial 4: Full Localization Rollout
Goal: translate frontend English and fill locale files safely.
1. Run `.cursor/commands/translate.md`.
2. Review inventory, key normalization, and locale gap matrix.
3. Review RTL and truncation risk reports.
4. Stop on unresolved `Blocker` or open questions.
5. Let `locale-implementer` fill locale files.
6. Run `l10n-a11y-verifier` before release.

## Use Cases
- Large legacy repo: enforce reuse-first changes and avoid abstraction sprawl.
- Multi-team monorepo: standardize severity tagging and report templates.
- Shopify agency workflow: convert screenshot specs into section delivery with QA loops.
- Global product rollout: detect locale gaps, RTL risks, and truncation issues before launch.
- PR quality gate: run checklist skills to keep tests/readability/regression coverage consistent.

## Adoption Playbook
1. Copy `.cursor/` into your target repository.
2. Keep `rules.md` unchanged first; tune only after 1-2 sprints.
3. Pick one command as team default (`backend-feature`, `frontend-feature`, or `translate`).
4. Require severity-tagged reports before any implementer runs.
5. Track recurring `Major`/`Blocker` patterns and add/update skills.

## Standard Workflow
1. Run a command from `.cursor/commands/`.
2. Follow report agents first to validate reuse path and risks.
3. Stop for human clarification if open questions exist.
4. Run implementer only when plan is approved and no blockers remain.
5. Re-run report/QA agents and enforce severity tagging.

## Copying To Another Repository
1. Copy the entire `.cursor/` directory into the target repository.
2. Keep file paths unchanged.
3. Use command files as entry points.
4. Keep `rules.md` as the highest-priority policy layer.
