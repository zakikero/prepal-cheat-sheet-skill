# Personalizing a Prepal Cheat Sheet

Read the saved defaults in `assets/default-preferences.json`; this file explains their meaning. Natural-language preferences are sufficient. Translate them into applied settings in the task's companion file, not a forced configuration exercise for the student.

## Override order

1. Confirmed exam restrictions are hard constraints. Surface conflicts with a requested layout rather than producing noncompliant exam notes.
2. Explicit preferences for this sheet override saved defaults.
3. Saved defaults control unspecified options.
4. The retained reference supplies component details not represented in the JSON.

Reuse preferences already supplied in the conversation. Ask only material questions: the sources and scope, allowed notes/pages, and any genuinely unresolved tradeoff. The optional preference offer can be one short question: "Keep the dense two-page French layout, or would you like larger text, a different page count, or more detailed examples?" No answer leaves the saved design preferences in effect; it does not establish permission to bring notes to an exam.

## What may change

| Preference | Interpretation |
| --- | --- |
| `language` | Output language and terminology. Default French Canadian. Preserve mathematical identifiers and optionally retain necessary original terms. |
| `printed_pages` | Total printed sides, not physical sheets. Default exactly two. Do not add a cover page or count the separate coverage companion against this target. |
| `layout.paper`, `orientation` | Letter/A4/Legal or another specified size, portrait/landscape. Changing paper changes usable column widths and pagination. |
| `layout.columns` | Column count per page. Default four; reflow content and recompute tables when changed. |
| `layout.body_font_pt` | Chosen body size. Default 6.5 points. Larger text needs less content, different geometry, or an agreed larger budget. Never silently shrink below the selected size. |
| Margins and column gap | JSON uses twips: 1 inch = 1440 twips, 1 point = 20 twips. Reject impossible geometry. Narrow margins remain subject to printer limits. |
| Fonts, headings, separators, colors | Keep the reference look by default; allow black-and-white, different font families, or stronger navigation when requested. Warn about unavailable fonts. |
| `content.organization` | By topic by default; by exercise type or another requested order is allowed. All required topics must remain accounted for. |
| `content.detail_mode` | Default `compact` favors concise definitions, formula usage, and procedures. `compact-worked` adds worked calculations when examples are selected; `step-by-step` allocates more room to methods; `formula-first` emphasizes formulas while retaining conditions and interpretation. |
| `content.priority_topics` | Additional space for named difficulties, without assuming those are the only examinable topics. Keep course-specific priorities task-local unless the user explicitly wants them saved. |
| `content.fill_available_space` | Default `true`: use nearly all usable page and column space for relevant, source-supported content; inspect gaps after rendering and enrich/reflow before delivery. This does not authorize changing the page limit, font size, or geometry, or adding padding. |
| `content.include_worked_examples`, `content.include_diagrams` | Default `"ask"` for each. Ask whether the user wants examples, diagrams, both, or neither when not already specified. `true` includes the selected element where useful; `false` omits it. These choices are independent of filling the available space. |
| Other content switches | Enable/disable comparison tables, procedures, or mistake reminders. Keep calculation-heavy methods usable with clear steps even when numerical examples are omitted. |
| `delivery.formats` | Editable DOCX and PDF by default. Do not claim a PDF exists or is print-ready until export and rendered verification succeed. |

`automatic_font_shrinking` is false by default. Even when the user authorizes smaller type, agree on a lower bound and verify the result rather than treating it as permission for unreadable compression.

## Examples of requests

- "Keep the same format, but make it English and prioritize definitions."
- "Toujours deux pages, mais détaille davantage les calculs avec un mini-exemple pour chaque méthode."
- "Use three columns and 8-point text; tell me what cannot fit before dropping it."
- "Four pages total, A4, black-and-white, with formulas and common mistakes."

The examples are alternatives, not simultaneous defaults. If two printed pages, larger type, and unchanged content cannot all be satisfied, present the tradeoff; do not pretend a preference setting guarantees fit.

## Asking about examples and diagrams

For a new sheet, resolve the two inclusion choices independently. Reuse each explicit choice from the current request and ask only about examples or diagrams whose inclusion remains unspecified. Use one brief preference question, such as "Would worked examples, diagrams, both, or neither be useful for this sheet?" Combine it with any other missing information; do not ask for these choices again once answered. Continue reviewing sources while waiting. If no answer is available, use compact explanations and procedures and state that choice; do not silently treat optional elements as selected.

Filling available space remains the default regardless of the answer. Expand relevant explanations, formula conditions and application steps, distinctions, and common mistakes when examples or diagrams are not selected. A previous sheet's subject, exercises, or visuals do not become permanent defaults.

## Saving preferences

One-off requests change only the new document and its companion. Only update `assets/default-preferences.json` when the user explicitly asks to remember a preference for future sheets. Preserve unrelated keys and the retained reference. Keep current course materials, exam dates, credentials, and personal study history out of global preferences.

If this skill folder is not writable, save a clearly identified task-local preference file and say it is not an installed global default. Do not change other skills or user configuration to work around that limitation.
