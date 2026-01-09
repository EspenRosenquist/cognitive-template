
# Copilot Instructions — Cognitive Project Loop (Repository-wide)

You are assisting in a repository that uses the **Cognitive Project Loop**.
Task-specific instructions in `.github/instructions` may add process when applicable; follow them in addition to these base rules.

Always:
- Read and follow `PROJECT_CONSTITUTION.md` and `INVARIANTS.md` before proposing changes.
- Maintain coherence with the Goal Stack in `TODO.md`.
- Prefer minimal diffs and preserve working components.
- Provide at least **two options** when proposing solutions:
  A) minimal-diff / preference-compatible
  B) efficiency-first / platform-native
- Quantify trade-offs using the rubric in `METRICS.md` (time, complexity, regression risk, maintainability).
- If a proposal crosses a **Decision Gate** (in `PROJECT_CONSTITUTION.md`), require explicit approval.
- If an RFC trigger threshold is met, draft an RFC (proposal only) instead of implementing.

## ExecPlans (required for complex work)
If any ExecPlan trigger applies (see `AGENTS.md`), **only draft/maintain the ExecPlan**; do not implement code/schema changes until the plan exists and Validation & acceptance is defined..

ExecPlan triggers (summary):
- Crosses a Decision Gate
- Estimated work > 2–4 hours
- Touches security boundaries, access control, anonymization, ETL correctness
- Changes deployment automation or operational runbooks
- High regression-risk refactor

When drafting an ExecPlan:
- Use `.agent/PLANS.md` template.
- Include options A/B with quantified evaluation (METRICS.md rubric).
- Include idempotence/recovery for ETL/ops tasks.

Deliverable discipline (planning/RFC/architecture tasks):
- Output should be actionable: file-level changes, commands, and verification steps.
- End substantive responses with: Alignment check / Assumptions / Next actions / Open decisions.

Do not:
- Refactor, rename, reorganize, or replace working parts unless explicitly requested or an RFC is approved.
- Introduce new major dependencies without approval.
