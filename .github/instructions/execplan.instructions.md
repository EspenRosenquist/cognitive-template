# ExecPlan Authoring — Prompt File

Use when the user asks to plan complex work or when ExecPlan triggers apply (see `AGENTS.md`).

Requirements:
1) Read `PROJECT_CONSTITUTION.md`, `INVARIANTS.md`, `TODO.md`, and `METRICS.md`.
2) Draft an ExecPlan file in `plans/` using `.agent/PLANS.md` template.
3) Ensure the plan is **self-contained**: do not rely on chat history for critical details.
4) Include at least two options (baseline vs efficiency-first) and quantify via `METRICS.md`.
5) Include Validation & acceptance, and (for ETL/ops) Idempotence & recovery.

Do not implement changes until:
- the ExecPlan exists and
- the Validation & acceptance section is defined and testable.

End with:
- Alignment check
- Assumptions
- Next actions
- Open decisions / risks
