# Install this skill in Codex (Windows / VS Code)

1. Extract `arabic-animation-studio-v0.1.0.zip`.
2. Open the folder of the project where you want Codex to use this skill. If you are working with the original animation project, this can be the root of your local `what-if-animation` working copy—but do not put the skill files inside the engine's `studio/` folder.
3. Create this path inside that workspace if it does not exist:

   ```text
   .agents/skills/arabic-animation-studio/
   ```

4. Copy the **entire extracted `arabic-animation-studio` folder** into that location. The result should include:

   ```text
   .agents/skills/arabic-animation-studio/SKILL.md
   .agents/skills/arabic-animation-studio/references/
   .agents/skills/arabic-animation-studio/workflows/
   .agents/skills/arabic-animation-studio/templates/
   ```

5. Open/reopen the workspace in Codex. If the skill does not appear, restart Codex.
6. In a Codex message, invoke it with `$arabic-animation-studio`, then give the topic and attach/provide the source material.

## Personal installation

To make the skill available in all workspaces, copy the complete folder to:

```text
%USERPROFILE%/.agents/skills/arabic-animation-studio/
```

## First use with the upstream engine

Keep the skill folder separate from the original engine clone. Start Codex in the parent workspace that contains both folders, or give it the exact path to your local `what-if-animation` clone. Ask it to inspect the local checkout and report its status before it changes anything. The skill's engine-integration reference explicitly requires a backup/separate working copy and prohibits overwriting the original engine.

## Notes

- Do not paste API keys into chat or into the skill files.
- Do not commit `.env` files.
- Do not run a paid voice/sound generation step until the expected use/cost has been reviewed and approved.
- Installing the skill does not install Node, Python, FFmpeg, Remotion, or any engine dependencies.
