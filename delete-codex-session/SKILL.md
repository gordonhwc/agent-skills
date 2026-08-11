---
name: delete-codex-session
description: Use when deleting Codex sessions by ID or for a project.
---

# Delete Codex Sessions

1. Resolve exact session IDs; confirm the list before project-wide deletion.
2. Read each rollout and prepare a brief summary.
3. Delete only with `codex delete --force <session-id>`; never modify Codex state manually.
4. Verify no matching database record or active/archived rollout remains. Stop on mismatch.
5. Put each rollout summary in a Markdown blockquote.
