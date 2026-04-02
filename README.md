# TJU Thesis Review Kit

为天津大学本科毕业设计（论文）准备的一套更实用的开源辅助工具：把零散的毕设经验整理成可复用的 Cursor、Codex、Claude Code 规则与技能、Prompt 和 `LaTeX` starter，帮助同学们更高效地完成论文自查、格式整改和送审前 review。

An open-source toolkit for Tianjin University undergraduate theses, including reusable Cursor, Codex, and Claude Code workflows, prompts, and a LaTeX starter template for review, revision, and pre-submission checks.

适合“已经在写论文，但总觉得格式、图表、摘要、参考文献容易出问题”的场景，也适合想把 AI 从“零散问答”升级成“长期协作助手”的同学。

This repository is designed for students who want more than one-off AI answers and prefer a reusable workflow for thesis writing and review.

## What Is Included

- Cursor `Skill` 与 `Rule`
- Codex 项目级 `AGENTS.md` 与 `.codex/skills/`
- Claude Code 项目级 `CLAUDE.md` 与 `.claude/skills/`
- 可直接起步的 `LaTeX` starter 模板
- `PROJECT.md` / `MEMORY.md` 模板
- 可直接复制使用的提问模板、送审前总检 prompt、导师汇报版输出模板

## 适合谁用

- 正在写天津大学本科毕业设计（论文）的同学
- 想用 Cursor / AI 辅助做格式审查、图表核对、摘要润色、参考文献核对的人
- 想把论文仓库整理成“可持续 review”结构的人

## 能解决什么问题

- 按天津大学本科毕业设计（论文）规范做全文 review
- 检查前置页、页码、页眉页脚、标题层级、摘要和关键词
- 检查图、表、公式、附录编号、题注位置和三线表
- 检查参考文献与文内引用的一致性
- 清理不适合送审的表达，比如内部文件名、本地路径、答辩备忘口吻

## 仓库结构

```text
tju-thesis-review-kit/
├── AGENTS.md
├── CLAUDE.md
├── .cursor/
│   ├── rules/
│   └── skills/
├── .codex/
│   └── skills/
├── .claude/
│   └── skills/
├── docs/
│   ├── requirements.md
│   ├── cleanup-notes.md
│   ├── open-source-checklist.md
│   └── release/
│       ├── github-copy.md
│       ├── github-release-draft.md
│       └── social-posts.md
├── latex-template/
├── prompts/
├── templates/
├── README.md
├── LICENSE
├── THIRD_PARTY.md
├── CONTRIBUTING.md
```

## 快速开始

### 1. 复制 AI review 能力

按你使用的工具复制对应文件：

- Cursor：复制 `.cursor/`
- Codex：复制 `AGENTS.md` 和 `.codex/`
- Claude Code：复制 `CLAUDE.md` 和 `.claude/`

### 2. 建立项目事实文件

把 `templates/PROJECT.md` 复制到你的论文仓库根目录，并填写论文题目、LaTeX 根目录、主数据源、文献边界和特殊约束。

如果你希望 AI 记住导师偏好、当前问题和本轮整改重点，再把 `templates/MEMORY.md` 复制到仓库根目录。

### 3. 使用 LaTeX starter 模板

如果你还没有论文骨架，可以直接从 `latex-template/` 开始。模板已做去私有化处理，不依赖你本机额外字体和封面图片。

### 4. 检查 Requirements

在真正接入前，建议先看 `docs/requirements.md`，里面写清了：

- 不同工具对应需要哪些文件
- 使用本仓库建议具备哪些工具或环境
- `LaTeX` starter 的推荐编译方式

### 5. 直接开始问

推荐先从这些问法开始：

- “请按天津大学本科毕业论文规范 review 我的 LaTeX 仓库。”
- “请重点检查图表、摘要和参考文献是否符合送审要求。”
- “请做送审前最后一轮总检，输出问题清单和剩余风险。”

更多可直接复制的问法见 `prompts/recommended-prompts.md`。

## Multi-Agent Support

本仓库现在同时提供三套平行入口，方便不同 AI 编码工具复用同一套论文 review 思路：

- `Cursor`：`.cursor/rules/` + `.cursor/skills/`
- `Codex`：`AGENTS.md` + `.codex/skills/`
- `Claude Code`：`CLAUDE.md` + `.claude/skills/`

### 接入方式对照表

| 工具 | 需要复制的文件 | 主要作用 | 适合谁 |
|------|----------------|----------|--------|
| `Cursor` | `.cursor/` | 提供规则、技能和 IDE 内常驻审稿能力 | 已经在 Cursor 里写论文的人 |
| `Codex` | `AGENTS.md` + `.codex/` | 提供项目级指令入口和可复用 skill | 想在 Codex 中复用同一套 review 工作流的人 |
| `Claude Code` | `CLAUDE.md` + `.claude/` | 提供项目级约束和 thesis review skill | 想在 Claude Code 中保持统一审稿流程的人 |

如果你同时使用多种工具，可以把三套入口一起放进论文仓库，让不同代理共享同一套论文上下文结构，再配合 `PROJECT.md` / `MEMORY.md` 使用。

## Requirements

使用前建议至少确认：

- 你已有论文仓库，或准备新建一个论文仓库
- 你知道自己要接入的是 `Cursor`、`Codex`、`Claude Code` 中的哪一种或哪几种
- 若使用 `latex-template/`，本地最好具备可用的 TeX 发行版，并按 `LuaLaTeX + BibTeX` 链路编译

完整要求见 `docs/requirements.md`。

## 开箱即用资源

- `prompts/recommended-prompts.md`
  - 常用提问模板，适合日常 review、图表整改、参考文献核对、摘要检查
- `prompts/pre-submission-review-prompt.md`
  - 送审前总检 prompt，可直接复制到 Cursor
- `prompts/advisor-report-template.md`
  - 导师汇报版输出模板，适合整理“已改什么、还差什么、风险在哪”
- `latex-template/README.md`
  - LaTeX starter 模板说明
- `docs/release/social-posts.md`
  - 朋友圈 / 小红书 / 即刻 / X / GitHub 动态可直接复制的发布文案
- `docs/requirements.md`
  - 使用本仓库前建议具备的工具、环境和接入要求

## 清洗说明

- 删除了个人课题名称、个人文件路径、私有仓库链接和本机环境命名
- 去掉了只适用于单一课题的章节号、数据集、实验材料和项目细节
- 把动态经验拆成通用 `Skill`、常驻 `Rule` 和仓库级模板
- 对 LaTeX 模板做了去私有化处理，使其更适合公开分发

更详细的映射说明见 `docs/cleanup-notes.md`。

## 发布到 GitHub 前

建议至少确认：

- `docs/open-source-checklist.md`
- `THIRD_PARTY.md`
- `docs/release/github-copy.md`
- `docs/release/github-release-draft.md`

这样你不仅能发代码，也能直接发简介、release 文案和使用说明。

## 注意

- 本仓库不能替代学院最终审查、导师意见、查重系统和 AIGC 检测系统
- 天津大学不同学院、不同年份可能存在细节差异，使用前请以最新正式要求为准
- 若你在此基础上扩展专业专属写法，建议单独增加学科规则，而不是把通用规则写死

## License

本仓库默认使用 `MIT` 许可证发布你在本仓库中的整理与新增内容。对于从既有模板衍生或整理而来的部分，请同时阅读 `THIRD_PARTY.md`。
