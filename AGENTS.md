# AGENTS.md

This repository packages reusable workflows for reviewing Tianjin University undergraduate theses.

## When working on a thesis repository

- Read `PROJECT.md` first when it exists. Treat it as the source of stable project facts.
- Read `MEMORY.md` when it exists for advisor preferences, known issues, and current review focus.
- Prioritize submission-blocking issues before style polishing.
- Prefer minimal necessary edits. Do not casually alter the thesis conclusion, data scope, or chapter logic.

## Review priorities

1. Front matter order, page numbering, headers/footers, and table of contents.
2. Abstracts and keywords, including Chinese/English consistency.
3. Figures, tables, equations, appendix numbering, and caption placement.
4. Citation consistency between in-text references and bibliography entries.
5. Writing tone: remove local paths, internal file names, and defense-note style phrasing.

## Hard checks

- Figure captions go below figures; table captions go above tables.
- Figures, tables, and equations should use chapter-based numbering.
- Tables should prefer three-line formatting.
- Chinese and English abstracts should stay aligned.
- Output review results with findings first, then touched files, residual risks, and compile status.

## Reusable skill

For detailed thesis review workflow, read `.codex/skills/tju-thesis-reviewer/SKILL.md`.
