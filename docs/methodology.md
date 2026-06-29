# Methodology

AI Workspace Governance is a method for managing file-based workspaces that are maintained by both humans and AI agents.

It is not a note-taking method, a project management app, or a prompt library. It is a governance layer for folders.

## Design Principles

1. **Governance is a layer.** Sits above tools, below human intent. Makes judgment explicit, does not replace it.
2. **Purpose beats file type.** A Markdown file can be raw input, knowledge, project work, output, or archive. Place it by purpose.
3. **Raw records deserve protection.** AI should not polish away source context, failed attempts, uncertainty, or original wording.
4. **Entry files route, rules govern.** `AGENTS.md`, `CLAUDE.md` should be short routing files. Detailed policy belongs in a centralized rules folder.
5. **Review before migration.** Review reports are cheap. File moves are consequential. AI should suggest before acting.
6. **Archive before delete.** Uncertainty should become archive, not deletion.
7. **One operation, one log.** A single mutable mega-log becomes unreadable. One operation per log file creates an audit trail.
8. **Public templates must be de-identified.** Use fictional names and relative paths. Do not publish private paths, credentials, or personal notes.

## The Two Loops

### 1. File Lifecycle Loop

Every file is somewhere in a lifecycle:

```text
Capture -> Understand -> Execute -> Deliver -> Retire
```

Maps to folders:

```text
01_Inbox     Capture raw input
02_Knowledge Understand and reuse
03_Projects  Execute active work
04_Outputs   Deliver artifacts
05_Archive   Retire safely
```

This prevents a common failure: treating every file as the same kind of note. A raw transcript, a reusable insight, a project decision, a final report, and an old draft should not live by the same rules.

### 2. Governance Loop

AI operations follow:

```text
Intent -> Route -> Read Rules -> Safety Gate -> Act -> Log -> Review -> Improve Rules
```

This prevents another failure: letting AI act without memory or boundaries.

## The Five Layers

### Layer 1: Structure

Structure gives every folder a job. Good structure rules say:

- what belongs here
- what does not belong here
- when something should leave
- what to do when uncertain

Bad structure rules are just category names with no decision criteria.

### Layer 2: Routing

AI tools read different instruction files (`AGENTS.md`, `CLAUDE.md`, `.codex/AGENTS.md`, etc.). The method keeps those files short. They should only answer:

- where the real rules live
- which rules must be read first
- what safety boundaries are absolute

Detailed policy belongs in the centralized rules folder.

### Layer 3: Safety

High-risk operations:

- deletion
- recursive deletion
- batch moving
- batch renaming
- overwriting user-authored content
- editing files with uncertain encoding
- publishing private material
- changing final outputs

The safety gate: if the action is high-risk, AI lists paths, explains risk, suggests safer alternatives, and waits for confirmation.

### Layer 4: Review

AI is often most useful before it acts. A review pass can identify:

- vague titles
- misplaced files
- duplicate concepts
- stale project folders
- raw dumps inside knowledge areas
- deliverables with missing sources
- archive candidates
- broken links or references

Review reports should be suggestions. They should not silently become migrations.

### Layer 5: Audit

Operation logs answer:

- What happened?
- When did it happen?
- Which rules were read?
- Which files changed?
- What risks were considered?
- What did the user confirm?
- What remains unresolved?

One log file per operation, not one giant mutable log.

## Decision Rules

### File Placement

1. Raw or unprocessed? -> Inbox
2. Reusable understanding? -> Knowledge
3. Active execution? -> Projects
4. Deliverable? -> Outputs
5. Inactive but worth keeping? -> Archive
6. About workspace operation? -> Rules

### AI Action Risk

1. Could this lose user content?
2. Could this break references?
3. Could this publish private information?
4. Could this rewrite source records?
5. Could this affect more than three files?
6. Would rollback be hard?

If yes to any, require confirmation.

## Navigation Layer

The lifecycle folders answer where files live. A separate navigation layer answers how to enter and move through the workspace.

Three surfaces:

| Surface | Purpose | Where |
| --- | --- | --- |
| Home | Launch page for common actions | `00_System/00-Home.md` or `8-Atlas/00-Home.md` |
| Maps / Atlas | Cross-folder routes, topic maps, project maps | `00_System/10_Maps/` or `8-Atlas/` |
| Guides | Local folder instructions | `00_Guide/` inside each lifecycle folder |

This prevents root folders from filling up with loose `index.md` and `README.md` files. Navigation pages should be stable and sparse.

## Customization

**Safe to customize:**

- folder names
- project statuses
- output categories
- metadata fields
- operation log naming convention
- domain-specific subfolders
- language of rule files

**Keep:**

- centralized rules folder
- short AI entry files
- explicit safety rules
- human confirmation for high-risk operations
- one operation log per AI action
- relative paths in public docs and logs

**Adaptation examples:**

```text
# Research workspace
01_Inbox/literature/    02_Knowledge/methods/    03_Projects/experiments/
04_Outputs/papers/     05_Archive/old-runs/

# Writing workspace
01_Inbox/fragments/     02_Knowledge/arguments/   03_Projects/books/
04_Outputs/articles/    05_Archive/old-drafts/

# Code repository docs
docs/inbox/    docs/knowledge/    docs/projects/    docs/outputs/    docs/archive/
.ai-rules/
```

If you rename the rules folder, update AI entry files, quick-start prompts, and any automation that reads rules.

## A Mature Workspace

A mature AI-governed workspace has these properties:

- New material is easy to capture.
- Important knowledge becomes reusable.
- Projects have visible state and next actions.
- Outputs can trace back to sources.
- Old material can be found without cluttering active work.
- AI agents know what to read before acting.
- Risky operations require confirmation.
- Future humans can inspect what AI changed.
