# AGENTS.md

这是 Obsidian vault 的 Codex 入口文件。

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

## 最高优先级

- 用户当前明确指令优先。
- 安全规则高于整理效率。
- 详细规则以 `99_Vault_Management_Rules/` 为准。
- 规则更新只能写入 `99_Vault_Management_Rules/`。
- 操作记录新建到 `99_Vault_Management_Rules/AI_Operations_Log/`，不要反复修改旧记录。