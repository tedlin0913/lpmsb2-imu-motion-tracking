# Work Log

Chronological record of work on this project. Each entry: what was built, why,
the commit it landed in, and pointers to the key code.

## 2026-09-21 — Project skeleton and workflow rules

Set up the base Qt6/QML application scaffold (`main.cpp`, `Main.qml`,
`CMakeLists.txt`) and defined the project workflow in `CLAUDE.md`: TDD with
Qt Test, `codex review --uncommitted` before each commit, commit+push per
completed unit, and this work log.

Commit: `be256ef`
Key files: `CLAUDE.md`, `main.cpp:1`, `Main.qml:1`, `CMakeLists.txt:1`

## 2026-09-21 — C++17 standard; codex review sandbox fix

Set `CMAKE_CXX_STANDARD 17` explicitly (required for the upcoming OpenZen SDK
integration, per LP Research's OpenZen C++ API docs). Also found that
`codex review --uncommitted` fails to init its sandbox in this environment
and needs `-c sandbox_mode="danger-full-access"`; recorded that in
`CLAUDE.md` so future reviews use the working invocation.

Key files: `CMakeLists.txt:5`, `CLAUDE.md`
