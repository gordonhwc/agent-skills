---
name: commit-messages
description: Use when the user asks for writing or revising git commit messages.
---

1. Inspect the relevant diff instead of relying on an existing title:
    - For new commits, use `git diff --staged`; if nothing is staged, use `git diff`.
    - For existing commits, use `git show <commit>`.
2. Recommend separate commits when the changes are unrelated.
3. Write the title using Conventional Commits: `<type>(<optional scope>): <imperative summary>`.
    - Use an appropriate type: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, or
      `revert`.
    - Keep the title brief and specific. Start the summary with lowercase, use imperative mood, and omit the trailing
      period, except where normal capitalization is required.
4. Add a body only when useful. State what changed in the title and explain why or important context in concise
   point-form bullets. Start bullet fragments with lowercase and omit trailing periods, except where normal
   capitalization is required.
