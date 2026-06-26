# Migration Checklist

Use this checklist when adding AI workspace governance to an existing workspace.

## Before Migration

- [ ] The workspace is backed up.
- [ ] If using Git, current work is committed or intentionally left uncommitted.
- [ ] If using cloud sync, sync is stable.
- [ ] The rules folder has been copied.
- [ ] The relevant AI entry files have been copied.
- [ ] AI has read the overview, structure rules, and safety rules.
- [ ] AI has produced recommendations before making changes.

## Inventory Existing Areas

- [ ] Raw input areas.
- [ ] Knowledge/reference areas.
- [ ] Active project areas.
- [ ] Output/deliverable areas.
- [ ] Archive or old material areas.
- [ ] Tool-generated or imported areas.
- [ ] Areas that should not be touched yet.

## First Migration Plan

- [ ] Source and target paths are listed.
- [ ] File counts are listed.
- [ ] Overwrite risk is checked.
- [ ] Link/reference risk is checked.
- [ ] Privacy risk is checked.
- [ ] Human confirmation is given for high-risk operations.

## Execution

- [ ] Start with low-risk files.
- [ ] Avoid moving personal/private records unless explicitly requested.
- [ ] Avoid moving tool-generated folders until their role is understood.
- [ ] Do not overwrite same-name files.
- [ ] Check results after each batch.
- [ ] Create an operation log.

## After Migration

- [ ] Inbox still captures raw input easily.
- [ ] Knowledge folders do not contain raw dumps.
- [ ] Project folders have clear current state and next steps.
- [ ] Outputs can trace back to sources.
- [ ] Archive is not treated as trash.
- [ ] Entry files point to the correct rules folder.