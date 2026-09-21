# Workflow rules for this project

## Test-driven development
For every new function or method:
1. Discuss the design and test plan with the user first: interface, inputs/outputs,
   edge cases, and what "correct" means. Do not start coding until this is agreed.
2. Write the test first, using **Qt Test (QTest)**. Run it and confirm it fails (red).
3. Write the minimal implementation to make the test pass (green).
4. Refactor if needed, keeping tests green.

## Pre-commit review
Before every commit, run `codex review --uncommitted` against the working tree.
Fix anything it flags before committing. Do not skip this step.

## Commit and push
- Commit after each complete, working unit (a function/method that passes its
  test, or a small cohesive change) — never mid-edit or on a failing/red state.
- Push to `origin` after every commit.

## Work log
- Maintain `WORKLOG.md` at the repo root.
- After each commit, append an entry with: date, what was built, why, the
  commit hash, and file:line pointers to the key code added/changed.
- It's a chronological log, not documentation — keep entries terse.
