---
name: commit-messages
description: Use when the user asks for writing or revising git commit messages.
---

1. Inspect the actual diff before writing or revising a commit message. Do not rely only on the current commit title.
2. Write the title so a reader can tell the commit's purpose from the title itself, not just that something changed.
3. Follow the conventional commit format:
   ```text
   <type>(<scope>): <description>
   ```
   where `scope` is optional and `description` is short and imperative.
4. Prefer naming the main artifact or system in the title when it improves clarity, such as `.gitignore`,
   `pyproject.toml`, the CLI name, or the main workflow being added.
5. Avoid generic titles like `update`, `improve`, or `change` unless the object of the change is explicit.
6. Keep the title brief, imperative, and without a trailing period.
7. If the title alone would hide important context, add a blank line and short point-form bullets.
8. Add bullets when the commit does things like:
    - add a feature that spans several modules
    - rename user-facing names
    - add tool or packaging metadata
    - bundle a few tightly related changes under one purpose
9. Use one of the following common commit types:
    - feat
    - fix
    - docs
    - style
    - refactor
    - test
    - chore
10. Prefer describing *what was added or changed* over explaining *why*.
11. The latest commit content can be inspected for context with:
   ```bash
   git show
   ```
12. When reviewing older commits or rewriting history, inspect each commit's actual diff instead of inferring from the
    existing message.

Example:

```text
feat(cli): add PikPak share URL resolution workflow

- add auth, share, client, workflow, and CLI modules
- support login, share restore, direct URL resolution, and cleanup

chore(gitignore): ignore uv.lock and local auth session file

refactor: rename "pikpak-share" to "pikdirect"

- rename the CLI program
- rename the default auth session file

chore(pyproject): add pyproject.toml for packaging and CLI entry

- define setuptools build metadata
- register the "pikdirect" console script
```
