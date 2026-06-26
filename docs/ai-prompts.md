# AI Prompts

These prompts can be copied into Codex, Claude Code, or another AI assistant.

## First Read

```text
Please read the workspace governance rules before making any changes:

- 99_Workspace_Rules/00-README.md
- 99_Workspace_Rules/01-Workspace-Structure.md
- 99_Workspace_Rules/99-Safety-Rules.md

Then summarize your understanding of folder responsibilities and safety boundaries. Do not move, delete, rename, or overwrite files yet.
```

For Obsidian, use:

```text
Please read:

- 99_Vault_Management_Rules/00-README.md
- 99_Vault_Management_Rules/01-Vault-Structure.md
- 99_Vault_Management_Rules/99-Safety-Rules.md
```

## Review File Locations

```text
Please review whether files are located in the right folders according to the workspace rules.

Requirements:
- Only suggest changes. Do not move files.
- For every suggestion, include source path, suggested target path, reason, and risk.
- If more than 3 files would move, wait for my confirmation.
- Save the review report under the AI operations log reviews folder.
```

## Check Titles

```text
Please check whether file titles are clear and actionable.

Look for vague titles such as notes, summary, related, untitled, draft, misc.

Only suggest renames. Do not rename files yet.
```

## Clean Inbox

```text
Please review the Inbox folder.

You may:
- classify raw materials
- identify reusable knowledge candidates
- identify project-related material
- identify deliverable drafts
- suggest archive candidates

You must not:
- delete raw material
- rewrite original records into conclusions
- batch move files without confirmation
```

## Update Rules

```text
I want to update the workspace governance rules.

Please first read the rule update rules, operation log rules, and safety rules. Then tell me:
- why this rule update is needed
- which rule files you would change
- whether entry files need updates
- whether existing files need migration

Wait for my confirmation before editing.
```

## Migration Plan

```text
Please produce a migration plan but do not execute it.

Use a table with:
- source path
- target path
- reason
- risk
- link/reference impact
- confirmation needed

After I confirm, execute only the confirmed batch and create an operation log.
```