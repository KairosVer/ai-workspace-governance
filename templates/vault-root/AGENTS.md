# AGENTS.md

这是 Obsidian vault 的通用 AI 入口文件。

本文件只做入口路由，不写详细规则。详细规则统一维护在：

```text
99_Vault_Management_Rules/
```

## 必读规则

任何 AI 在整理、移动、改写、删除或创建 vault 文件前，必须先读取：

```text
99_Vault_Management_Rules/00-README.md
99_Vault_Management_Rules/01-Vault-Structure.md
99_Vault_Management_Rules/99-Safety-Rules.md
```

按任务类型继续读取：

```text
3-Inbox    -> 02-Inbox-Rules.md
4-Wiki     -> 03-Wiki-Rules.md
5-Projects -> 04-Project-Rules.md
6-Outputs  -> 05-Output-Rules.md
7-Archive  -> 06-Archive-Rules.md
规则更新   -> 07-Rule-Update-Rules.md
AI检查     -> 08-AI-Review-Rules.md
操作记录   -> 09-Operation-Log-Rules.md
```

## 规则更新位置

规则新增、修改、拆分、合并、废弃，只能写入：

```text
99_Vault_Management_Rules/
```

不要把详细规则写散到 AI 入口文件或内容目录中。

## 最高优先级

- 用户当前明确指令优先。
- 安全规则高于整理效率。
- 涉及删除、批量移动、中文文件写入、附件处理时，必须遵守 `99-Safety-Rules.md`。
- vault 内正文链接优先使用 Obsidian wiki-link，不写本机绝对路径。
- AI 的整理、迁移、规则更新、检查操作，应记录为 `99_Vault_Management_Rules/AI_Operations_Log/` 下的新文件。