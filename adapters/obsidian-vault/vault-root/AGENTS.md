# AGENTS.md

`D:\ObNotes` Obsidian vault 的入口文件。**所有 AI 的唯一入口点。**

## ⚠️ 在新的对话开始时

**在整理、移动、改写、删除、创建 vault 文件之前，必须先按顺序阅读：**

```text
99_Vault_Management_Rules/00-README.md
99_Vault_Management_Rules/01-Vault-Structure.md
99_Vault_Management_Rules/99-Safety-Rules.md
99_Vault_Management_Rules/10-AI-Execution-Rules.md
```

读完以上三篇之前，**不要动 vault 里的任何文件**。这包括创建新笔记、移动文件、修改内容、删除文件。

## 按任务类型继续阅读

```text
3-Inbox    → 02-Inbox-Rules.md
4-Wiki     → 03-Wiki-Rules.md
5-Projects → 04-Project-Rules.md
6-Outputs  → 05-Output-Rules.md
7-Archive  → 06-Archive-Rules.md
规则更新   → 07-Rule-Update-Rules.md
AI 检查    → 08-AI-Review-Rules.md
Atlas     → 09-Atlas-Rules.md
AI 执行    → 10-AI-Execution-Rules.md
```

## 规则维护

规则新增、修改、拆分、合并、废弃，只能写入：

```text
99_Vault_Management_Rules/
```

**不要把详细规则写到本文件或其他内容目录。**

本文件只是入口路由，指向 `99_Vault_Management_Rules/` 中的集中规则。

## 操作记录

AI 的每次整理、迁移、检查、规则更新，应在以下目录中新建一篇操作记录：

```text
99_Vault_Management_Rules/AI_Operations_Log/
```

操作记录使用中文，不使用 Obsidian 双链。

## 顶层结构

```text
0-Template
1-Attachment
2-Diary
3-Inbox
4-Wiki
5-Projects
6-Outputs
7-Archive
99_Vault_Management_Rules
Z-WeRead
Z-Zotero
```

## 硬性规则

- 安全规则（`99-Safety-Rules.md`）优先于所有整理、清理和效率需求。
- 删除文件优先用回收站，不直接 `rm -rf`。
- vault 内正文链接使用 Obsidian wiki-link，不写绝对路径。
- 与用户交互默认使用中文。
