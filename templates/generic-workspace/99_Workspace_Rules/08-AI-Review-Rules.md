# AI Review Rules

AI reviews should identify problems and suggest changes without automatically making high-risk edits.

Review areas:

- vague titles
- misplaced files
- broken links or references
- duplicate files or concepts
- stale project folders
- raw material incorrectly placed in knowledge folders
- deliverables without traceable sources

Reports go to:

```text
99_Workspace_Rules/AI_Operations_Log/reviews/
```

Batch rename, batch move, overwrite, and deletion require confirmation.

## Navigation Layer Review

Check that:

- `00_System/00-Home.md` remains a short launch page, not a full index.
- Lifecycle folders keep guide pages inside `00_Guide/`.
- Cross-folder navigation lives in maps, not scattered root-level index files.
- Guide pages do not duplicate long file lists already visible from the filesystem or maps.
