# AI Instructions — Cognitive Project Loop

These instructions guide any AI assistant (for example, GitHub Copilot Chat) working in this repository.  They summarise the **Cognitive Project Loop** so that the assistant can act autonomously while staying aligned with your goals and constraints.

## Always

- **Read and follow `PROJECT_OVERVIEW.md`** before proposing changes.
- Keep outputs aligned with the **Goal Stack** in `TODO.md`.
- **Prefer minimal diffs** and preserve working components and interfaces.
- For any substantive change, provide at least **two options**:
  - **Option A** – minimal‑diff / preference‑compatible.
  - **Option B** – efficiency‑first / platform‑native.
- **Quantify trade‑offs** using the weights defined in `PROJECT_OVERVIEW.md` (human time, complexity, regression risk, maintainability).  Use ranges or simple scores as appropriate.
- If a proposal **crosses a Decision Gate** (see `PROJECT_OVERVIEW.md`), stop and ask for explicit approval from the human owner.
- If an **Exec Plan trigger** applies, draft an Exec Plan under `plans/` using `.agent/PLAN_TEMPLATE.md`.  Do **not** implement code until the plan exists and its Acceptance & verification section is defined.

## When to ask for clarification

Ask questions only when one of these is true:

- A required detail for your task is missing and **cannot be deduced from context**.
- A **Decision Gate** is crossed and human approval is required.
- You must choose between mutually exclusive behaviours that are **not** covered by the Goal Stack or constraints.

Otherwise, proceed with reasonable assumptions and clearly document them.

## Deliverable discipline

For planning, RFC, or architecture tasks, your output must be **actionable**.  This means you should specify:

- **Which files or sections to change**,
- **Commands to run** (if any),
- **Verification steps** (tests, checks, manual validations).

Always end substantive responses with a short footer containing:

1. **Alignment Check** – which goals are advanced by the proposed work.
2. **Assumptions** – any assumptions you made because details were missing.
3. **Next Actions** – what you will do next.
4. **Open Decisions** – unresolved choices or risks that need attention.

## Never

- Do **not** refactor, rename, reorganise, or replace working parts unless explicitly requested or an approved RFC exists.
- Do **not** introduce new major dependencies without approval.

---

These instructions allow the agent to act with autonomy, maintaining project coherence while still asking questions when truly necessary.
