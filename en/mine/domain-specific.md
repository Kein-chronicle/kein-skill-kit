# Domain-specific

Scope: Domain-specific

Install (all): `git clone <url>.git ~/.claude/skills/<name>` — read the SKILL.md before installing.

### canvas-render-pixel-gate
- Type: Skill
- Source: https://github.com/Kein-chronicle/canvas-render-pixel-gate
- Summary: Verify that art assets actually appear on screen by measuring rendered pixels instead of grepping source.
- When to use: When a game/app "has the sprites" but plays like grey boxes, when assets are generated but not wired into the play scene, when a gate counts load.image/add.image calls, or when you need an objective rendered-richness check (unique colours, top-N colour share) on a screenshot. Exit code 3 means "could not measure", never a pass.
- Install: `git clone https://github.com/Kein-chronicle/canvas-render-pixel-gate.git ~/.claude/skills/canvas-render-pixel-gate`

### ai-sprite-pipeline-audit
- Type: Skill
- Source: https://github.com/Kein-chronicle/ai-sprite-pipeline-audit
- Summary: Control quality and consistency when mass-producing game characters/sprites with image generators - hash-pinned style master ("only one reference defines the style"), generation ledger, manifest of every action x direction x frame, RGBA/transparency/duplicate checks, atlas grid and baseline contracts …
- When to use: When producing hundreds of AI-generated frames for a cast of characters, when styles drift between characters, or when generated PNGs have baked-in backdrops.
- Install: `git clone https://github.com/Kein-chronicle/ai-sprite-pipeline-audit.git ~/.claude/skills/ai-sprite-pipeline-audit`

### game-asset-license-ledger
- Type: Skill
- Source: https://github.com/Kein-chronicle/game-asset-license-ledger
- Summary: Keep a license ledger for downloaded game/art/audio/font asset packs so nothing with unknown, non-commercial or copyleft terms slips into a product.
- When to use: When you hoard free assets (CC0 packs, CC-BY, OGA, mixed repositories), when preparing a release, or when credits/attribution files must be generated. Checks every pack on disk has a ledger entry, classifies commercial-use risk, warns on share-alike and mixed-license repos, and writes CREDITS.md.
- Install: `git clone https://github.com/Kein-chronicle/game-asset-license-ledger.git ~/.claude/skills/game-asset-license-ledger`

### web-game-asset-reality-check
- Type: Skill
- Source: https://github.com/Kein-chronicle/web-game-asset-reality-check
- Summary: Catch "declared but not real" in built web apps and games - fonts declared but never bundled, @font-face files that do not exist, runtime CDN stylesheets and fonts in an offline-by-design app, and runtime page errors (uncaught exceptions, console errors, failed requests) that the type checker cannot see.
- When to use: Before shipping a web build, when text renders in a fallback font, or after any code-writing step to smoke-test the page in headless Chromium.
- Install: `git clone https://github.com/Kein-chronicle/web-game-asset-reality-check.git ~/.claude/skills/web-game-asset-reality-check`

### swift-runtime-trap-fuzz
- Type: Skill
- Source: https://github.com/Kein-chronicle/swift-runtime-trap-fuzz
- Summary: Catch Swift runtime traps (Int overflow, Int(Double.nan), out-of-range casts, array index, precondition) that table-driven unit tests structurally cannot see.
- When to use: When a Swift/SwiftUI app does arithmetic on user input, converts Double to Int, uses rational/fixed-point math, or when all tests are green but users can crash the app with two taps. Gives the fuzz recipe and the safe-arithmetic fixes.
- Install: `git clone https://github.com/Kein-chronicle/swift-runtime-trap-fuzz.git ~/.claude/skills/swift-runtime-trap-fuzz`

### ios-simulator-ui-test-hygiene
- Type: Skill
- Source: https://github.com/Kein-chronicle/ios-simulator-ui-test-hygiene
- Summary: Keep iOS simulator UI-test runs and crash-fuzz runs from dying on a laptop - diagnosing "stopped because the system is running low on memory", simulator process pileups, and the endless macOS crash-report dialog that appears while a fuzz gate deliberately kills your app.
- When to use: When xcodebuild UI tests die on 16GB Macs, when you run crash fuzzing, or when a "dialog that never goes away" shows up.
- Install: `git clone https://github.com/Kein-chronicle/ios-simulator-ui-test-hygiene.git ~/.claude/skills/ios-simulator-ui-test-hygiene`

### app-store-connect-api-gotchas
- Type: Skill
- Source: https://github.com/Kein-chronicle/app-store-connect-api-gotchas
- Summary: Field-tested pitfalls when automating App Store Connect (ASC) - the review-submission API sequence, age-rating declarations (advertising flag auto-rejection, per-field types, live apps), screenshot upload that appends instead of replaces, review-attachment loss on new versions, export-compliance key …
- When to use: When scripting ASC/iris API calls, preparing an app update submission, debugging an automated "age rating / advertising" rejection, or verifying what actually shipped inside an archive.
- Install: `git clone https://github.com/Kein-chronicle/app-store-connect-api-gotchas.git ~/.claude/skills/app-store-connect-api-gotchas`

### ffmpeg-video-qa-gates
- Type: Skill
- Source: https://github.com/Kein-chronicle/ffmpeg-video-qa-gates
- Summary: Machine-check rendered videos (shorts, long-form, social clips) with ffmpeg instead of eyeballing - frozen/still stretches, dead air, loudness and true peak, duration/size/audio-presence, subtitle format and reading speed, and a "flat opening" visual-density measure.
- When to use: When producing videos with an AI/automated pipeline, when you need objective publish gates, or when a video "passes" review but feels like a slideshow. Exit code 3 = could not measure, never a pass.
- Install: `git clone https://github.com/Kein-chronicle/ffmpeg-video-qa-gates.git ~/.claude/skills/ffmpeg-video-qa-gates`

