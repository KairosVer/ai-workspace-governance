# Quick Start

For the underlying method, read docs/methodology.md. For immediate use, follow this guide.

This guide helps you add AI workspace governance to an existing folder, repository, knowledge base, or Obsidian vault.

## 1. Back Up First

Before copying templates or asking AI to reorganize files, back up the workspace.

If the workspace is a Git repository, commit or stash current work first.

If it is synced by cloud storage, make sure sync is stable before migration.

## 2. Choose a Template

Generic workspace:

```text
templates/generic-workspace/
```

Obsidian vault:

```text
adapters/obsidian-vault/vault-root/
```

## 3. Copy Governance Rules

Minimal installation:

```text
99_Workspace_Rules/
```

or, for Obsidian:

```text
99_Vault_Management_Rules/
```

Agent-ready installation also copies AI entry files:

```text
AGENTS.md
.codex/AGENTS.md
.claude/CLAUDE.md
.agents/AGENTS.md
```

## 4. First Prompt to AI

```text
Please read the workspace governance rules before making changes. Start with the overview, structure rules, and safety rules. After reading them, summarize the folder responsibilities and safety boundaries. Do not move, delete, rename, or overwrite files until I confirm a concrete plan.
```

## 5. First Review

Ask AI for a review-only pass:

```text
Please review this workspace structure and suggest where files should belong. Only provide recommendations. Do not move, rename, delete, or overwrite anything.
```

## 6. Small Batch Migration

After reviewing suggestions, migrate in small batches.

A good first migration affects:

- one folder, or
- fewer than 10 files, or
- one obvious category such as raw imports, old outputs, or inactive projects.

## 7. Record Operations

When AI changes files, it should create an operation log under the rules directory.

Generic workspace:

```text
99_Workspace_Rules/AI_Operations_Log/
```

Obsidian vault:

```text
99_Vault_Management_Rules/AI_Operations_Log/
```

## 8. Add Navigation Without Clutter

After the rules are installed, add a small navigation layer:

Generic workspace:

```text
00_System/00-Home.md
00_System/10_Maps/Workspace-Map.md
01_Inbox/00_Guide/Inbox-Guide.md
02_Knowledge/00_Guide/Knowledge-Guide.md
03_Projects/00_Guide/Projects-Guide.md
04_Outputs/00_Guide/Outputs-Guide.md
05_Archive/00_Guide/Archive-Guide.md
```

Obsidian vault:

```text
8-Atlas/00-Home.md
8-Atlas/90-System-Maps/Atlas说明.md
3-Inbox/00-Guide/Inbox说明.md
4-Wiki/00-Guide/Wiki说明.md
5-Projects/00-Guide/Projects说明.md
6-Outputs/00-Guide/Outputs说明.md
7-Archive/00-Guide/Archive说明.md
```

Keep Home short. Put cross-folder routes in maps. Put local folder rules in guides.
