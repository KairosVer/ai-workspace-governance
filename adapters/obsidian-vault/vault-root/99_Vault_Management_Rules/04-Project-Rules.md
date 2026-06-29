# Projects 规则

`5-Projects` 是项目驾驶舱，服务正在推进的课题、任务和长期目标。

## 目录职责

项目目录负责回答：这个项目是什么、推进到哪里、下一步做什么、关键资料在哪里、相关实验/知识/输出链接到哪里。

## 项目创建标准

有明确目标和阶段、持续超过一周、涉及多个文件/实验/资料/输出、需要定期回顾进展，即可创建项目。

## 子文件夹建议

```text
5-Projects/
  00-Guide/
  01-Active/
  02-Paused/
  03-Completed/
  04-Experiments/
```

如果项目数量少，也可以先不建状态文件夹，直接按项目名建目录。

## 项目目录模板

```text
5-Projects/项目名/
  index.md
  progress.md
  tasks.md
  notes.md
```

小项目可以只保留 `index.md`。

## 项目首页模板

```md
---
type: project
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
---

# 项目名

## 目标
## 当前状态
## 下一步
- [ ] 
## 关键链接
### 原始资料
### 知识页
### 实验记录
### 输出
## 决策记录
## 风险与问题
```

## 与 Experiments 的关系

`04-Experiments/` 独立存放实验记录。项目通过首页"实验记录"链接关联，不强制把实验记录移入项目子目录。

原因：实验记录可能被多个项目引用，独立存放更灵活。如果某个实验明确只服务单一项目，可以在项目目录下建 `experiments/` 子目录存放。

## 与 Wiki/Outputs 的区别

`5-Projects` 关注推进；`4-Wiki` 关注复用；`6-Outputs` 关注交付。

项目完成后，应把可复用经验提炼到 `4-Wiki`，最终成果链接到 `6-Outputs`。