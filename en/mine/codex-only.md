# Codex-only skills

Skills that work **only in Codex** (not for Claude Code). Install: `git clone https://github.com/Kein-chronicle/codex-imagegen-skill.git ~/.codex/skills/imagegen`

### imagegen
- Type: Skill (Codex only)
- Target tool: **Codex only**
- Source: https://github.com/Kein-chronicle/codex-imagegen-skill
- Summary: A Codex skill that generates or edits raster images (photos, illustrations, textures, sprites, mockups). The built-in image_gen tool is the default (no API key); the CLI fallback runs only on request and needs OPENAI_API_KEY. Transparent backgrounds are generated on a chroma key and removed locally with the bundled remove_chroma_key.py.
- When to use: New images, style/composition from reference images, inpainting, background replacement, object removal, asset variants, transparent cut-outs. Not for shapes, diagrams or icons better built in SVG/HTML/CSS.
- Install: `git clone https://github.com/Kein-chronicle/codex-imagegen-skill.git ~/.codex/skills/imagegen`
- License / provenance note: Licensed under Apache-2.0 (LICENSE.txt in the repo, not MIT). Its folder layout and license match the form of OpenAI's Codex imagegen system skill, so keep the LICENSE and notices and state your changes when redistributing or modifying.

## Notes
- The default path is the built-in `image_gen` tool and needs no `OPENAI_API_KEY`. The CLI fallback runs only when the user asks and needs a key.
- Generated files land under `$CODEX_HOME/generated_images/` by default; copy assets into the project folder before using them.
- Existing files are never overwritten; new files get a new name such as `hero-v2.png`.
- Transparent backgrounds are generated on a flat chroma key and removed with `scripts/remove_chroma_key.py` (confirm the CLI path with the user if true transparency is required).
