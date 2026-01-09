
# Project Constitution — {{PROJECT_NAME}}

This document is the **canonical control plane** for the project.
If something conflicts with this document, **flag the conflict and stop** until resolved.

## 1) North Star
{{PLACEHOLDER: One paragraph describing what success looks like for stakeholders.}}

## 2) Definition of Done (DoD)
{{PLACEHOLDER: Paste the DoD checklist for this project (measurable, testable).}}

## 3) Constraints (non-negotiables)
- Security / privacy:
  - {{PLACEHOLDER}}
- Platform / runtime:
  - {{PLACEHOLDER}}
- Tooling (allowed / disallowed):
  - Allowed: {{PLACEHOLDER}}
  - Disallowed: {{PLACEHOLDER}}
- Data classification and access policy:
  - {{PLACEHOLDER}}

## 4) Invariants (must not break)
See `INVARIANTS.md` (normative).

## 5) Optimization weights (default)
These weights govern recommendations. Preferences are captured but **not dominant** unless raised per task.

| Criterion | Weight | Notes |
|---|---:|---|
| Human time | HIGH | Reduce cycles and rework |
| Complexity | HIGH | Prefer simple, boring solutions |
| Regression risk | HIGH | Preserve known-good behavior |
| Maintainability | HIGH | Onboarding and operations matter |
| Runtime/infra cost | MED | Only optimize when material |
| User preference (stack) | LOW | Only increase explicitly |

## 6) Decision gates (requires explicit approval)
1. Change primary language/stack
2. Introduce/remove a major dependency/service
3. Break or modify an invariant interface/output
4. Change security posture, data classification, or access model
5. Cross-repo or multi-module architecture changes

### Decision gate quick test
Ask “yes/no” for each:
- Does this alter a published interface or output contract?
- Does this add/remove a major dependency or service?
- Does this change data access, privacy, or security posture?
- Does this change deployment topology or runbook obligations?
- Does this break an invariant or require an exception?

## 7) ExecPlan policy (complex work)
For changes that cross a Decision Gate, exceed 2–4 hours, or touch security/ETL correctness/deployment automation,
an ExecPlan must be authored under `plans/` (see `AGENTS.md` and `.agent/PLANS.md`) before implementation begins.

## 8) RFC triggers (proposal-only; do not implement without approval)
An RFC must be raised if the recommended change is estimated to provide any of:
- ≥25% reduction in human time vs baseline
- ≥1 point improvement in complexity (see rubric in `METRICS.md`)
- ≥1 point improvement in regression risk
- A major reduction in dependencies or operational burden

### RFC quick test
- Would this change materially improve time, complexity, or risk?
- Does it remove major dependencies or operational burden?
- Would it set a precedent for future architecture decisions?

## 9) Working agreements (Cognitive Project Loop)
- Maintain an ordered **Goal Stack** (3–7 items) in `TODO.md`.
- Prefer **minimal diffs** and preserve interfaces.
- No refactors/renames/reorgs without approval or an accepted RFC.
- Every substantive change includes verification steps (tests, checks, validation).

## 10) Artifacts (Project Pack)
- `README.md` — orientation
- `TODO.md` — goal stack + backlog
- `DECISIONS.md` — decision log (ADR-lite)
- `INVARIANTS.md` — must-not-break rules
- `CONTEXT.md` — glossary, data contracts, domain notes
- `RISK_REGISTER.md` — risks and mitigations
- `METRICS.md` — scoring rubric + estimation guidance
- `RUNBOOK.md` — operations and troubleshooting (if relevant)

## 11) Versioning and release policy
{{PLACEHOLDER: How releases are cut; how schema/migrations are versioned; how to roll back.}}
