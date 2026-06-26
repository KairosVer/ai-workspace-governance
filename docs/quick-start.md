# 快速开始

## 1. 先备份

在复制模板前，先备份 Obsidian vault。规则模板会影响 AI 如何移动、整理和改写文件，备份永远是第一步。

## 2. 复制模板

把以下目录中的内容复制到你的 vault 根目录：

```text
templates/vault-root/
```

复制后你的 vault 可以长这样：

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
AGENTS.md
.codex/AGENTS.md
.claude/CLAUDE.md
.agents/AGENTS.md
```

如果你只使用某一个 AI 工具，可以只保留对应入口文件。

## 3. 第一次让 AI 读取规则

给 AI 的第一条指令可以这样写：

```text
请先读取 99_Vault_Management_Rules/00-README.md、01-Vault-Structure.md 和 99-Safety-Rules.md。之后再根据任务类型读取对应规则。不要删除或批量移动文件，除非你先列出清单并得到确认。
```

## 4. 日常收集

- 临时想法放入 `3-Inbox/Ideas/`。
- 网页剪藏放入 `3-Inbox/Clippings/`。
- AI 对话或 AI 生成的原始内容放入 `3-Inbox/AI-Chats/`。
- 未判断价值的文件放入 `3-Inbox/Temp/`。

## 5. 日常整理

整理时按这个顺序判断：

```text
原始材料 -> 3-Inbox
长期知识 -> 4-Wiki
具体项目 -> 5-Projects
可交付成果 -> 6-Outputs
冷存储 -> 7-Archive
```

## 6. 定期检查

建议每周让 AI 轻量检查新增文件，每月检查一次 3-Inbox 到 7-Archive。检查报告保存到：

```text
99_Vault_Management_Rules/AI_Operations_Log/reviews/
```

检查只提出建议，不自动批量改名、移动或删除。