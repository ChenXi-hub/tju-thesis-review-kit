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
2. Check title hierarchy, paragraph formatting, abstracts, and keyword consistency.
3. Check figures, tables, equations, appendix numbering, caption placement, and three-line tables.
4. Check bibliography style and one-to-one mapping between in-text citations and references.
5. Check writing tone and remove local paths, internal PDF names, and defense-note phrasing.
6. Compile when possible and report warnings plus residual risk.

## Output

Present results in this order:

1. Findings ordered by severity
2. Files changed or recommended to change
3. Completed vs pending items
4. Residual risks
5. Compile result
6. Suggested sections or pages to re-check

## References

- For detailed checklist, read `references/review-checklist.md`.
- For example requests and outputs, read `references/examples.md`.
