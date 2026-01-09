# Agents Context (optional)

Use this file if your tooling supports reading an `AGENTS.md` file for AI assistance.
Keep it short.

## Repository intent
This repo uses the Cognitive Project Loop. Canonical docs:
- PROJECT_CONSTITUTION.md
- INVARIANTS.md
- DECISIONS.md
- TODO.md
- METRICS.md

## ExecPlans (for complex work)
- If ExecPlan triggers apply (as defined in this repo), the assistant drafts an ExecPlan in `plans/` using `.agent/PLANS.md`.
- Ask questions only if a Decision Gate is crossed or a missing fact blocks safe progress.
- Do not implement until the plan includes Options A/B (quantified via METRICS.md) and Acceptance & verification.

## How to work here
- Prefer minimal diffs.
- Propose options with quantified trade-offs.
- Do not refactor without an approved RFC.
