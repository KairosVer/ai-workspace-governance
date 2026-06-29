# Obsidian Vault Adapter

`vault-root/` is a template you can copy into an Obsidian vault root.

Copy options:

- Rules only: copy `99_Vault_Management_Rules/`.
- AI-ready: also copy `AGENTS.md` and one of `.agents/`, `.claude/`, `.codex/`.
- Full workflow: copy the entire `vault-root/`.

Back up your vault before copying. Remove empty directories after copying to fit your needs.

## Rule Files

```text
99_Vault_Management_Rules/
  00-README.md              Overview and reading order
  01-Vault-Structure.md    Folder structure and placement rules
  02-Inbox-Rules.md        Raw material handling
  03-Wiki-Rules.md         Knowledge page standards
  04-Project-Rules.md      Project structure and lifecycle
  05-Output-Rules.md       Deliverable standards
  06-Archive-Rules.md      Cold storage rules
  07-Rule-Update-Rules.md  How to update rules + operation log rules
  08-AI-Review-Rules.md    AI review procedures
  09-Atlas-Rules.md        Navigation and map page rules
  10-AI-Execution-Rules.md Session-level execution triggers
  99-Safety-Rules.md       Safety boundaries (highest priority)
  AI_Operations_Log/        Operation logs (one file per action)
```

## Navigation Layer

```text
8-Atlas/00-Home.md          Launch page (Homepage plugin target)
8-Atlas/90-System-Maps/     System maps
*/00-Guide/                 Local folder guides
```

Use `00-Home.md` as the Homepage plugin target. Use Atlas pages for navigation routes. Use `00-Guide/` pages for local folder purpose and rules.
