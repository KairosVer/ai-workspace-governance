# Workspace Governance Overview

This directory contains the rules for managing this workspace with AI assistance.

It is not ordinary content. It is the governance layer: structure, file flow, safety boundaries, review procedures, and AI operation logs.

## Required Reading Order

Before changing files, read:

1. `01-Workspace-Structure.md`
2. `99-Safety-Rules.md`
3. `09-Operation-Log-Rules.md` if the task changes files
4. Task-specific rules

## Core Workflow

```text
Collect -> 01_Inbox
Understand -> 02_Knowledge
Execute -> 03_Projects
Deliver -> 04_Outputs
Retire -> 05_Archive
Govern -> 99_Workspace_Rules
```

## Rule Priority

1. Current explicit user instruction.
2. Safety rules.
3. Workspace structure rules.
4. Task-specific rules.
5. Local conventions and style preferences.

When uncertain, suggest first and act later.

## AI Boundaries

AI may suggest, structure, summarize, format, review, and create templates.

AI must not delete, batch move, batch rename, overwrite, or publish private material without confirmation.