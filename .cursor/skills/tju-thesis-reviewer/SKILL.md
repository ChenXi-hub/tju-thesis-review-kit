---
name: tju-thesis-reviewer
description: Review Tianjin University undergraduate thesis tex/doc/docx/pdf files for format compliance, figure and table conventions, citation consistency, and academic writing tone. Use when the user asks to review, revise, or polish a TJU thesis before submission or defense.
---

# TJU Thesis Reviewer

## Use when

- 用户要求按天津大学本科毕业设计（论文）规范审稿。
- 用户要求检查终稿、送审稿、答辩前版本。
- 用户要求重点检查前置页、图表、摘要、参考文献、附录或语气。
- 用户正在处理 `.tex`、`.docx`、`.pdf` 等论文文件。

## First step

优先读取仓库根的 `PROJECT.md` 和 `MEMORY.md`。如果存在，以它们作为课题特定信息来源；如果不存在，先根据现有文件结构和用户描述推断，再补充询问缺失事实。

## Review priorities

1. 先处理会影响提交的格式和引用问题，再处理表达润色。
2. 最小必要改动，不随意改动论文结论、数据口径和章节逻辑。
3. 图、表、公式、引用必须与正文叙述一致。
4. 删除不适合送审的“过程痕迹”，但保留必要的可追溯性。

## Workflow

1. 确认论文入口文件、摘要文件、正文文件、参考文献文件和附录文件。
2. 检查前置页顺序、页码切换、页眉页脚和目录层级。
3. 检查正文格式：标题层级、段落、摘要与关键词、中英文对应。
4. 检查图表公式：位置、编号、题注、附注、字体、三线表、正文引用。
5. 检查参考文献：文内 `\cite{}` 或编号引用是否有对应条目，体例是否统一。
6. 检查语体：删除内部文件名、本地路径、答辩提示式表达。
7. 如可执行编译，则至少完成一次完整编译，并汇总 warning 与剩余风险。

## Hard checks

- 正文中文宋体，英文和数字 Times New Roman；正文常用小四、固定值 20 磅、首行缩进 2 字符。
- 前置部分与正文页码体系分离；正文页码从 1 重新开始。
- 图题在图下，表题在表上，居中；图表与正文前后通常留一行。
- 图、表、公式按章编号，如“图2-3”“表4-1”“(5-2)”。
- 表格优先三线表；宽表先考虑重排或拆分，而不是硬压缩。
- 摘要与关键词中英文对应；中文摘要通常保持在学校要求范围内。
- 参考文献体例全文统一，文中引用与文后条目一一对应。
- 附录编号与正文分离。

## Writing tone

- 禁止把本地路径、内部 PDF、脚本文件名写成正文论据。
- 禁止“答辩中应避免”“读者应注意”这类答辩备忘口吻。
- 优先使用客观、克制、可检验的学术表达。

## Output format

按下面结构输出，优先列问题，不要先写总结：

1. 问题清单（按严重程度）
2. 开始修改或建议修改的文件
3. 已完成项与未完成项
4. 剩余风险
5. 编译结果
6. 建议优先复核的位置

## Additional resources

- 详细核对项：`[review-checklist.md](review-checklist.md)`
- 示例问法与输出：`[examples.md](examples.md)`
