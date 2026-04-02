# LaTeX Template

这是一个适合开源分享的天津大学本科毕设 LaTeX starter 模板，基于你当前模板结构做了清洗和最小化处理。

## 已做的处理

- 删除了个人课题、姓名、学号、导师、私有仓库地址和实验材料路径。
- 删除了依赖本地资源的封面图片与额外字体文件，避免别人拿到后直接编译失败。
- 保留了 `main.tex`、`include/`、`appendix/`、`setup/`、`references/` 的常见结构。
- 保留了参考文献样式文件 `references/ref.bst`，以便继续按学校样式生成文献表。

## 建议编译方式

```bash
lualatex main.tex
bibtex main
lualatex main.tex
lualatex main.tex
```

## 使用步骤

1. 先修改 `include/cover.tex` 中的题目、学院、专业、姓名、学号和导师信息。
2. 再修改 `include/abstract.tex`，保持中英文摘要与关键词同步。
3. 按章节填充 `include/body.tex`。
4. 在 `references/ref.bib` 中替换为你自己的参考文献条目。
5. 根据需要补充 `appendix/appendix.tex` 与 `appendix/acknowledgements.tex`。

## 注意

- 这是一个 starter 模板，不保证与你学院每一条最新细则完全一致。
- 若学院另发封面样式、签字页、页眉文本或摘要格式要求，请以最新正式通知为准。
- 若你要公开发布，建议在仓库说明中明确“模板来源”和“需自行核对学院最新要求”。
