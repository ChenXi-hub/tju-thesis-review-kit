---
name: tju-thesis-reviewer
description: Review Tianjin University undergraduate thesis tex/doc/docx/pdf projects for format compliance, figure and table conventions, citation consistency, and submission-ready academic tone. Use when reviewing, revising, or polishing a TJU thesis before submission or defense.
---

# TJU Thesis Reviewer

Use this skill when the user is working on a Tianjin University undergraduate thesis and asks for review, revision, cleanup, or pre-submission checks.

## First step

- Read `PROJECT.md` if it exists.
- Read `MEMORY.md` if it exists.
- Infer the thesis entry files, abstract files, bibliography files, and appendix files before editing.

## Priorities

1. Fix submission-blocking format or citation problems first.
2. Keep changes minimal and do not casually alter conclusions, data scope, or chapter structure.
3. Keep figures, tables, equations, and citations aligned with the surrounding thesis narrative.
4. Remove process traces that are not appropriate for submission, but preserve necessary traceability.

## Workflow

1. Check front matter order, page-number transitions, headers/footers, and contents.
2. Check title hierarchy, paragraph formatting, abstracts, and keyword consistency (Chinese/English alignment).
3. Check figures, tables, equations, appendix numbering, caption placement, float spacing (about half a line to one line from body text), three-line tables, and non-split floats when possible.
4. Check bibliography style (e.g. GB/T 7714-2015), in-text citation placement (no “references-only-at-end” gaps), superscript vs inline citation grammar, and citation tags for baselines/methods named inside tables.
5. Check writing tone: remove local paths, internal PDF names, defense-note phrasing, and colloquialisms; prefer “本文实现了” over “本文提出了” unless the contribution is clearly novel.
6. Compile when possible and report warnings plus residual risk.

## Hard checks (TJU undergraduate thesis norms)

### Body and layout

- A4 single-sided; margins and header/footer positions follow the official template.
- Chinese body: Songti; Latin digits: Times New Roman; usual size xiaosi; fixed 20 pt line spacing; first-line indent 2 characters.
- Title hierarchy matches the template (fonts, sizes, spacing).
- Body paragraphs justified by default; each chapter starts on a new page.
- Avoid large blank gaps; if a float does not fit, move text or adjust float placement instead of leaving empty vertical space.
- Do not paste long source code into the main text; use prose or pseudocode (details may go to an appendix).

### Front matter and page numbers

- Order: cover, title page, originality statement, Chinese/English abstract and keywords, contents, main text, references, appendices, acknowledgements (adjust if your college specifies otherwise).
- Roman numerals for front matter; Arabic page numbers restart at 1 for the main text.
- Header text matches the template (e.g. “天津大学 20XX 届本科生毕业设计（论文）”).

### Figures, tables, and equations

- Figure captions below figures; table captions above tables; centered.
- Per-chapter numbering for figures/tables/equations (e.g. Figure 2-3, Table 4-1, (5-2)).
- Prefer three-line tables (`booktabs`); avoid dense vertical rules.
- In Chinese theses, prefer Chinese labels in figures/tables; avoid English-only screenshot artifacts.
- Do not crop figures/tables/equations from other papers or references; redraw/rebuild and cite sources.
- Floats should not split across pages when avoidable; figure/table text uses Times New Roman for Latin text.
- After equations, explanatory paragraphs starting with “其中” should be flush left (no hanging indent).
- Variables: italic lowercase by default; matrices: upright bold capitals by default.

### References

- One-to-one mapping between every in-text citation and a bibliography entry.
- Uniform punctuation and fields across the reference list.
- Citations are superscripts by default; use normal inline form only when the citation number is a grammatical part of the sentence (e.g. “文献 [5] 指出…”).

## Output

Present results in this order:

1. Findings ordered by severity
2. Files changed or recommended to change
3. Completed vs pending items (map to advisor checklist when provided)
4. Residual risks
5. Compile result
6. Suggested sections or pages to re-check

## References

- Detailed checklist (Chinese): `references/review-checklist.md`
- Example prompts and outputs: `references/examples.md`
- Advisor format/content checklist (Chinese, line-by-line): `references/supervisor-requirements.md`
