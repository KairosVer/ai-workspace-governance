# AI Workspace Governance Methodology

AI Workspace Governance is a method for managing file-based workspaces that are maintained by both humans and AI agents.

It is not a note-taking method, a project management app, or a prompt library. It is a governance layer for folders.

## The Core Claim

When AI can act on files, a workspace needs an explicit operating protocol.

That protocol should answer five questions:

1. Where should things go?
2. What should AI read before acting?
3. What actions require human confirmation?
4. How do we inspect the workspace without immediately changing it?
5. How do we remember what AI changed?

## The Two-Loop Model

### 1. The File Lifecycle Loop

Every file is somewhere in a lifecycle:

```text
Capture -> Understand -> Execute -> Deliver -> Retire
```

This maps to folders:

```text
01_Inbox     Capture raw input
02_Knowledge Understand and reuse
03_Projects  Execute active work
04_Outputs   Deliver artifacts
05_Archive   Retire safely
```

The lifecycle prevents a common failure: treating every file as the same kind of note.

A raw transcript, a reusable insight, a project decision, a final report, and an old draft should not live by the same rules.

### 2. The Governance Loop

AI operations follow another loop:

```text
Intent -> Route -> Read Rules -> Safety Gate -> Act -> Log -> Review -> Improve Rules
```

This loop prevents another common failure: letting AI act without memory or boundaries.

## Layer 1: Structure

Structure gives every folder a job.

The goal is not to create a perfect taxonomy. The goal is to make file placement decidable.

Good structure rules say:

- what belongs here
- what does not belong here
- when something should leave
- what to do when uncertain

Bad structure rules are just category names with no decision criteria.

## Layer 2: Routing

AI tools read different instruction files:

```text
AGENTS.md
CLAUDE.md
.codex/AGENTS.md
.claude/CLAUDE.md
.agents/AGENTS.md
```

The method keeps those files short. They should only answer:

- where the real rules live
- which rules must be read first
- what safety boundaries are absolute

Detailed policy belongs in the centralized rules folder.

## Layer 3: Safety

Safety rules define what AI must not do casually.

High-risk operations include:

- deletion
- recursive deletion
- batch moving
- batch renaming
- overwriting user-authored content
- editing files with uncertain encoding
- publishing private material
- changing final outputs

The safety gate is simple:

```text
If the action is high-risk, AI lists paths, explains risk, suggests safer alternatives, and waits for confirmation.
```

## Layer 4: Review

AI is often most useful before it acts.

A review pass can identify:

- vague titles
- misplaced files
- duplicate concepts
- stale project folders
- raw dumps inside knowledge areas
- deliverables with missing sources
- archive candidates
- broken links or references

Review reports should be suggestions. They should not silently become migrations.

## Layer 5: Audit

AI work should leave a trail.

Operation logs answer:

- What happened?
- When did it happen?
- Which rules were read?
- Which files changed?
- What risks were considered?
- What did the user confirm?
- What remains unresolved?

The method uses one log file per operation instead of one giant mutable log.

## Decision Rules

### File Placement

Ask:

1. Is this raw or unprocessed? Put it in Inbox.
2. Is this reusable understanding? Put it in Knowledge.
3. Is this active execution? Put it in Projects.
4. Is this a deliverable? Put it in Outputs.
5. Is this inactive but worth keeping? Put it in Archive.
6. Is this about how the workspace should operate? Put it in Rules.

### AI Action Risk

Ask:

1. Could this lose user content?
2. Could this break references?
3. Could this publish private information?
4. Could this rewrite source records?
5. Could this affect more than three files?
6. Would rollback be hard?

If yes, require confirmation.

## Why This Works

The method separates concerns that are often mixed together:

- collection vs understanding
- project work vs reusable knowledge
- deliverables vs source material
- archive vs deletion
- AI suggestions vs AI actions
- instructions vs audit records

This separation makes AI more useful because it gives agents a smaller, clearer decision space.

## What To Customize

Customize:

- folder names
- metadata fields
- domain-specific subfolders
- operation log format
- review frequency
- adapter conventions

Keep:

- centralized rules
- short AI entry files
- safety gate
- review-before-migration
- archive-before-delete
- operation logs

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