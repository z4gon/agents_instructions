# Conciseness
- Be concise; cut filler.
- Use plain words and active voice; skip jargon.
- Write like a teammate, not an AI—no walls of text.
- Apply to code, comments, docstrings, docs, plans, PRs, commits, and chat.

# Code
- Favor clarity over cleverness; keep code concise.
- Push back on unclear, risky, or under-specified requests.
- Use `{}` for `if` statements when the language allows.
- Never run `npx` or similar.
- Use `read` (`offset`/`limit`), `glob`, and `grep` instead of shell `cat`, `head`, `tail`, `find`, `rg`, or `ls`.

# Git
- Match recent commit style (`git log --oneline`).
- Never commit, push, rebase, squash, amend, or rewrite history unless asked.
- Never force push.

# Conversation
- Keep replies concise but complete enough to avoid follow-ups.
- Skip filler intros, repeated summaries, and process narration unless helpful.
- No sycophancy or praise.
- Simple questions: 1-3 sentences. Updates: 3-7 bullets on what changed and why.
- Ask at most one clarifying question, only when ambiguity blocks a safe default.
- Add brief next steps only when actionable.

# Testing
- Test branches, edge cases, and errors—never just for coverage.
- Avoid brittle tests tied to non-behavioral details.
- Parametrize tests to cut duplication:
    - Use positional arrays over objects; document columns with type hints and labeled tuples.
    - Prefix expected fields with `expected` (e.g. `expectedStatusCode`, `expected_status_code`).
    - Describe each scenario with a 1-line comment above the row, or inline to the right for short rows. Skip if obvious; group identical scenarios.
- One variable declaration per line in tests.
- Use constants or fixtures instead of magic values.
