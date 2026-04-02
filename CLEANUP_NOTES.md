# Cleanup Notes

这份说明用于解释原始 `.cursor` 资产是如何被抽象成开源套件的。

## 已保留为通用能力

- `tju-thesis-figures.mdc`
  - 其中与学校格式、图表、公式、页码、摘要相关的通用规范，已经吸收到：
  - `.cursor/skills/tju-thesis-reviewer/SKILL.md`
  - `.cursor/skills/tju-thesis-reviewer/review-checklist.md`
  - `.cursor/rules/tju-thesis-review-core.mdc`

- `thesis-writing-voice.mdc`
  - 其中与学术语体、去内部材料痕迹、避免答辩备忘口吻相关的内容，已经保留并压缩为：
  - `.cursor/rules/tju-thesis-writing-voice.mdc`

## 已从“硬规则”改为“模板”

- `thesis-mission.mdc`
  - 原文件同时包含“学校通用要求”和“当前课题私有事实”。
  - 开源后不适合继续作为 alwaysApply 规则，因此拆分为：
  - 通用部分进入 Skill 与核心 Rule。
  - 课题特定部分改为 `templates/PROJECT.md`，由每个使用者自己填写。

- `thesis-roadmap.mdc`
  - 原文件更像你个人的收尾路线图与动态待办。
  - 这类内容不适合变成别人仓库里的硬规则，因此改造成：
  - `templates/MEMORY.md`

## 不建议原样开源的内容

- `fuxiu-conda-plots.mdc`
  - 绑定了个人 conda 环境名和本机路径。
  - 若开源，建议由具体仓库自己写环境说明，而不是放入学校通用 review 套件。

- `deai-finance-prompt.md`
  - 明显偏财务管理专业写作风格，不适合作为“全校通用”默认资产。
  - 如果以后你想扩展，可以单独做 `finance-thesis-writing` 之类的学科扩展包。

## 当前这套开源包的定位

- 主体是一个“天津大学本科毕设通用 review 套件”。
- 它优先解决格式、图表、引用、摘要和语体问题。
- 课题事实、导师偏好、阶段性问题不写死在规则里，而是交给 `PROJECT.md` 和 `MEMORY.md` 承载。

## 新增的 LaTeX starter 模板处理

- 已新增 `latex-template/` 目录，保留 `main.tex`、`include/`、`appendix/`、`setup/`、`references/` 的基本结构。
- 已把你的个人课题内容替换为通用占位文本，避免公开后暴露具体研究内容。
- 已去掉依赖本地资源的封面图片和额外字体文件，避免第三方拿到仓库后因缺少 `figures/tjuname`、`figures/tjulogo`、`fonts/SimHei.ttf` 而直接编译失败。
- 已保留 `references/ref.bst`，以便继续沿用学校参考文献样式。
