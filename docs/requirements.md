# Requirements

这份文档说明使用 `TJU Thesis Review Kit` 时建议具备的工具、环境和仓库接入条件。

## 1. 基本使用要求

- 你有一个论文仓库，或准备创建一个论文仓库。
- 论文内容最好已经按目录分开，例如 `main.tex`、`include/`、`references/`、`appendix/`。
- 建议在仓库根提供 `PROJECT.md`，让 AI 能读到稳定事实信息。
- 如需长期协作式 review，建议再提供 `MEMORY.md`。

## 2. 不同工具的接入要求

| 工具 | 需要复制的文件 | 说明 |
|------|----------------|------|
| `Cursor` | `.cursor/` | 提供规则和技能，适合在 Cursor IDE 内长期使用 |
| `Codex` | `AGENTS.md` + `.codex/` | 提供项目级指令入口和可复用 skill |
| `Claude Code` | `CLAUDE.md` + `.claude/` | 提供项目级约束与 thesis review skill |

如果你同时使用多种工具，可以把这三套入口一起放进仓库。

## 3. LaTeX starter 模板要求

若你使用 `latex-template/`：

- 建议使用 `LuaLaTeX`
- 推荐编译链：

```bash
lualatex main.tex
bibtex main
lualatex main.tex
lualatex main.tex
```

- 需要本地具备基本 TeX 发行版，例如 TeX Live 或 MacTeX
- 若学院另有模板细则，请以最新正式要求为准

## 4. GitHub 相关

如果你想像本仓库一样发布到 GitHub，建议本机具备：

- `git`
- `gh`（GitHub CLI，可选但推荐）
- 已配置可用的 GitHub 登录状态

## 5. 使用边界

- 本仓库不能替代学院最终审查、导师意见、查重系统和 AIGC 检测系统。
- 不同学院、不同年份的格式细节可能不同，使用前请自行核对最新正式要求。
- 对于基于既有模板整理而来的内容，请同时阅读仓库根的 `THIRD_PARTY.md`。
