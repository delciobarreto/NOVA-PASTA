# Upstream provenance

- Source: https://github.com/virgiliojr94/book-to-skill
- Pinned commit: `e180fc46365e8c1aab0120778cc8a40b9515324b` (2026-10-05, "docs: sync translated skill destinations (#262)"), version 1.4.0 in `pyproject.toml`
- Upstream tag v1.4.0 is `387d938ec58eef578bbd34828a8bba405a3e53a0` (older than the pinned commit)
- Verified: every file kept here is byte-identical to the pinned commit, except `SKILL.md`.
- Local modifications to `SKILL.md` (diff against upstream `SKILL.md` at the pinned commit):
  1. Step 2: input paths passed to `extract.py` as a quoted array (`"${INPUT_PATHS[@]}"`).
  2. Step 10: workdir deletion guarded (requires `metadata.json` + `full_text.txt`; refuses `/`, `$HOME`, cwd); stray code fence fixed.
- Removed from the install (not needed at runtime): tests, docs, CI workflows, images, translations, eval tools.
- Do not run `npx skills update`: it would overwrite the local modifications. To update, review the upstream diff from the pinned commit and re-apply the changes above.
