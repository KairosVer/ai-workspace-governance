# Operation Log Rules

AI operations should be auditable.

Create one log file per operation under:

```text
99_Workspace_Rules/AI_Operations_Log/
```

Use subfolders:

```text
rule-updates/
reviews/
migrations/
maintenance/
```

Recommended filename:

```text
YYYY-MM-DD-HHMM-operation-topic.md
```

Each log should include:

- time
- operation type
- rules read
- files affected
- actions taken
- risks and confirmations
- result
- follow-up

Use plain relative paths, not local absolute paths.