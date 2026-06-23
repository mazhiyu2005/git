# Codex Skills

这个仓库存放我本地维护的 Codex skills。每个 skill 都放在 `skills/<skill-name>/` 下面，可以按需复制到 Codex 的 skills 目录中使用。

## Skill 简介

| Skill | 简介 | 适合场景 |
| --- | --- | --- |
| [`ai-microdrama`](skills/ai-microdrama/SKILL.md) | AI 短剧/漫剧制作工作流，把故事想法拆成项目设定、分集分幕、分镜、图片提示词、视频提示词和制作清单。 | AI 短剧、AI 漫剧、Seedance/即梦/可灵/灵矢提示词、角色与场景一致性。 |
| [`cobra-cosmology`](skills/cobra-cosmology/SKILL.md) | Cobra/C 资料宇宙论档案导航，把资料体系按宇宙论、冲突历史、事件、灵魂关系、女神/蔷薇等层级组织回答。 | 查询 Cobra 资料、整理概念图谱、对比 PDF 档案、构建阅读路线。 |
| [`hatch-pet`](skills/hatch-pet/SKILL.md) | 从角色设定、品牌线索或参考图生成 Codex 兼容动画宠物，并完成 spritesheet、pet.json、校验和视觉 QA。 | 做 Codex 小宠物、品牌吉祥物、透明背景动画图集。 |
| [`huashu-nuwa`](skills/huashu-nuwa/SKILL.md) | “女娲造人”工作流：从人物、主题或模糊需求出发，调研并蒸馏成可运行的人物/思维方式 Skill。 | 创建人物视角、认知顾问、方法论框架，或更新已有 persona skill。 |
| [`make-money`](skills/make-money/SKILL.md) | 帮用户选择合法、低成本、可验证、可自动化的赚钱项目，并产出报价、销售素材、实验指标和执行计划。 | 副业选择、产品变现、服务包装、获客话术和 7 天验证。 |
| [`mao`](skills/mao/SKILL.md) | 毛泽东方法论 AI 助手，包含六层认知架构、矛盾分析、实践论、调查研究、群众路线和毛选原文精读。 | 用毛选方法分析问题、学习原文、构建 Obsidian 学习路线、查询概念库。 |
| [`video-course-teacher`](skills/video-course-teacher/SKILL.md) | 把视频课、B 站课程、课程目录或本地课件拆成 Obsidian 学习路线，并按课时上课、布置作业、批改和更新进度。 | 学编程课、跟黑马 Python 课程、把收藏的视频课变成每日学习系统。 |
| [`wang-yangming-perspective`](skills/wang-yangming-perspective/SKILL.md) | 王阳明心学视角，把问题收束到此心此念，再用知行合一、致良知、事上磨练处理决策和行动。 | 修身、拖延、人际冲突、道德困境、人生选择和行动卡点。 |
| [`write-novel`](skills/write-novel/SKILL.md) | 小说共创、续写、改稿和长篇项目管理工作流，维护人物、时间线、伏笔和章节推进。 | 中文小说、网文、短篇、章节续写、故事 bible、节奏和文风修改。 |

## 结构

```text
skills/
├── ai-microdrama/
├── cobra-cosmology/
├── hatch-pet/
├── huashu-nuwa/
├── make-money/
├── mao/
├── video-course-teacher/
├── wang-yangming-perspective/
└── write-novel/
```

常见文件：

- `SKILL.md`：skill 的核心说明和触发描述。
- `agents/openai.yaml`：Codex 界面展示名称、短简介和默认提示词。
- `scripts/`：skill 需要的确定性脚本。
- `references/`：按需读取的参考资料。
- `assets/`：用于生成或输出的素材。

## 大文件说明

`ai-microdrama` 本地有一个 `assets/source-materials/` 原始素材库，体积约 5GB，且含多个超过 GitHub 普通仓库限制的文件。这个目录没有上传到仓库；仓库中保留了可用的 `references/` 索引和说明文件。

## 使用说明

这些 skill 是个人工作流沉淀，默认面向 Codex 使用。部分 skill 会读写本机路径，例如 Obsidian vault、pet 输出目录、本地 PDF 或课程资料目录；在其他机器使用时，需要根据自己的环境调整路径。
