# Handover

## Current State

- Repository: `C:\Workspace\KnowledgeRoots\multica-ai\andrej-karpathy-skills`
- Remote: `https://github.com/multica-ai/andrej-karpathy-skills.git`
- CodeGraph is initialized and healthy for this repo.
- This is a documentation/plugin guidance repo; CodeGraph has no code symbols to index, which is expected.
- The local `CLAUDE.md` count was verified on 2026-06-06: 65 lines, 44 non-empty lines.
- Codex global rules were updated in `C:\Users\other\.codex\AGENTS.md` with a refined "全局工程纪律：先澄清，少做，不乱碰，可验证" section.
- Global skills were created at:
  - `C:\Users\other\.kimi\skills\karpathy-guidelines\SKILL.md` (Kimi Code)
  - `C:\Users\other\.codex\skills\karpathy-guidelines\SKILL.md` (Codex)
- `~/.kimi/config.toml` has `merge_all_available_skills = true`, so Kimi Code should auto-merge the new skill.

## Important Notes

- Do not treat README popularity or Karpathy attribution claims as engineering evidence. The durable value is the four behavioral disciplines.
- Root `AGENTS.md` was already untracked before this task; do not assume it was created by the current run.
- `.codegraph/` is local index state and should stay ignored.
- Read UTF-8 files with explicit UTF-8 when using Windows PowerShell to avoid mojibake in Chinese or arrow characters.

## Next Actions

- If asked to publish, stage explicit files only after reviewing `git status -sb`.
- If asked to adapt these rules elsewhere, prefer a compact merge into the target agent's existing rules rather than copying the full `CLAUDE.md` blindly.
- If asked to verify the global skill is working, check that Kimi Code loads `karpathy-guidelines` skill on startup (look for it in the skill list or context).

