# 原文精读教学协议

当用户要求“讲毛选”“掰开揉碎”“逐段讲原文”“从第一卷开始学”时，按本协议执行。

## 资料优先级

1. 优先读取本地资料库：
   - `knowledge/mao-source-library/qstheory-index.json`
   - `knowledge/mao-source-library/qstheory-pages/*.txt`
   - `knowledge/mao-source-library/qstheory-volumes/*.md`
2. 需要补充背景时，再读：
   - `knowledge/mao-source-library/mzdbl-text-index.json`
   - `knowledge/mao-source-library/mzdbl-texts/*.txt`
3. 不要只凭记忆讲解。先定位原文，再解释。

## 讲解格式

每次讲一篇或一个自然段群，不要一次吞太多。

固定结构：

1. 这段在回答什么问题。
2. 历史现场是什么。
3. 原文关键句。
4. 白话翻译。
5. 论证链条。
6. 关键概念。
7. 容易误读的地方。
8. 方法论抽象。
9. 今日类比和练习。

## 拆解原则

- 先讲问题，再讲结论。
- 先讲现实矛盾，再讲理论概念。
- 把“口号感”的句子还原成具体判断。
- 遇到阶级、群众、统一战线、矛盾、实践等概念，要解释它在该篇中的具体作用。
- 不做政治宣传式复述；聚焦文本、历史语境、方法论和思维训练。
- 对有争议或强烈时代色彩的表达，要说明其历史语境和适用边界。

## Obsidian 输出

用户要求生成学习计划或笔记时，写入：

- `C:\Users\Administrator\Documents\大姐姐skill\Obsidian-Mao-Study`

推荐结构：

- `000-毛选学习总览.md`
- `Volume-01/00-volume-01-index.md`
- `Volume-01/NN-topic.md`
- `templates/original-text-breakdown-template.md`

每篇笔记必须能单独阅读，并尽量链接到上一课、下一课和本地原文路径。


## 进度同步规则

当用户报告“看完了”“读完了”“完成第 N 课”等学习进度时：

1. 更新 Obsidian 学习路线，把对应课次标记为已完成，并指出下一课。
2. 同步更新以下镜像目录中的学习路线和相关笔记：
   - `C:\Users\Administrator\Documents\Obsidian Vault\毛选学习`
   - `C:\Users\Administrator\Documents\大姐姐skill\毛选学习`
   - `C:\Users\Administrator\.codex\skills\mao\knowledge\毛选学习`
   - `C:\Users\Administrator\.agents\skills\mao\knowledge\毛选学习`
3. 同步更新学编程项目里的评分系统：`C:\Users\Administrator\Documents\学编程\评分系统`。优先更新 `reading_projects.json` 中的“毛选”项目，再刷新/更新 `score_data.json` 快照；字段至少包括已读课次、总课次、当前下一课、进度说明和分数。毛选第一卷必须按 `lesson_scores` 的每课重要性加权计分，不要平均分。
4. 若评分系统路径不存在，不要声称已同步；必须告诉用户暂未定位到路径，并请用户补充具体位置。


## 第一卷默认路线

1. 中国社会各阶级的分析。
2. 湖南农民运动考察报告。
3. 井冈山的斗争。
4. 关于纠正党内的错误思想。
5. 星星之火，可以燎原。
6. 反对本本主义。
7. 必须注意经济工作。
8. 怎样分析农村阶级。
9. 我们的经济政策。
10. 关心群众生活，注意工作方法。
11. 论反对日本帝国主义的策略。
12. 中国革命战争的战略问题。
13. 实践论。
14. 矛盾论。

如果源文本把一篇拆成多页，先在讲解中合并为一个主题，再按段落推进。

