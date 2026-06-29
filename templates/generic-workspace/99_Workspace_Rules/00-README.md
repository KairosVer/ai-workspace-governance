# Workspace Governance Overview

This directory contains the rules for managing this workspace with AI assistance.

It is not ordinary content. It is the governance layer: structure, file flow, safety boundaries, review procedures, and AI operation logs.

## Required Reading Order

Before changing files, read:

1. `01-Workspace-Structure.md`: decide where content belongs.
2. `99-Safety-Rules.md`: read before any deletion, batch move, encoding, or attachment work.
3. `09-Execution-Rules.md`: AI session start, post-action self-check, session end.
4. `07-Rule-Update-Rules.md`: before modifying rules or writing operation logs.
5. `08-AI-Review-Rules.md`: for checking titles, locations, links, duplicates, and orphans.
6. `10-Navigation-Rules.md`: for creating or maintaining maps and navigation pages.
7. Task-specific rules.

## Rule Priority

1. Current explicit user instruction.
2. Safety rules.
3. Workspace structure rules.
4. Task-specific rules.
5. Local conventions and style preferences.

When uncertain, suggest first and act later.

## Core Workflow

```text
Collect -> 01_Inbox
Understand -> 02_Knowledge
Execute -> 03_Projects
Deliver -> 04_Outputs
Retire -> 05_Archive
Govern -> 99_Workspace_Rules
```

## AI Boundaries

AI may suggest, structure, summarize, format, review, and create templates.

AI must not delete, batch move, batch rename, overwrite, or publish private material without confirmation.

## Operation Logs

AI operations are logged under:

```text
99_Workspace_Rules/AI_Operations_Log/
```

One log file per operation. See `07-Rule-Update-Rules.md` for format and requirements.