### deterministic-html-motion-render
- Type: Skill
- Source: https://github.com/Kein-chronicle/deterministic-html-motion-render
- Summary: Build or audit a code-driven motion-graphics / video renderer (HTML+CSS+JS scenes captured frame by frame with headless Chrome and ffmpeg) so output is reproducible.
- When to use: When AI-written animation code renders differently on re-runs, when jumping to a frame gives a different image than playing up to it, when an agent writes scene code that must not touch clocks/randomness/network, or when you want sound as data (cue lists) instead of audio code.
- Install: `git clone https://github.com/Kein-chronicle/deterministic-html-motion-render.git ~/.claude/skills/deterministic-html-motion-render`

### cold-read-comprehension-review
- Type: Skill
- Source: https://github.com/Kein-chronicle/cold-read-comprehension-review
- Summary: Verify that a viewer/reader actually understands a deliverable (video, article, onboarding page, landing page) by giving it to isolated readers with no memory and grading their structured answers with code, not with another opinion.
- When to use: When "it passes all checks but people are confused", when you need an independent comprehension gate, when AI-produced content must be reviewed without the author's context, or when stale approvals must expire after the artifact changes.
- Install: `git clone https://github.com/Kein-chronicle/cold-read-comprehension-review.git ~/.claude/skills/cold-read-comprehension-review`

### ai-content-editorial-lint
- Type: Skill
- Source: https://github.com/Kein-chronicle/ai-content-editorial-lint
- Summary: An operating contract for AI-assisted publishing (blogs, guides, game/tech articles, video scripts from research) that keeps facts, rights and readability under control.
- When to use: When an AI drafts content from web sources, when all your articles start to look identical, when summarizing tools misquote sources, when you need an independent reviewer that actually converges, or when a reviewed manuscript must not be silently edited before publishing …
- Install: `git clone https://github.com/Kein-chronicle/ai-content-editorial-lint.git ~/.claude/skills/ai-content-editorial-lint`

### llm-adaptation-fidelity-check
- Type: Skill
- Source: https://github.com/Kein-chronicle/llm-adaptation-fidelity-check
- Summary: Guarantee that AI-written narration, summaries, scripts or adaptations stay faithful to a source text, using string comparison rather than model opinion.
- When to use: When turning an article/blog post/document into a video script, summary or social post; when you must prove quotes are verbatim, numbers exist in the source, every sentence maps to a source paragraph, new "framing" content is bounded, and dropped paragraphs are declared …
- Install: `git clone https://github.com/Kein-chronicle/llm-adaptation-fidelity-check.git ~/.claude/skills/llm-adaptation-fidelity-check`

### ai-image-pairwise-eval
- Type: Skill
- Source: https://github.com/Kein-chronicle/ai-image-pairwise-eval
- Summary: Evaluate visual quality (game art, illustrations, UI, generated images) reliably against golden reference images - rubric levels instead of absolute scores, order-swapped pairwise comparison, and CLIP/DINO embedding similarity as a consistency gate.
- When to use: Whenever you must judge if an asset is good enough, rank candidates, gate AI-generated art, or replace "looks fine to me" with a repeatable method.
- Install: `git clone https://github.com/Kein-chronicle/ai-image-pairwise-eval.git ~/.claude/skills/ai-image-pairwise-eval`

### ai-resume-screening-safeguards
- Type: Skill
- Source: https://github.com/Kein-chronicle/ai-resume-screening-safeguards
- Summary: Guardrails for AI-assisted resume screening and applicant evaluation - deterministic career arithmetic (overlap union, gaps as questions), a rubric linter that blocks protected attributes and flags proxies, prompt-injection detection in resumes, masking before the model sees data …
- When to use: When building or reviewing any AI hiring/ranking/screening tool. Not legal advice - lexicons are examples to adapt per jurisdiction and have counsel review.
- Install: `git clone https://github.com/Kein-chronicle/ai-resume-screening-safeguards.git ~/.claude/skills/ai-resume-screening-safeguards`

### pdf-annotation-rotation
- Type: Skill
- Source: https://github.com/Kein-chronicle/pdf-annotation-rotation
- Summary: Rotate boxes, lines, ink and source masks in display coordinates without mutating input.
- When to use: When implementing PDF or canvas annotation rotation.
- Install: `git clone https://github.com/Kein-chronicle/pdf-annotation-rotation.git ~/.claude/skills/pdf-annotation-rotation`

### pdf-text-position-table-extract
- Type: Skill
- Source: https://github.com/Kein-chronicle/pdf-text-position-table-extract
- Summary: Extract aligned text regions into a rectangular table while preserving empty cells.
- When to use: When turning positioned document text into CSV rows.
- Install: `git clone https://github.com/Kein-chronicle/pdf-text-position-table-extract.git ~/.claude/skills/pdf-text-position-table-extract`

### ai-companion-persona-kit
- Type: Kit (no SKILL.md)
- Source: https://github.com/Kein-chronicle/ai-companion-persona-kit
- Summary: A skeleton for a long-running AI companion character: persona-as-data, a daily situation engine, deterministic proactive messages, and a wellbeing guard.
- When to use: When designing a long-running AI companion (character) service. This is a tooling/documentation kit without a SKILL.md.
- Install: `git clone https://github.com/Kein-chronicle/ai-companion-persona-kit.git`
