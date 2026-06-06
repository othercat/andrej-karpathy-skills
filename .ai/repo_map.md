# Repo Map

## Purpose

This repository is a small guidance/plugin package for applying Karpathy-inspired coding-agent discipline across Claude Code, Cursor, and other agents.

The useful core is not a magical prompt or benchmarked effectiveness claim. It is a compact set of behavioral constraints for coding agents: clarify first, keep changes simple, edit surgically, and verify against explicit success criteria.

## Structure

| Path | Role |
|---|---|
| `CLAUDE.md` | Core 65-line guideline file; local count on 2026-06-06 was 65 lines, 44 non-empty lines. |
| `AGENTS.md` | Root AGENTS variant with the same guideline content; this file was already untracked before this task. |
| `README.md` | English project overview, attribution, installation, and customization notes. |
| `README.zh.md` | Chinese overview, but console output may show mojibake unless read as UTF-8. |
| `CURSOR.md` | Cursor-specific usage notes. |
| `.cursor/rules/karpathy-guidelines.mdc` | Cursor project rule. |
| `skills/karpathy-guidelines/SKILL.md` | Skill packaging of the same four principles. |
| `.claude-plugin/` | Claude plugin packaging metadata. |

## CodeGraph

`codegraph status --json .` was run on 2026-06-06.

- Initial state: `initialized=false`.
- Action taken: `codegraph init .`.
- Result: `initialized=true`, `pendingChanges=0`, `backend=better-sqlite3`.
- `fileCount=0`, `nodeCount=0`, and `languages=[]` are expected for this mostly Markdown/control-plane repository.

Use CodeGraph startup guards anyway. Do not run `codegraph index .` unless the index is broken or the user explicitly requests a forced rebuild.

## Reading Order

For future tasks, start with:

1. `.ai/handover.md`
2. `.ai/repo_map.md`
3. `CLAUDE.md`
4. `README.md`
5. `skills/karpathy-guidelines/SKILL.md` if skill packaging matters
6. `CURSOR.md` or `.cursor/rules/karpathy-guidelines.mdc` only for Cursor-specific work

