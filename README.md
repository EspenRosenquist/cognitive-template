
# Cognitive Project Loop — Repository Template (VS Code + GitHub Copilot)

This repository is a **template** for bootstrapping long-running projects using the **Cognitive Project Loop** operating mode.

It provides:
- A **Project Pack** (constitution, decisions, TODO, invariants, context, risks, metrics)
- GitHub **issue/PR templates** to keep work aligned and traceable
- **Copilot instruction files** so Copilot Chat and code generation stay consistent within VS Code

## What is the Cognitive Project Loop
- One canonical set of docs defines goals, constraints, and invariants.
- Work starts from the Goal Stack and is tracked as Tasks or RFCs.
- Decisions are recorded once and referenced rather than re-litigated.
- Options are compared with a simple rubric to make trade-offs explicit.
- Changes are kept small, verified, and aligned to the North Star.
- Drift is caught early by gates, RFCs, and explicit approvals.

## Start here (15–30 min)
1. Create a new repository from this template (GitHub: **Use this template**).
2. Open in VS Code.
3. Confirm Copilot instruction files are enabled (see `.vscode/settings.json`).
4. Complete the **Bootstrap Checklist** in `TODO.md` (and core sections in `PROJECT_CONSTITUTION.md`).
5. Start work using GitHub issues (Task or RFC) and small PRs.

## Phase 1 (week 1)
- Finish the domain summary, glossary, and data contracts in `CONTEXT.md` (link to source docs where possible).
- Populate `RISK_REGISTER.md` with top risks, mitigations, and owners.
- Define a minimal validation/test harness and initial runbook notes if the project is operational.
- Set a Goal Stack review cadence (weekly or biweekly) and note it in `TODO.md`.
- Create initial backlog items as GitHub issues and keep `TODO.md` focused on the Goal Stack.

## How to use this template
- Treat `PROJECT_CONSTITUTION.md` as the **canonical source of truth** for constraints, weights, and decision gates.
- Record **any decision that changes the architecture, interfaces, security posture, or major dependencies** in `DECISIONS.md`.
- Keep `INVARIANTS.md` short but strict: it prevents accidental refactors.
- Use `RISK_REGISTER.md` for known risks and mitigations.
- Use `METRICS.md` to define the scoring rubric for time/complexity/risk/maintainability.
- Update the Project Constitution contact link in `.github/ISSUE_TEMPLATE/config.yml` to your new repo URL when you create a project from this template.

## Copilot instructions
Copilot custom instructions are read from `.github/copilot-instructions.md` (repository-wide) in supported IDEs. See GitHub Docs.
In VS Code you must also enable instruction files (see `.vscode/settings.json`).

- Core repo-wide instructions: `.github/copilot-instructions.md`
- Additional, focused instruction files: `.github/instructions/*.instructions.md`

## Recommended workflow
- Create a **Task** issue for each deliverable.
- Create an **RFC** issue for changes that cross decision gates or exceed the RFC trigger thresholds.
- Keep PRs small; include the checklist in the PR template.

## What to replace
Search for `{{PLACEHOLDER}}` across the repo and replace with project-specific information.
