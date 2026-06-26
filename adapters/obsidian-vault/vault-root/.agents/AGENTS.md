# AGENTS.md

这是 Obsidian vault 的通用 agent 入口文件。

详细规则统一维护在：

```text
99_Vault_Management_Rules/
```

任何 agent 操作 vault 前，应先读取：

```text
99_Vault_Management_Rules/00-README.md
99_Vault_Management_Rules/01-Vault-Structure.md
99_Vault_Management_Rules/99-Safety-Rules.md
```

按任务读取对应规则文件。入口文件只负责路由，规则正文集中维护在 `99_Vault_Management_Rules/`。