# Prepal Cheat Sheet

A reusable Codex skill for source-grounded study sheets in a compact, editable format.

The default layout is **two printed Letter pages, four columns per page**, with blue headings, Calibri 6.5-point body text, native Word equations, and compact tables. Language, page count, typography, and emphasis can be changed per request.

The skill aims to fill the usable space with relevant information. It asks about worked examples and diagrams when you have not specified them; neither is automatically required.

## Install by asking your agent

Give this command to Codex:

```text
Use $skill-installer to install https://github.com/zakikero/prepal-cheat-sheet-skill/tree/main/skills/artifact-template-prepal-cheat-sheet. Use my existing GitHub access. If a valid installation already exists, preserve it and my saved preferences rather than overwriting it.
```

This repository is **private**. Each person needs repository access and an authenticated Git connection or another authentication method supported by their Skill Installer. Do not paste access tokens into the conversation. If Git is not authenticated, sign in locally with your normal GitHub tools.

The agent should locate its built-in Skill Installer and use the available Python runtime. Its equivalent installer arguments are:

```text
--repo zakikero/prepal-cheat-sheet-skill --path skills/artifact-template-prepal-cheat-sheet --ref main --method git
```

The built-in installer copies the entire skill directory, including the reference and preferences. Its default destination is under `$CODEX_HOME/skills`, or `~/.codex/skills` when `CODEX_HOME` is unset. Let your agent resolve the paths for your installation. The installer stops if the destination already exists; it does not automatically update an existing skill.

## Use it

On your next turn, attach your course files or provide their folder and ask:

```text
Use $artifact-template-prepal-cheat-sheet to create a two-page study sheet from these files. Include the relevant formulas with brief explanations of how to use them. Fill the available space with useful material and ask whether worked examples or diagrams would help if I have not specified them. Deliver an editable DOCX, a verified PDF, and a separate coverage companion.
```

To install and start a sheet in the same request:

```text
Use $skill-installer to install https://github.com/zakikero/prepal-cheat-sheet-skill/tree/main/skills/artifact-template-prepal-cheat-sheet, preserving any valid existing installation and saved preferences. Then read the installed SKILL.md directly and follow it to create a two-page study sheet from my attached course files. Ask about examples and diagrams if unspecified.
```

New skills are normally detected automatically. If the skill is not visible, start a new turn or restart Codex. Reading the installed `SKILL.md` directly lets the agent follow it during the installation turn without assuming the skill list has already refreshed.

## What it does

- Maps the supplied course material before compressing it.
- Includes required topics even when they have no practice exercise.
- Keeps formulas usable with definitions, conditions, units, and application steps.
- Uses exercises to prioritize space without treating them as an exam guarantee.
- Revisits avoidable blank areas after rendering and adds useful source-supported information.
- Preserves the chosen page limit, geometry, font size, and legibility.
- Checks every rendered page, equations, tables, and column boundaries.
- Keeps scope, source discrepancies, exclusions, and unresolved gaps in a separate companion.

Examples and diagrams are separate preferences. If no answer is available, the skill uses compact explanations and procedures rather than silently enabling those options.

## Defaults and customization

The defaults are stored in [default-preferences.json](skills/artifact-template-prepal-cheat-sheet/assets/default-preferences.json). They include French Canadian, two pages, relevant use of available space, and `"ask"` for worked examples and diagrams.

For example:

```text
Use $artifact-template-prepal-cheat-sheet, but make this one English, with three columns and no worked examples.
```

A one-off request changes that sheet. Ask explicitly to remember a choice if you want the agent to update your local defaults. Keep existing local preferences when downloading a new version.

## Reference and dependencies

The retained [reference.docx](skills/artifact-template-prepal-cheat-sheet/assets/reference.docx) and preview contain **neutral layout placeholders**, not private course notes. They demonstrate the design; they are not content to reuse as a syllabus.

This repository does not include course uploads, completed student sheets, private workspace files, credentials, or document rendering runtimes.

Use a Codex environment with document creation and PDF rendering tools. The skill uses the Documents and PDF workflows when available. Calibri and Cambria Math should be available for the closest match; font substitution requires a fresh render and layout check. If rendering is unavailable, the agent must label the editable document as an unverified draft.

## Sharing

Add collaborators in this repository's GitHub access settings before sending them the installation command. A private repository link alone does not grant access.

## Package

```text
skills/artifact-template-prepal-cheat-sheet/
  SKILL.md
  artifact-template.json
  agents/openai.yaml
  assets/default-preferences.json
  assets/reference.docx
  assets/preview.png
  references/layout-and-content.md
  references/preferences.md
```

## Documentation

- [OpenAI documentation on skills and Skill Installer](https://learn.chatgpt.com/docs/build-skills)
- [Skill instructions](skills/artifact-template-prepal-cheat-sheet/SKILL.md)
- [Layout and content guidance](skills/artifact-template-prepal-cheat-sheet/references/layout-and-content.md)
