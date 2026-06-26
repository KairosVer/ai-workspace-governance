# Customization Guide

The template is meant to be adapted. Keep the governance pattern even if you rename folders.

## Safe to Customize

- folder names
- project statuses
- output categories
- metadata fields
- operation log naming convention
- domain-specific subfolders
- language of rule files

## Strongly Recommended to Keep

- a centralized rules folder
- short AI entry files
- explicit safety rules
- human confirmation for high-risk operations
- one operation log per AI action
- relative paths in public docs and logs

## Minimal Generic Structure

```text
01_Inbox
02_Knowledge
03_Projects
04_Outputs
05_Archive
99_Workspace_Rules
```

## Obsidian Structure

Use the adapter:

```text
adapters/obsidian-vault/vault-root/
```

## Code Repository Adjacent Docs

Possible adaptation:

```text
docs/inbox/
docs/knowledge/
docs/projects/
docs/outputs/
docs/archive/
.ai-rules/
```

Keep AI rules separate from product documentation.

## Research Workspace

Possible adaptation:

```text
01_Inbox/literature/
02_Knowledge/methods/
03_Projects/experiments/
04_Outputs/papers/
05_Archive/old-runs/
99_Workspace_Rules/
```

## Writing Workspace

Possible adaptation:

```text
01_Inbox/fragments/
02_Knowledge/arguments/
03_Projects/books-or-series/
04_Outputs/articles/
05_Archive/old-drafts/
99_Workspace_Rules/
```

## If You Rename Rules Folder

Update:

- AI entry files
- quick-start prompts
- review rules
- operation log rules
- any automation that reads rules