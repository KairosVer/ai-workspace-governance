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