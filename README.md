# Cognitive Project Loop — Simplified Template

This simplified template helps you apply the **Cognitive Project Loop** with minimal overhead.

It provides a small set of documents that act as the control plane for your project and a set of instructions for interacting with an AI assistant.  The aim is to give your agent enough context to act autonomously, while still giving you full control over the hard decisions.

## What it provides

- **Project Overview** (`PROJECT_OVERVIEW.md`) — the single source of truth for goals, definition of done, constraints, invariants, optimisation weights and decision gates.
- **Goal Stack and Backlog** (`TODO.md`) — a living list of what you are trying to achieve and what comes next.
- **Decision Log** (`DECISIONS.md`) — a lightweight log of important architectural or policy choices.
- **Context** (`CONTEXT.md`) — a place to capture domain knowledge, glossary terms, data contracts and assumptions.
- **Plan template** (`.agent/PLAN_TEMPLATE.md`) — a short, self‑contained template for any complex change that requires a plan.
- **AI instructions** (`AI_INSTRUCTIONS.md`) — the guidelines your AI assistant should follow when working in this repository.

## Getting started

1. Create a new repository from this template.
2. Open the repository in VS Code and ensure Copilot instruction files are enabled (the setting lives in `.vscode/settings.json` if you use VS Code).
3. Complete the **Bootstrap Checklist** in `TODO.md` and fill in the key sections of `PROJECT_OVERVIEW.md`.
4. Keep the Goal Stack in `TODO.md` updated, use GitHub issues for backlog items, and record decisions in `DECISIONS.md`.
5. For any work that crosses a decision gate, is expected to take more than a few hours or touches security/deployment, create a plan under `plans/` using `.agent/PLAN_TEMPLATE.md`.

## Why simplify?

Previous versions of the Cognitive Project Loop split responsibilities across many files (`PROJECT_CONSTITUTION.md`, `INVARIANTS.md`, `METRICS.md`, etc.).  While expressive, this could feel heavy and discourage adoption.  This simplified template consolidates the most important controls into a single **Project Overview** file and moves the rest into optional documents.  The result is easier to bootstrap and easier for an AI assistant to consume.

## How the AI assistant fits in

Your AI assistant (e.g. GitHub Copilot Chat) reads `AI_INSTRUCTIONS.md` to understand how to work in this repo.  It then uses the information you provide in `PROJECT_OVERVIEW.md` and `TODO.md` to propose solutions, raise questions only when necessary, and maintain alignment with your goals.  See the AI instructions file for details.
