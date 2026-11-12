# Production engine integration: upstream Remotion/Python reference

## What the upstream project contains

The public reference project `kelano86/what-if-animation` includes:

- `studio/`: a React/Remotion project that draws scenes in SVG and registers episode compositions;
- `studio/src/engine/`: shot/episode rendering, rig, room/set, lighting, props, UI and animation helpers;
- `studio/src/episodes/`: example episodes and their shot components;
- `scripts/voice.py`: voice generation and word timing;
- `scripts/plan.py`: shot/edit planning from word timings;
- `scripts/stills.mjs` and `scripts/board.py`: still/storyboard rendering;
- `scripts/sfx.py` and `scripts/mixcheck.py`: sound generation and mix review;
- `scripts/motiongrid.py`: motion review grids;
- `scripts/master.py`: Remotion render, loudness mastering, and report;
- `scripts/wi.py`: shared paths, API, timing, and audio helpers.

This summary describes the public reference observed during skill design. Always inspect the user's local checkout; do not assume it has the same revision or exact behavior.

## Supported workflow shape

The reference short-form pipeline centers on an episode folder under `studio/src/episodes/<slug>/` and an `episode.json` containing fields such as `id`, `slug`, `topic`, `title`, `script`, `shots`, `edit`, `fx`, `sound`, and optional voice/gap controls. The local scripts create artifacts such as word timing JSON and timeline JSON, public audio stems, storyboards, render outputs, and cost reports. The exact supported keys and cue syntax must be read from the local scripts and examples before use.

The Remotion episode engine receives a timeline with segments/shots/audio and a map of React shot components. The project registers each episode in an episode index. Do not skip registration/type-checking steps.

## Important limitation

This is a code-drawn 2D SVG/Remotion engine—not a general native 3D engine and not a universal long-form documentary editor. Its existing What If formula, short episode assumptions, character rig, and room set library are optional assets, not universal requirements. A historical documentary, a long narrated explainer, a 3D sequence, or a mixed archival film may need a new adapter, another tool, or a separate project. Do not claim the existing engine can do it without checking.

## Safe local procedure

1. Ask for or discover the local upstream directory within the active workspace only. Do not scan unrelated drives or private folders.
2. Confirm the local root and studio root. The studio should have `package.json` and `src/episodes/`; scripts should be available in the expected parent repository.
3. Read `LICENSE`, `README.md`, `SKILL.md`, the local references, script source/help, package manifest, episode engine, registry, and example episode.
4. Check `git status` and current branch if the checkout is a Git repository. Do not discard uncommitted changes.
5. Create a separate working copy, branch, or new output directory. Never overwrite the original checkout.
6. Do not run dependency upgrades as part of a routine episode. Use the versions in the local lockfile.
7. Keep secrets in environment variables or the existing supported local `.env` mechanism. Never show or commit `.env`, API keys, account tokens, or private usage data.
8. Create episode files only after confirming the expected schema. Preserve UTF-8 and Arabic text. Test JSON parsing and TypeScript compilation before rendering.
9. Run dry-run/preview commands before any cost-incurring voice or sound calls. Confirm estimated cost and obtain approval when required.
10. Render a storyboard/animatic, inspect it, fix failed shots, then render animation and sound.
11. Run local audio/mix and final output checks. Watch the final video; a successful process exit is not a complete quality review.
12. Report all changes, exact commands, test results, output paths, costs if known, and unresolved limitations.

## Compatibility rule

Map the research dossier and Arabic script package into `episode.json` only if the local engine's schema supports the requested format. Keep the full source ledger outside the renderer's episode JSON; add concise claim/source identifiers to script metadata only when the schema permits. Avoid overloading `episode.json` with large research content.

If the existing engine lacks a needed capability, prepare a minimal adapter proposal with: requirement, current limitation, files that would change, backward-compatibility plan, test plan, and rollback. Ask before implementing structural engine changes.
