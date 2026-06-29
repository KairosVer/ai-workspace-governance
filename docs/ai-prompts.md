# AI Prompts

Copy-paste prompts for Codex, Claude Code, or other AI assistants.

All prompts assume AI has read the workspace rules first and follows the Safety Rules (`99-Safety-Rules.md`).

## First Read

```text
Please read the workspace governance rules before making any changes:

- 99_Workspace_Rules/00-README.md
- 99_Workspace_Rules/01-Workspace-Structure.md
- 99_Workspace_Rules/99-Safety-Rules.md

Then summarize your understanding of folder responsibilities and safety boundaries.
Do not move, delete, rename, or overwrite files yet.
```

For Obsidian, use `99_Vault_Management_Rules` instead of `99_Workspace_Rules`.

## Review File Locations

```text
Please review whether files are located in the right folders.

Only suggest changes. For every suggestion, include:
- source path
- suggested target path
- reason
- risk

If more than 3 files would move, wait for my confirmation.
Save the review report under the AI operations log reviews folder.
```

## Check Titles

```text
Please check whether file titles are clear and actionable.

Look for vague titles such as: notes, summary, related, untitled, draft, misc.
Only suggest renames. Do not rename files yet.
```

## Clean Inbox

```text
Please review the Inbox folder.

Classify raw materials into:
- reusable knowledge candidates
- project-related material
- deliverable drafts
- archive candidates

Do not delete, rewrite original records, or batch move without confirmation.
```

## Update Rules

```text
I want to update the workspace governance rules.

First read the rule update rules, operation log rules, and safety rules.
Tell me:
- why this rule update is needed
- which rule files you would change
- whether entry files need updates
- whether existing files need migration

Wait for my confirmation before editing.
```

## Migration Plan

```text
Please produce a migration plan but do not execute it.

Use a table with: source path, target path, reason, risk, link/reference impact, confirmation needed.

After I confirm, execute only the confirmed batch and create an operation log.
```