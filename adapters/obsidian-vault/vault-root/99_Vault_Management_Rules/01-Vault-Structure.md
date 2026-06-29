# Vault 结构规则

本 vault 用于个人知识管理和科研工作流管理，包含日记、外部资料、知识沉淀、项目推进、成果输出和归档。

## 顶层目录

```text
0-Template
1-Attachment
2-Diary
3-Inbox
4-Wiki
5-Projects
6-Outputs
7-Archive
8-Atlas
99_Vault_Management_Rules
Z-WeRead
Z-Zotero
```

## 0-Template

模板目录。存放日记、实验记录、读书笔记、总结等通用模板。

## 1-Attachment

附件目录。存放图片、截图、图表、文档附件等资源。外部图片下载后放入此目录，正文使用 `![[filename]]`。

## 2-Diary

个人日记和周期回顾目录。保持个人表达原貌，只做错别字、格式和链接修正。

```text
2-Diary/
  YYYY-MM-DD.md
  Weekly/
  Monthly/
  Yearly/
```

日记按日期命名放根目录，周记、月度总结、年度总结分别进对应子目录。

## 3-Inbox

原始材料层。放未消化、未判断、未提炼的内容。

## 4-Wiki

长期知识库。放经过理解、提炼、可复用的知识页面。

## 5-Projects

项目驾驶舱。放正在推进的课题、任务和项目总览。

## 6-Outputs

成果输出层。放论文、报告、PPT、申请材料、专利、正式文档等可交付成果。

## 7-Archive

归档层。放暂时不用、已完成、已废弃但不该删除的内容。

## 8-Atlas

地图和索引层。只放导航页、主题地图、MOC、阅读路径和跨目录索引，不放正文知识。4-Wiki 存知识正文，8-Atlas 负责把相关页面组织成可浏览的地图。

## 99_Vault_Management_Rules

规则层。只放管理规则和 AI 操作记录，不放普通知识笔记。

## Z-WeRead / Z-Zotero

外部来源库。当前先不主动整理。需要整理时，先提出方案。

## AI 工具配置目录

`.agents/`、`.claude/`、`.claudian/`、`.codex/`、`skills-lock.json` 是 AI 工具的配置目录和锁定文件，不属于知识库内容。已加入 `.gitignore`，不纳入 git 版本管理。这些目录的维护由对应 AI 工具负责，不写入本规则层的操作记录。

## 判断标准

1. 是否是原始来源？是则进 `3-Inbox`。
2. 是否是长期可复用的理解？是则进 `4-Wiki`。
3. 是否服务某个正在推进的具体目标？是则进 `5-Projects`。
4. 是否是可交付成果？是则进 `6-Outputs`。
5. 是否不再活跃但不该删除？是则进 `7-Archive`。
6. 是否是跨目录导航、主题地图、项目地图或索引？是则进 `8-Atlas`。
## 目录说明页

一级内容目录中的入口说明文件统一放入各自的 `00-Guide/` 子目录，避免 `index.md` 或 `README.md` 孤立散放在目录根部。

```text
3-Inbox/00-Guide/Inbox说明.md
4-Wiki/00-Guide/Wiki说明.md
5-Projects/00-Guide/Projects说明.md
6-Outputs/00-Guide/Outputs说明.md
7-Archive/00-Guide/Archive说明.md
```

这些说明页只写目录用途、常用入口和少量维护原则，不维护完整文件清单。完整路线交给 `8-Atlas`。

## 空目录策略

规则中列出的子文件夹是建议骨架，不要求预先建满。空子目录不预建，有内容时再建；已建但长期为空的目录应及时删除，避免产生检查噪音。