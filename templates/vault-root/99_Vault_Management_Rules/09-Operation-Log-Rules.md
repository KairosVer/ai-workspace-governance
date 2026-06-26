# AI 操作记录规则

本文件规定 AI 整理、迁移、检查、规则更新时如何记录操作。

## 基本原则

- 每次操作新建一篇记录。
- 不把所有记录写进同一个总日志。
- 不反复修改旧记录，除非需要修正事实错误、编码问题或安全问题。
- 操作记录使用普通相对路径，不使用 Obsidian 双链。
- 操作记录应能让未来的人理解：为什么做、做了什么、影响了什么、还剩什么。

## 保存位置

```text
99_Vault_Management_Rules/AI_Operations_Log/
  README.md
  rule-updates/
  reviews/
  migrations/
  maintenance/
  legacy/
```

目录职责：

- `rule-updates/`：规则新增、修改、拆分、合并、废弃。
- `reviews/`：标题、位置、链接、重复内容、孤岛页面等检查报告。
- `migrations/`：文件移动、目录重组、批量重命名。
- `maintenance/`：小规模维护，如创建索引、补模板、修链接。
- `legacy/`：旧日志或旧格式记录。

## 文件命名

推荐格式：

```text
YYYY-MM-DD-HHMM-operation-topic.md
```

示例：

```text
2026-06-26-1430-update-inbox-rules.md
2026-06-26-1500-review-file-locations.md
2026-06-26-1530-migrate-project-folders.md
```

文件名使用英文或拼音，正文可以使用中文。

## 记录模板

```md
# 操作记录：简短标题

## 时间

YYYY-MM-DD HH:mm

## 操作类型

规则更新 / 检查 / 迁移 / 维护 / 其他

## 背景

为什么需要这次操作。

## 读取的规则

- 99_Vault_Management_Rules/00-README.md
- 99_Vault_Management_Rules/01-Vault-Structure.md
- 99_Vault_Management_Rules/99-Safety-Rules.md

## 操作内容

列出实际做了什么。

## 涉及路径

| 路径 | 动作 | 说明 |
| --- | --- | --- |

## 风险与确认

是否涉及删除、批量移动、覆盖、编码、隐私。

## 结果

完成了什么，哪些没有做。

## 后续建议

未来需要继续处理的事项。
```

## 什么时候必须记录

以下情况必须记录：

- 修改规则文件。
- 移动或重命名文件。
- 创建或删除目录。
- 批量修复链接或附件。
- 定期 AI 检查。
- 大规模格式整理。
- 用户要求可追溯的操作。

以下情况可以不记录：

- 只回答问题，没有改文件。
- 只读取文件，没有改变 vault。
- 单个文件中的轻微错别字修复，且用户没有要求记录。

## 隐私要求

操作记录不应包含：

- 账号、密钥、token。
- 真实个人身份信息。
- 未公开研究或商业敏感细节。
- 不必要的本机绝对路径。

如果必须提到路径，使用相对 vault 根目录的路径。