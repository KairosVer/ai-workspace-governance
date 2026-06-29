# Rule Update and Operation Log Rules

## When to Update Rules

- folder responsibilities change
- AI repeatedly misplaces files
- a safety incident occurs
- the same workflow repeats often enough to standardize
- users explicitly change how the workspace should operate

## Update Principles

- be short and executable
- avoid private details
- resolve conflicts instead of adding contradictory text
- update entry files only when routing changes
- create an operation log entry under `AI_Operations_Log/rule-updates/`

## Operation Log Rules

AI operations should be auditable. Create one log file per operation.

### Log Location

```text
99_Workspace_Rules/AI_Operations_Log/
  rule-updates/    Rule changes (add, modify, split, retire)
  reviews/         Review reports (titles, locations, links, duplicates, orphans)
  migrations/      File moves, directory reorganization, batch renames
  maintenance/     Small maintenance (index creation, template fills, link fixes)
  external/        External operations (system config, tool installation)
```

### Filename Format

```text
YYYY-MM-DD-HHMM-operation-topic.md
```

Use hyphens between date, time, and description. Use one language consistently.

### Log Template

```md
# Operation Log: Brief Title

## Time
YYYY-MM-DD HH:mm

## Operation Type
Rule update / Review / Migration / Maintenance / Other

## Background
Why this operation was needed.

## Rules Read
- 99_Workspace_Rules/00-README.md
- 99_Workspace_Rules/01-Workspace-Structure.md
- 99_Workspace_Rules/99-Safety-Rules.md

## Actions
What was done.

## Paths Affected

| Path | Action | Notes |
| --- | --- | --- |

## Risks and Confirmation
Whether deletion, batch move, overwrite, encoding, or privacy was involved.

## Result
What was completed, what was not.

## Next Steps
Follow-up items.
```

### When to Log (Required)

- Modifying rule files
- Moving or renaming files
- Creating or deleting directories
- Batch fixing links or attachments
- Periodic AI reviews
- Large-scale formatting
- Any user-requested traceable operation

### When Not to Log

- Only answered a question, no files changed
- Only read files, no modifications
- Minor typo fix in a single file, user did not request logging

### Privacy

Operation logs must not contain:

- accounts, keys, tokens
- real personal identity information
- unpublished research or business-sensitive details
- unnecessary local absolute paths

Use relative paths from workspace root.
