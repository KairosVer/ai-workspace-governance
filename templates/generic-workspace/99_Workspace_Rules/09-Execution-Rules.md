# Execution Rules

Rules do not execute themselves. A workspace needs session-level triggers to keep rules running.

## Session Start: Read State

When a session involves workspace maintenance, file operations, or review, AI should first read state:

1. Read `00-Home.md` or workspace entry to understand current projects and priorities.
2. Scan `01_Inbox/` for material sitting unprocessed for too long.
3. Scan active projects for empty "next steps" or stale progress.
4. Check `AI_Operations_Log/reviews/` for the last review date. If over 1 month, suggest a review.

State reading is not written to a file. It is reported briefly in the reply.

## After Action: Self-Check

After any file move, rename, delete, or rule update, AI must self-check:

| Check | Method | On failure |
| --- | --- | --- |
| Links | Search for references to moved/renamed files | Fix or report broken links |
| Empty dirs | Check if operation left empty shell directories | Delete or explain |
| Metadata | Check new/modified files have required frontmatter | Fill or flag |
| Operation log | Check if this action needs a log entry | Write log per rules |

Self-check results are reported briefly in the reply.

## Session End: Wrap Up

Before ending a session (user says "done", "commit", or clearly wrapping up):

1. Confirm operation log is written. If not, write it.
2. List unresolved issues discovered but not addressed.
3. Write "next steps" suggestion in the log.

## Trigger-Action Table

| Trigger | Required action | Output |
| --- | --- | --- |
| Create knowledge page | Write frontmatter (type/status/created/updated/source) | Page ready |
| Create project folder | Create `index.md` with goal/status/next-steps | Project home ready |
| Move file | Search all references, fix broken links | Links valid |
| Rename 3+ files | List changes, wait for user confirmation | User confirmed |
| Delete file | Move to `05_Archive` instead of deleting | Safe archive |
| Update rule | Write log to `AI_Operations_Log/rule-updates/` | Traceable |
| Migrate files | Write log to `AI_Operations_Log/migrations/` | Traceable |
| Maintenance | Write log to `AI_Operations_Log/maintenance/` | Traceable |
| Inbox stale >2 weeks | Suggest user decide destination | No backlog |
| Project next-steps empty | Suggest user fill in | No stall |

## Review Trigger

- **User-triggered**: User says "review", "check", "audit" → run full review, write report to `reviews/`.
- **AI-suggested**: Session start shows last review >1 month old → suggest review.
- **Operation-triggered**: Large migration (5+ files) → link check before and after, logged in operation record.

## Rule Execution Loop

Every rule should answer:

1. When is it triggered?
2. Who executes it?
3. Where is the result recorded?
4. What happens if it is not executed?

If a rule cannot answer all four, it is a dead rule and should be revised or retired.
