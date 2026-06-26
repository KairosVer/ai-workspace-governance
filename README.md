# Obsidian Vault Management Rules

一套面向 Obsidian 个人知识库的管理规则模板，重点解决三件事：

1. 笔记应该放在哪里。
2. AI 助手整理笔记时应该先读哪些规则、遵守哪些边界。
3. 规则、检查报告、迁移记录如何长期维护。

这个项目适合把 Obsidian 当作长期知识库、项目驾驶舱和输出工作台的人使用。你可以直接复制 `templates/vault-root/` 到自己的 vault 根目录，也可以只复制其中的 `99_Vault_Management_Rules/` 和 AI 入口文件。

## 设计目标

- 低摩擦收集：临时想法、网页剪藏、AI 对话和外部资料先进入 Inbox。
- 渐进式整理：只有经过理解、提炼、复用的内容才进入 Wiki。
- 项目和知识分离：项目目录负责推进，Wiki 负责沉淀，Outputs 负责交付。
- 安全优先：删除、批量移动、中文编码、图片本地化都有明确规则。
- AI 可执行：给 Codex、Claude Code、通用 agent 准备短入口文件和详细规则文件。
- 可审计：AI 的整理、迁移、检查和规则更新都写成单次操作记录。

## 推荐目录

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
```

这不是 PARA、Zettelkasten 或 LYT 的复刻，而是一套偏实用的混合工作流：先收集，再理解，再推进项目，最后形成输出。

## 快速开始

1. 备份你的 Obsidian vault。
2. 将 `templates/vault-root/` 中的内容复制到 vault 根目录。
3. 按需保留 `.codex/AGENTS.md`、`.claude/CLAUDE.md`、`.agents/AGENTS.md` 或根目录 `AGENTS.md`。
4. 让 AI 在整理 vault 前先读取：

```text
99_Vault_Management_Rules/00-README.md
99_Vault_Management_Rules/01-Vault-Structure.md
99_Vault_Management_Rules/99-Safety-Rules.md
```

5. 根据任务类型继续读取对应规则文件。

详细步骤见 `docs/quick-start.md`。

## 适配哪些 AI 助手

模板默认包含这些入口文件：

```text
AGENTS.md
.codex/AGENTS.md
.claude/CLAUDE.md
.agents/AGENTS.md
```

它们只负责路由，不承载详细规则。详细规则集中在：

```text
99_Vault_Management_Rules/
```

这样做的好处是：不同 AI 工具读到的入口一致，规则更新也不会散落在多个系统文件里。

## 规则文件

```text
00-README.md                总览、阅读顺序和优先级
01-Vault-Structure.md       顶层目录职责和判断标准
02-Inbox-Rules.md           收集区、临时想法、剪藏和原始材料规则
03-Wiki-Rules.md            长期知识页、命名、结构和维护规则
04-Project-Rules.md         项目目录、项目首页、进展和决策规则
05-Output-Rules.md          输出文档、草稿、定稿和来源追溯规则
06-Archive-Rules.md         归档和冷存储规则
07-Rule-Update-Rules.md     如何修改规则本身
08-AI-Review-Rules.md       定期检查标题、位置、链接和重复内容
09-Operation-Log-Rules.md   AI 操作记录的写法和保存位置
99-Safety-Rules.md          删除、批量移动、编码、图片和链接安全规则
```

## 社区约定

- 规则文本使用中文，路径和文件名尽量使用稳定、可迁移的英文。
- 不提交个人隐私、真实 vault 路径、账号信息、未公开研究资料或私有笔记。
- 新规则应短、明确、可执行，并说明适用范围。
- 大规模迁移、删除、重命名前，AI 必须先列清单并等待人工确认。

## 许可证

本项目使用 MIT License。你可以自由复制、修改、分发和商用，但请自行承担用于真实知识库时的备份和数据安全责任。