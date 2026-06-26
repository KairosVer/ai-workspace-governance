# Outputs 规则

`6-Outputs` 保存可交付成果和正式产物。

## 目录职责

适合放入：

- 论文草稿和定稿。
- 报告。
- PPT 或演讲稿文本。
- 项目申请书。
- 提案。
- 专利、软著或规范材料。
- 正式信件。
- 面向他人的教程和总结。
- 准备发布的文章。

不适合放入：

- 原始资料。
- 未整理剪藏。
- 项目待办。
- 日常流水记录。
- 纯个人日记。
- 尚未明确用途的一句话想法。

## 推荐子目录

```text
6-Outputs/
  index.md
  Papers/
  Reports/
  Slides/
  Proposals/
  Patents/
  Letters/
  Specs/
  Articles/
```

按实际需要逐步创建，不必一次建满。

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

## 读者

## 正文

## 来源与依据

## 待修改
```

## 状态

建议使用这些状态：

```text
draft       草稿
review      待检查或待反馈
final       定稿
published   已发布
archived    已归档
```

## 来源要求

正式输出中的事实、数据、实验结论、引用和关键判断应能追溯到：

- `3-Inbox` 的原始来源。
- `4-Wiki` 的长期知识页。
- `5-Projects` 的项目记录。
- 外部公开来源。

AI 不应编造来源。没有来源时，应标注“待补来源”或“需核查”。

## 草稿与定稿

- 草稿标 `status: draft`。
- 定稿标 `status: final`。
- 已发布内容标 `status: published`。
- 过时但需要保留的输出，移入 `7-Archive`，不要直接删除。

## AI 辅助边界

AI 可以：

- 重组结构。
- 润色表达。
- 检查逻辑。
- 生成摘要。
- 列出需要补充来源的位置。

AI 不应：

- 编造数据或引用。
- 擅自改变结论。
- 删除限制条件和不确定性。
- 将草稿误标为定稿。