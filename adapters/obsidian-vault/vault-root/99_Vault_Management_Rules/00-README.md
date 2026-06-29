# Vault 管理规则总览

本目录存放当前 Obsidian vault 的管理规则。这里不是普通知识区，而是管理全库结构、文件流转、安全边界和 AI 操作行为的规则层。

## 阅读顺序

整理文件、让 AI 处理笔记、迁移内容或创建目录前，优先阅读：

1. `01-Vault-Structure.md`：判断内容属于哪个目录。
2. `99-Safety-Rules.md`：涉及删除、批量移动、编码、图片下载时优先阅读。
3. `10-AI-Execution-Rules.md`：AI 会话开始、操作后自检、会话结束时必读。
4. `07-Rule-Update-Rules.md`：修改规则前阅读。
5. `08-AI-Review-Rules.md`：检查标题、位置、链接、重复和孤岛页面时阅读。
6. `09-Atlas-Rules.md`：创建、维护地图页和跨目录索引时阅读。
7. 根据目标目录读取对应规则。

## 规则优先级

1. 用户当前明确指令优先。
2. `99-Safety-Rules.md` 中的安全规则优先于所有效率和整理需求。
3. 根目录 `AGENTS.md`、`CLAUDE.md`、`.agents/AGENTS.md` 只作为入口路由，详细规则以本目录为准。
4. 目录职责冲突时，按文件实际用途判断，不按文件名机械判断。

## 核心原则

```text
3-Inbox   原始材料
4-Wiki    长期知识
5-Projects 项目推进
6-Outputs 成果输出
7-Archive 归档冷存储
8-Atlas  知识地图（规则见 09-Atlas-Rules.md）
```

## 工作流

```text
收集 -> 3-Inbox
理解 -> 4-Wiki
推进 -> 5-Projects
交付 -> 6-Outputs
冷存储 -> 7-Archive
导航 -> 8-Atlas
```

判断不清的文件，默认留在 `3-Inbox`，或在需要清理时移入 `7-Archive`，不要急着删除。

## 操作记录

AI 的整理、迁移、检查和规则更新，不写入单一总日志，而是在以下目录中新建单次操作记录：

```text
99_Vault_Management_Rules/AI_Operations_Log/
```

按操作类型放入对应子文件夹：

```text
rule-updates/  — 规则变更（新增、修改、拆分、废弃）
reviews/       — 定期检查报告（标题、位置、链接、重复、孤岛）
maintenance/   — vault 维护操作（批量整理、格式修复、标签补全等）
migrations/    — 文件迁移记录（跨目录移动、归档、重组等）
external/      — vault 外部文件操作（系统配置、工具安装、计划任务等）
```

根目录不放日志文件。