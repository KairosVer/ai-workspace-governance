# Methodology

AI Workspace Governance is a method for managing file-based workspaces that are maintained by both humans and AI agents.

It is not a note-taking method, a project management app, or a prompt library. It is a governance layer for folders.

## First Principles

The method rests on five observations about what happens when AI can modify files.

### 1. Capability requires boundaries, not suppression

AI can scan folders, rewrite notes, move files, and maintain projects. This is power. Governance does not remove that power; it makes the power traceable. An AI that acts within explicit boundaries is more useful than one that acts freely but unpredictably.

**Implementation**: Safety rules define high-risk operations. Entry files route agents to rules before they act. Every action has a gate.

### 2. Judgment must be made explicit

Human judgment is implicit and fast: "this belongs here, not there." When AI executes, that judgment must become a written rule. Otherwise AI is either too cautious (asking about every small action) or too aggressive (moving files without understanding why).

**Implementation**: Structure rules say what belongs where, not just category names. Placement is decidable, not subjective.

### 3. Closed loops beat perfect rules

A rough system with feedback is more reliable than a perfect system without it. Rules drift. Folders rot. Projects stall. The question is not "are the rules correct?" but "can the system detect and correct when they are not?"

**Implementation**: Session-start state reading, post-action self-check, session-end logging. Review reports surface drift before it compounds.

### 4. Reversibility takes priority over efficiency

Deletion is irreversible. Archiving is reversible. When uncertain, the system should prefer the reversible option. This is not caution for its own sake; it is the recognition that AI mistakes are cheaper to undo than to discover too late.

**Implementation**: Archive before delete. Batch operations require confirmation. High-risk actions list paths and wait.

### 5. Design for minimum trust

Do not assume AI will read the rules. Design as if AI will forget rules between sessions. Entry files force routing. Operation logs force accountability. Self-checks force verification. Trust is earned through trails, not assumed through prompts.

**Implementation**: Short entry files that must be read first. One log per operation. Post-action self-check as a mandatory step.

### How the principles connect

| Principle | What it produces | Where it lives |
| --- | --- | --- |
| Boundaries | Safety rules | `99-Safety-Rules.md` |
| Explicit judgment | Structure rules | `01-Structure.md`, folder-specific rules |
| Closed loops | Execution rules | `09-Execution-Rules.md` |
| Reversibility | Archive rules, confirmation gates | `06-Archive-Rules.md`, safety gate |
| Minimum trust | Entry files, operation logs | `AGENTS.md`, `07-Rule-Update-Rules.md` |

The rest of this document describes how these principles turn into a working system.

## Design Principles

The following operational principles are derived from the First Principles above:

1. **Governance is a layer.** Sits above tools, below human intent. Makes judgment explicit, does not replace it.
2. **Purpose beats file type.** A Markdown file can be raw input, knowledge, project work, output, or archive. Place it by purpose.
3. **Raw records deserve protection.** AI should not polish away source context, failed attempts, uncertainty, or original wording.
4. **Entry files route, rules govern.** `AGENTS.md`, `CLAUDE.md` should be short routing files. Detailed policy belongs in a centralized rules folder.
5. **Review before migration.** Review reports are cheap. File moves are consequential. AI should suggest before acting.
6. **Archive before delete.** Uncertainty should become archive, not deletion.
7. **One operation, one log.** A single mutable mega-log becomes unreadable. One operation per log file creates an audit trail.
8. **Public templates must be de-identified.** Use fictional names and relative paths. Do not publish private paths, credentials, or personal notes.

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
