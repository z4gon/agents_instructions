---
description: Load a PR's diff and comments into context, then wait for instructions
---

Read these PRs: $ARGUMENTS

Arguments are PR numbers or URLs, one or more, e.g. `1234` or `https://github.com/org/repo/pull/1234`.

For each PR:

1. Get the diff: `gh pr diff <pr>`
2. Get the title, description, base/head branches: `gh pr view <pr> --json title,body,baseRefName,headRefName`
3. Get the review comments, including inline code comments: `gh pr view <pr> --comments`

If a bare number doesn't resolve, derive `--repo` from the URL form.

Then stop and confirm what you read in one line per PR — number, title, diff size, comment count. Do not review, summarize, or analyze. Wait for instructions.
