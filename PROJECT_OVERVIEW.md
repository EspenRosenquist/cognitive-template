# Project Overview — {{PROJECT_NAME}}

This file is the **canonical control plane** for your project.  Fill it out once and keep it up to date as constraints or weights change.  If anything in this repository conflicts with this file, stop and resolve the conflict before proceeding.

## North Star

{{Describe what success looks like for stakeholders.  One or two sentences that anchor the project.}}

## Definition of Done (DoD)

{{List the measurable criteria for project completion.  These should be testable conditions that indicate the project is ready for hand‑off or release.}}

## Constraints & Invariants

Describe what must **never be violated**.  Keep this section short and specific.  Breaking any of these constraints or invariants requires explicit approval under the decision gate policy.

- **Security & Privacy**: {{e.g., no PII exposed; follow GDPR; all data encrypted at rest; …}}
- **Platform / Runtime**: {{e.g., must run on Python 3.11; must deploy offline; must support Podman; …}}
- **Tooling**:
  - Allowed: {{e.g., R, Python, Bash, dbt, …}}
  - Disallowed: {{e.g., external SaaS without approval; …}}
- **Interfaces & Outputs**: {{e.g., API endpoints, file formats, naming conventions, user‑facing reports}}
- **Operational**: {{e.g., must run on Linux; must be deployable via Docker; must be idempotent; …}}

## Optimisation Weights

Use these weights when comparing options.  They are guidelines, not absolute rules.  Adjust them if your project has different priorities.

| Criterion           | Weight | Notes                                                  |
|---------------------|------:|---------------------------------------------------------|
| Human time          |   HIGH | Prefer solutions that reduce manual effort.            |
| Complexity          |   HIGH | Choose simple, boring solutions over clever ones.       |
| Regression risk     |   HIGH | Preserve known‑good behaviour; avoid breaking working parts. |
| Maintainability     |   HIGH | Aim for code and configuration that are easy to understand and extend. |
| Runtime/infra cost  |    MED | Optimise costs only when they materially matter.        |
| User preference     |    LOW | Honour preferences (e.g. language choice) only when explicitly requested. |

## Decision Gates

You must seek approval before proceeding if your change:

1. Alters a published interface or output.
2. Introduces or removes a major dependency or service.
3. Changes data access, privacy, or security posture.
4. Changes deployment topology or runbook obligations.
5. Breaks a declared constraint or invariant or requires an exception.

To test quickly whether a decision gate applies, ask yourself:
- Does this alter a published interface or output contract?
- Does this add or remove a major dependency or service?
- Does this change data access, privacy, or security posture?
- Does this change deployment topology or operational obligations?
- Does this break a constraint or invariant?

If any answer is “yes,” pause implementation and request approval.

## Exec Plan Triggers

An Exec Plan must be authored under `plans/` using the plan template if the change:
- Crosses a decision gate (see above),
- Is expected to take **more than 2–4 hours**,
- Touches security, privacy, access control, deployment automation, or data correctness,
- Introduces **high regression risk**.

Exec Plans are short, self‑contained documents that describe the problem, compare options using the optimisation weights, and define how success will be verified.  They help agents stay on track for larger tasks.

## Working Agreements

- Maintain an ordered **Goal Stack** of three to seven items in `TODO.md`.  This is your active memory.
- Prefer **minimal diffs** and preserve existing interfaces and working code.
- Do not refactor, rename, reorganise, or replace working components unless explicitly requested or an approved RFC exists.
- Every substantive change must include **verification steps** (tests, checks, validation).  Do not consider a change complete until it has been verified.
