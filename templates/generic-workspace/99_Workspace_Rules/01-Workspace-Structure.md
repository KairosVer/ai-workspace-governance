# Workspace Structure Rules

This workspace uses purpose-based folders. Place files by job-to-be-done, not by file type alone.

## Top-Level Structure

```text
00_System
  00-Home.md
  10_Maps/
01_Inbox
  00_Guide/
02_Knowledge
  00_Guide/
03_Projects
  00_Guide/
04_Outputs
  00_Guide/
05_Archive
  00_Guide/
99_Workspace_Rules
```

## 00_System

System files, templates, reusable scripts, configuration notes, and workspace utilities.

Do not place ordinary work notes here.

## 01_Inbox

Raw input and unprocessed material.

Examples:

- temporary notes
- clipped articles
- meeting dumps
- imported documents
- AI chat transcripts
- unclassified files

## 02_Knowledge

Reusable understanding.

Examples:

- concepts
- decisions
- methods
- references
- reusable explanations
- lessons learned across projects

## 03_Projects

Active work.

Examples:

- project plans
- task lists
- progress logs
- decision records
- project-specific notes

## 04_Outputs

Deliverables and publishable artifacts.

Examples:

- reports
- proposals
- articles
- presentations
- specifications
- final documents

## 05_Archive

Cold storage for inactive, completed, deprecated, or uncertain material that should not be deleted yet.

## 99_Workspace_Rules

Governance rules and AI operation logs. Do not store ordinary content here.

## Placement Questions

1. Is it raw or unprocessed? Put it in `01_Inbox`.
2. Is it reusable knowledge? Put it in `02_Knowledge`.
3. Is it part of active execution? Put it in `03_Projects`.
4. Is it a deliverable? Put it in `04_Outputs`.
5. Is it inactive but worth keeping? Put it in `05_Archive`.
6. Is it a governance rule or AI log? Put it in `99_Workspace_Rules`.

## Guide and Map Files

Each lifecycle folder may contain a `00_Guide/` folder for durable local instructions. This keeps guide files from sitting alone in the folder root, where they are easy to mistake for ordinary content.

Recommended guide files:

```text
01_Inbox/00_Guide/Inbox-Guide.md
02_Knowledge/00_Guide/Knowledge-Guide.md
03_Projects/00_Guide/Projects-Guide.md
04_Outputs/00_Guide/Outputs-Guide.md
05_Archive/00_Guide/Archive-Guide.md
```

Guide pages should explain folder purpose, common entry points, and local rules. They should not maintain complete file inventories. Use `00_System/10_Maps/` for discovery maps and cross-folder routes.

`00_System/00-Home.md` is the recommended workspace launch page. It should stay short: common actions first, then links to maps, guides, projects, outputs, and rules.
