# Newly released

### public-release-audit
- Type: Skill
- Source: https://github.com/Kein-chronicle/public-release-audit
- Summary: Read-only pre-release audit for code, skills, plugins and repos: secrets, personal data, client-specific content, git-history exposure, license, risky execution patterns, and third-party terms.
- When to use: When asked "is it safe to publish?", "review before going public", or "can I share this skill?".
- Install: `git clone https://github.com/Kein-chronicle/public-release-audit.git ~/.claude/skills/public-release-audit`

### reverse-spec-kit-public
- Type: Skill bundle (10)
- Source: https://github.com/Kein-chronicle/reverse-spec-kit-public
- Summary: A bundle of 10 skills that write Figma screen-spec documents in a standard layout from HTML mockups, requirements, IA and design guides. With a mockup it reverse-engineers the spec; without one it proposes screens from requirements.
- When to use: When producing a Figma screen-spec from an HTML mockup or requirements. Requires Claude, Chrome and the Claude in Chrome extension.
- Install: `git clone https://github.com/Kein-chronicle/reverse-spec-kit-public.git  # 이 폴더에서 Claude를 실행`

## The 10 skills inside reverse-spec-kit-public

Location: `.claude/skills/<name>/SKILL.md` in the repo. They need the kit root (`scripts/`, `docs/`, `templates/`), so **clone the whole repo and run Claude in that folder**.

| Skill | Role |
|---|---|
| `reverse-spec` | Orchestrator. Each stage must pass a gate before the next one, recorded in gates.md. |
| `rs-intake` | Stage 0. Creates the project and input folders, requests materials, confirms empty folders, and fixes the mode (reverse-engineer / proposal). |
| `rs-setup` | Stage 1. Environment check: Claude, Chrome, Claude in Chrome extension, figma.com login, Korean fonts. |
| `rs-inputs` | Stage 2. Normalizes received materials (pdf, docx, xlsx, pptx, images) into requirements.md, ia.md and design.json. |
| `rs-crawl` | Stage 3. Walks the mockup, builds the screen inventory and extracts per-screen DOM coordinates. |
| `rs-propose` | Stage 3 alternative. With no mockup, proposes a screen list for approval and builds a low-fidelity HTML mockup from requirements. |
| `rs-review` | Stage 3c. Finds contradictions between source documents and separates "AI suggested fix" from "needs confirmation". |
| `rs-figma-write` | Stage 5. Uploads files into the Figma tab and draws the spec: cover to appendix, per-screen wireframe plus description. |
| `rs-verify` | Stage 6. Rule checks (page split, board size, overlap, overflow) plus a visual check from screenshots. |
| `rs-change` | After release. Applies change requests to a shared Figma spec in place, without redrawing. |

### Before you use it
- Unofficial approach: it does not use Figma's official API/MCP. It drives the editor object of a signed-in figma.com tab through the Claude in Chrome extension. A Figma UI change can break it; check Figma's terms yourself.
- Use it only on sites and materials you own or are allowed to read and extract from. `rs-crawl` runs scripts (sometimes `eval`) on the target page.
- Keep client or internal materials only in `work/` (excluded from git).
- Korean-language only.
