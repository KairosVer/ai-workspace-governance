# Outputs 规则

`6-Outputs` 保存可交付成果和正式产物。

## 目录职责

适合放入：论文草稿和定稿、报告、PPT 文本、项目申请书、专利/软著材料、正式信件、面向他人的教程和总结。

不适合放入：原始资料、未整理剪藏、项目待办、实验流水账、纯个人日记。

## 子文件夹建议

```text
6-Outputs/
  00-Guide/
  01-Papers/
  02-Reports/
  03-Slides/
  04-Proposals/
  05-Patents/
  06-Letters/
  07-Specs/
```

按实际需要逐步创建，不必一次建满；空子目录不预建，有内容时再建。

## 输出页面结构

```md
---
type: output
status: draft
project: [[5-Projects/项目名/index]]
created: YYYY-MM-DD
updated: YYYY-MM-DD
---

# 标题

## 用途
## 正文
## 来源与依据
## 待修改
```

## 来源要求

正式输出中的事实、数据、实验结论应能追溯到 `3-Inbox`、`4-Wiki`、`5-Projects` 或对应实验记录。

## 草稿与定稿

草稿标 `status: draft`，定稿标 `status: final`。过时但需要保留的输出，移入 `7-Archive`，不要直接删除。