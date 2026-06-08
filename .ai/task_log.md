# Task Log

## 2026-06-06 - Distill Karpathy-inspired guidelines into Codex global rules

User asked to read this repo, initialize global CodeGraph indexing, and extract the useful part of the 65-line guideline into Codex global settings.

Actions:

- Read existing `.ai/` entrypoints; they were missing.
- Ran `codegraph status --json .`; repository was not initialized.
- Ran `codegraph init .`; result was a healthy local index with no indexed code files, expected for this Markdown guidance repo.
- Built candidate file list before reading project files.
- Read `CLAUDE.md`, `README.md`, `README.zh.md`, `CURSOR.md`, `AGENTS.md`, `EXAMPLES.md`, `skills/karpathy-guidelines/SKILL.md`, and `C:\Users\other\.codex\AGENTS.md`.
- Verified `CLAUDE.md` has 65 lines and 44 non-empty lines.
- Added a compact global Codex section: "先澄清，少做，不乱碰，可验证".
- Created `.ai/` handover files and `.gitignore` for local CodeGraph/AI cache state.

Verification:

- Re-run `codegraph status --json .`.
- Run `git diff --check`.
- Review `git status -sb` for intended scope.
- Result: `codegraph status --json .` reported `initialized=true`, `pendingChanges=0`, `fileCount=0`, `nodeCount=0`.
- Result: `git diff --check` exited cleanly.
- Result: `git status -sb` showed new `.ai/` and `.gitignore`, plus pre-existing untracked root `AGENTS.md`.

## 2026-06-06 - Create global skills and refine AGENTS.md

User asked to further distill the essence into Kimi Code global settings so all projects benefit.

Actions:

- Read the project's core files: `CLAUDE.md`, `AGENTS.md`, `CURSOR.md`, `README.md`, `skills/karpathy-guidelines/SKILL.md`.
- Verified `CLAUDE.md` is exactly 65 lines (44 non-empty), confirming the "65 lines" claim.
- Attempted `codegraph index .`; result: `No files found to index` — expected for a pure Markdown repo. CodeGraph is initialized but has no code symbols to extract.
- Confirmed `~/.codex/config.toml` already has `[mcp_servers.codegraph]` configured globally.
- Created global skill at `~/.kimi/skills/karpathy-guidelines/SKILL.md` for Kimi Code.
- Created global skill at `~/.codex/skills/karpathy-guidelines/SKILL.md` for Codex.
- Refined `~/.codex/AGENTS.md` "全局工程纪律" section:
  - Added correction disclaimer: not a magic prompt, not written by Karpathy, no benchmark proof.
  - Added mapping table linking 先澄清/少做/不乱碰/可验证 to original principles.
  - Enriched each subsection with missing details from the original 65-line file.
  - Added effectiveness criteria at the end.

Verification:

- `codegraph status --json .` still reports `initialized=true`, `pendingChanges=0`.
- Both skill files are readable and follow the project's original content.
- `~/.kimi/config.toml` has `merge_all_available_skills = true`, so the new skill should be auto-loaded.
