---
name: artifact-template-prepal-cheat-sheet
description: "Create or customize dense exam cheat sheets using the retained Prepal Cheat Sheet layout, with adjustable page count, typography, language, topic emphasis, and worked examples. Use when this template is selected or a similar compact exam aid is requested; not for a single homework explanation or study-calendar planning."
---

# Prepal Cheat Sheet

Reproduce the compact reference-sheet format the user approved: two printed pages, four columns per page, small text, blue topic headings, compact comparison tables, and editable mathematical equations. Adapt the content to the current course and the student's preferences. This is a standalone sheet-making skill; it does not require Prepal, calendar access, or a particular learning platform.

## Reference and defaults

Read `artifact-template.json`, [the saved preferences](assets/default-preferences.json), and [the layout and content guidance](references/layout-and-content.md). Resolve all paths relative to this skill folder. Inspect the retained DOCX and preview rather than relying on a remembered description of the format.

The retained DOCX is a style reference, not the syllabus for a new course. Keep it byte-for-byte unchanged. Its generic placeholders demonstrate the design; replace them with the current course content, and never treat them as syllabus facts. Do not upload or publish the reference, preview, skill, or course files without a separate request.

## Establish the sheet contract

Reuse facts already supplied. Ask only for missing information that changes the result: course and sources, examinable sections and exclusions, whether notes are permitted, and the allowed number of printed sides. Two double-sided physical sheets mean four printed pages, not two. The saved two-page target is a design preference, never evidence of exam permission; confirmed exam restrictions override it. When permission is unknown, describe the result as a study aid rather than exam-approved notes.

Reuse the saved layout unless the user changes it. For a new sheet, when worked examples or diagrams have not been specified, ask one compact preference question about whether either would be useful; combine it with other necessary questions. Do not inherit these choices from the reference or a previous course. Reuse explicit choices already supplied and do not ask again. Read [preferences](references/preferences.md) for inclusion choices, fallback behavior, and saved defaults. Do not require a questionnaire or raw JSON editing.

## Select content from the current sources

Create a topic-to-source coverage map before compressing. Include required topics even when they lack practice questions. Distinguish covered, partial, missing, excluded, and unresolved topics; never claim a percentage of future exam questions is guaranteed. Explain scope conflicts and inaccessible sources.

Prioritize usable definitions, distinctions, formulas with conditions and units, calculation procedures, and common mistakes. Add worked examples and diagrams when requested or selected; they are optional content choices, not requirements for every sheet. A formula naming an operation is not necessarily a calculation method: for an unfamiliar inverse, logarithm, recurrence, or transformation, include the steps needed to apply it; add an executable example only when worked examples are selected. Allocate extra space to requested difficulties without silently deleting other required topics. Recalculate numerical examples and flag material source discrepancies outside the page-limited sheet.

## Author and personalize

Use the available Documents skill and its retained-reference workflow, plus the PDF workflow for export verification when available. Copy the reference into the current output workspace; never author over the retained original or the student's existing notes. Adapt the copy's content-bearing paragraphs, tables, equations, and course-specific header/metadata while retaining its design system. Read both pages because the second-page equation and procedure patterns matter too.

Use the measured settings in the layout reference and the selected preferences. Change direct run formatting as well as styles when adjusting typography; changing Normal alone will not change the reference's explicitly formatted text. Recompute table widths when paper geometry or column count changes. Preserve native equations, superscripts, subscripts, accents, and symbols. Keep a complete worked procedure together where practical.

Treat the permitted pages as a space budget to use well, not only a maximum. With `content.fill_available_space` enabled, aim to fill the usable area of every page and column with relevant, source-supported information. After the first render, revisit substantial gaps against the coverage map and enrich compressed explanations, formula usage, procedures, distinctions, or common mistakes; use examples or diagrams only when selected. Reflow uneven columns and render again. The reference's blank space is not a limit on content capacity. See [the space-use guidance](references/layout-and-content.md#use-the-available-page-budget).

If the content does not fit, remove repetition and tighten wording before reducing legibility. Do not silently shrink the selected font, widen the permitted page budget, or omit essential topics. Explain the tradeoff and ask which constraint may change when necessary. Do not fill spare space with unsupported facts or unrelated reference content.

## Verify and deliver

Render the final DOCX and inspect every final page. Check the actual rendered page count, column reading order, tables, equations, clipping, glyphs, header content, and avoidable unused space in every column. A correct page count alone is not sufficient; when useful source-supported content remains, expand into substantial gaps and re-render before delivery. Export and verify the PDF if supported. If rendering or export is unavailable, deliver an explicitly unverified editable draft, not a claimed print-ready result. Do not imply that a retained preview proves pagination of newly written content.

Deliver an editable DOCX and verified print-ready PDF by default, respecting requested formats. Keep an applied-preference summary, topic/source coverage map, excluded material, and unresolved gaps in a separate companion Markdown file, outside the exam page budget. Never report complete coverage while that map contains unresolved omissions.

State the paper size and actual-size/100% print setting, with no extra pages per sheet. The reference's 6.5-point text and narrow margins need a real-size print check; font substitution and printer hardware can affect readability. Suggest testing a few representative exercises with the sheet. Do not book sessions, create check-ins, or modify study progress merely because a sheet was generated.
