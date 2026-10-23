# Reference layout and exam usefulness

## Measured design authority

The retained `assets/reference.docx` is a neutral redistribution copy of the approved Prepal design, with generic content slots rather than private course notes. Its SHA-256 is `18a238b6c559dd3a7ac14755791b124218006aa596f72aaeb63514a259f5a8b9`. Re-inspect if the retained reference ever changes; do not overwrite it to make a hash check pass.

| Component | Reference value |
| --- | --- |
| Paper | Letter, portrait, 12240 x 15840 twips (8.5 x 11 inches) |
| Pages | Two rendered pages, four columns per page |
| Margins | Top 380 twips; left/right/bottom 300 twips |
| Header/footer distances | 140 / 150 twips |
| Columns | Four equal widths, 150-twip gaps, vertical separators |
| Usable column width | Approximately 2797.5 twips at the reference geometry |
| Body | Calibri, 6.5 points, black, justified |
| Headings | Bold Calibri, 8.5 points, blue `1F4E78`, kept with following text |
| Paragraph rhythm | Zero before/after; Word auto line spacing 180/240 = 0.75 |
| Inline labels | Bold topic lead-ins within short paragraphs |
| Tables | Fixed column width, compact 20-twip cell margins, gray borders, pale-blue `DDEBF7` header, left-aligned text |
| Header | Small, right-aligned current course/aid label; no separate cover |
| Mathematics | Editable native Word equations, Cambria Math; source contains 32 equations |
| Flow | Controlled column breaks, related procedures grouped together; topics may span multiple columns when needed |

These are reproducible starting measurements, not a promise that different content or font substitution will fit. The DOCX's real run properties override several named styles. Measure the copy after applying a preference instead of assuming a changed style changed all text.

Read the reference's second page as well as its preview: it demonstrates compact equations, comparison tables, and procedures. Do not force eight topic headings or equal space per chapter just because the source has eight major column groups. Avoid literal text replacements that accidentally leave old course details in headers, tables, equations, comments, or metadata.

## Coverage before compression

Create a compact companion map with columns such as topic, source/page, exam status, sheet location, and coverage (`covered`, `partial`, `missing`, `excluded`, `unresolved`). Use PDF-viewer page numbers or actual slide numbers consistently. An exam-specific course section and explicit teacher exclusions outrank a random older exam.

Check every required chapter, including conceptual subsections that have no exercise in the practice set. A chapter heading alone is not coverage: note which concepts or methods are actually summarized. Do not inherit omissions in this reference as proof that the omitted topic is never examinable.

For a new subject, use its current sources. The reference's placeholder text is layout scaffolding, not syllabus content. Replace it with the new course material.

## Keep the sheet executable

- A definition should distinguish a concept from its common near-neighbor.
- A formula should identify symbols, units, prerequisites, and the intended result.
- A calculation procedure should show input, transformations, result, and a quick check. Inverse notation alone does not explain how to compute an inverse.
- When worked examples are selected, use independently checked numbers and make the decisive step visible, rather than just state a numerical answer.
- A comparison table should help choose the correct method, not replace necessary reasoning with isolated labels.
- An error reminder should point to an actual mathematical or conceptual trap, not predict exam questions.

For instance, "find the inverse modulo the specified modulus; verify the product leaves remainder one" is more usable than a bare inverse symbol for a student who asked for calculation support. Apply that lesson to the new subject without adding unrelated subject matter.

## Use the available page budget

The saved default is to fill the usable space with relevant study content. Aim for nearly full page and column heights, allowing small gaps that preserve readable equations and complete procedures. Do not preserve empty lower sections merely because the retained reference has them or because the requested page count has already been reached.

After the first render, inspect each page and column for substantial unused areas. Compare them with the coverage map and current sources. First restore omitted or overcompressed required concepts, symbol definitions, formula conditions and usage, calculation steps, useful distinctions, and common mistakes. When the user has selected worked examples or diagrams, use the remaining space for those where they help. Their inclusion is a separate preference: ask when unspecified rather than assuming they are needed to fill space.

Rebalance content across columns instead of leaving large gaps caused by early manual breaks. Recalculate additions and update the coverage map, then render and inspect again. Keep the selected font sizes, geometry, page budget, and legibility; check matrix row separation and complete procedure flow after expansion.

Stop when the pages are well used or no further useful, source-supported additions remain. Never fill space with repetition, administrative detail, unrelated topics, unsupported claims, decorative padding, or inflated spacing. Do not shrink type or add pages to achieve fullness. If useful content is exhausted, retain the remaining space and briefly explain the reason in the companion file.

## Fit and final checks

Remove duplicates first. Then shorten prose, combine nearby definitions, and replace repeated statements with a comparison. Do not remove conditions that make a formula valid. If a required concept remains uncovered, disclose it before calling the sheet comprehensive.

When changing paper size, orientation, margins, or column count, derive table widths from the new usable column width. Do not reuse a hard-coded full-page table width. Avoid equations or indivisible tokens wider than the column. Verify column breaks and the order in which a reader encounters tables and examples.

Render every page and check actual page count. A filename saying "2 pages", a Word metadata count, or the retained preview is not sufficient. Inspect at both reading zoom and real print size. Keep superscripts, subscripts, accents, tables, and section headings intact. If PDF export uses a different renderer, verify that PDF too.

Small type and narrow margins are an explicit style choice here, not a general recommendation for all students or printers. State Letter/A4/etc. and 100%/actual-size printing; avoid "fit multiple pages per sheet". Encourage a test print, and offer a less-dense variant if the student cannot comfortably read the result.
