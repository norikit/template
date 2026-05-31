# CLAUDE.md — entry point for AI agents working in {{PROJECT}}

**You are working on `{{PROJECT}}` (a project of the `norikit` org): {{TAGLINE}}.**

This file is the front door. Before doing substantive work, read the knowledge base.

## ⇒ Start here: the knowledge base

All durable project knowledge lives in **[`ai-docs/`](ai-docs/)**. It is the single source
of truth for design intent — code may not exist yet, but the decisions do. Read in order:

1. **[decisions.md](ai-docs/decisions.md)** — locked architectural choices. Treat as
   constraints; do not relitigate without explicit owner direction.
2. **[architecture.md](ai-docs/architecture.md)** — the evolving system design.
3. **[open-questions.md](ai-docs/open-questions.md)** — what's still undecided.
4. **[status.md](ai-docs/status.md)** — current phase + changelog.
5. **[glossary.md](ai-docs/glossary.md)** — domain terms, as needed.

For **what is being worked on right now**, read the task board at
**[`tasks/`](tasks/)** ([tasks/README.md](tasks/README.md)).

The ecosystem-wide mission, directives, and conventions live in
[`norikit/ai-docs/`](https://github.com/norikit/norikit/tree/main/ai-docs).

## The locked decisions (do not violate without instruction)

<!-- TEMPLATE: restate this project's locked decisions here once recorded in
     ai-docs/decisions.md — e.g. platform, stack, OS floor, UI/config approach. -->

- _Record them in [ai-docs/decisions.md](ai-docs/decisions.md) and mirror the headline here._

## Your responsibility: keep the knowledge base current

**This is a standing instruction from the project owner.** Whenever you make a decision,
land a change, or learn something durable:

- Update the relevant file in `ai-docs/` **in the same change**.
- Decision made → [decisions.md](ai-docs/decisions.md). Design changed →
  [architecture.md](ai-docs/architecture.md). Question resolved → record it and replace its
  entry in [open-questions.md](ai-docs/open-questions.md) with a one-line resolved-pointer.
- Task started/finished → update its `status:` in `tasks/<id>/task.md` and the row in
  [tasks/README.md](tasks/README.md).
- Append a dated line to [status.md](ai-docs/status.md) for meaningful progress.
- Update [README.md](README.md) when user-facing facts (goals, status, build) change.
- New knowledge-base file → link it from [ai-docs/README.md](ai-docs/README.md).

Stale docs are worse than no docs. If you change reality, change the knowledge base.

## Git workflow: always branch, always PR

**This is a standing instruction from the project owner.** Never commit directly to `main`.

- **Work happens in worktrees — start every piece of work by updating to the latest.** Each
  task is developed in its own git worktree branched off `main`; one cut from a stale base
  silently drifts. Always `git fetch origin` first and base the worktree/branch on the
  freshest `origin/main`, never an old local snapshot.
- Sync first: `git fetch origin`, fast-forward local `main` (`git pull --ff-only`), then
  branch off the latest `origin/main` (`git checkout -b <descriptive-branch> origin/main`,
  or `git worktree add -b <descriptive-branch> <path> origin/main`).
- Open a pull request when the task is complete — the PR is the deliverable. Use
  `gh pr create` with a clear title and a body covering what changed, why, and how it was
  verified.
- Keep the PR current: push follow-up commits and `gh pr edit` the title/body.
- License is AGPL-3.0.

## Conventions

- Match surrounding code style; favor clarity and low-latency, main-thread-safe UI code.
- Work items (spikes, milestones, chores) live as task folders under `tasks/` — see
  [tasks/README.md](tasks/README.md). Throwaway PoC code lives in `tasks/<id>/code/` and is
  **not** the product; real product code lives under `Sources/`.
