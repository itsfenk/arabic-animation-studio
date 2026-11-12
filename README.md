# Arabic Animation Studio

**An Arabic-first production skill for research-led animated videos.**

Arabic Animation Studio helps an AI coding/creative agent plan, research, write, storyboard, produce, quality-check, and package animated videos in clear Modern Standard Arabic. It supports religious, historical, heritage, educational, factual, fictional, speculative, and mixed-format projects. Duration and visual style are chosen per project.

> This repository is the skill/instruction layer. It is not a copy of the upstream animation engine and does not bundle Remotion, ElevenLabs, fonts, stock media, or other third-party assets.

## Key features

- User-provided source intake for PDFs, books, articles, URLs, notes, images, and transcripts.
- Traceable source register and claim ledger, with page/section/timecode references.
- Strict religious-content verification and safeguards against fabricated religious wording, events, or attributions.
- Historical and cultural source comparison with uncertainty clearly labeled.
- Modern Standard Arabic scriptwriting, pronunciation planning, RTL graphics, and subtitle guidance.
- Flexible narrative structures, video lengths, aspect ratios, and visual approaches.
- Storyboard-first production and detailed continuity/quality checks.
- Safe integration guidance for an existing local Remotion/Python animation engine.

## Install in Codex

Codex supports skill folders containing `SKILL.md` plus optional references and assets. For a project-local installation, place this folder at:

```text
<your-workspace>/.agents/skills/arabic-animation-studio/
```

For a personal installation available across projects, use:

```text
$HOME/.agents/skills/arabic-animation-studio/
```

On Windows, `$HOME` normally resolves to your user profile directory. Extract the ZIP first, then copy the complete `arabic-animation-studio` folder—not just `SKILL.md`—into the selected location. Start Codex in the relevant workspace and invoke the skill explicitly with `$arabic-animation-studio` (or select it from the skill picker). If Codex does not detect a newly added skill, restart Codex. See `INSTALL-CODEX.md` for a short checklist.

These are Codex skill locations, not a command to overwrite or merge the upstream engine. Keep this skill and the `what-if-animation` engine as separate folders.

Start a project with a request such as:

> أريد إعداد فيديو وثائقي قصير عن بيت الحكمة. سأعطيك كتابًا ومقالتين كمصادر أساسية. حلّل المصادر أولًا، ثم اقترح معالجة وسيناريو، ولا تبدأ الإنتاج قبل مراجعة البحث.

For projects using the upstream engine, provide the path to your local `what-if-animation` clone if the agent cannot discover it in the current workspace. The skill must inspect the local version before making changes.

## Project structure

- `SKILL.md` — main operating instructions and workflow.
- `references/` — research, religious policy, Arabic language, visual design, engine, sound, and QA rules.
- `workflows/` — playbooks by content type and format.
- `templates/` — reusable project documents and source/claim tracking sheets.
- `examples/` — safe examples and illustrative structures, not pre-verified factual content.

## Important boundaries

- A user-provided source is not automatically reliable; it must be evaluated.
- A source citation is not proof that the exact claim is supported. The exact passage or data must be checked.
- Religious claims that cannot be verified under the strict protocol are omitted or escalated for review.
- The upstream SVG/Remotion engine is not a native 3D renderer. Different visual formats may require external assets, other software, or a separate adapter.
- No local project files are modified and no remote repository is published by merely installing this skill.

## Upstream engine reference

The technical reference used while designing this skill is [`kelano86/what-if-animation`](https://github.com/kelano86/what-if-animation). It provides a Remotion/SVG studio and Python production scripts. This skill is a separate project and does not claim authorship of, or ownership over, that upstream code. Preserve its original license and attribution notices when reusing any of its code or substantial portions.

## Status

Initial skill package. It has been structurally checked as a set of Markdown/CSV/JSON files, but it has **not** been installed into the user's local agent, connected to their local engine, or used to render a finished video. Those checks must happen in the user's actual environment.
