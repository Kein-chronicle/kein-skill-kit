# Data & file utilities

Scope: General

Install (all): `git clone <url>.git ~/.claude/skills/<name>` — read the SKILL.md before installing.

### csv-injection-safe-export
- Type: Skill
- Source: https://github.com/Kein-chronicle/csv-injection-safe-export
- Summary: Encode CSV fields with quoting and spreadsheet formula-prefix neutralization.
- When to use: When exporting untrusted text to spreadsheet-readable CSV.
- Install: `git clone https://github.com/Kein-chronicle/csv-injection-safe-export.git ~/.claude/skills/csv-injection-safe-export`

### csv-table-diff-by-key
- Type: Skill
- Source: https://github.com/Kein-chronicle/csv-table-diff-by-key
- Summary: Compare keyed tables while preserving scalar types and structural column changes.
- When to use: When comparing exported datasets with reordered rows or columns.
- Install: `git clone https://github.com/Kein-chronicle/csv-table-diff-by-key.git ~/.claude/skills/csv-table-diff-by-key`

### pdf-page-range-parser
- Type: Skill
- Source: https://github.com/Kein-chronicle/pdf-page-range-parser
- Summary: Parse bounded page selections without silently sorting or deduplicating them.
- When to use: When splitting or reordering paginated documents.
- Install: `git clone https://github.com/Kein-chronicle/pdf-page-range-parser.git ~/.claude/skills/pdf-page-range-parser`

### exif-orientation-guard
- Type: Skill
- Source: https://github.com/Kein-chronicle/exif-orientation-guard
- Summary: Fix image-pipeline bugs caused by EXIF orientation - screenshots that "are landscape" by file size but display portrait, OCR boxes that crop the wrong area, store-screenshot size checks that disagree between tools, or generated images that look rotated 90 degrees only in some tools.
- When to use: When measuring, cropping, validating or uploading images produced by simulators, phones, or AI image tools.
- Install: `git clone https://github.com/Kein-chronicle/exif-orientation-guard.git ~/.claude/skills/exif-orientation-guard`

### image-crop-bounds-clamp
- Type: Skill
- Source: https://github.com/Kein-chronicle/image-crop-bounds-clamp
- Summary: Validate crop bounds, clamp drag movement and budget raster output dimensions.
- When to use: When implementing bounded image crop UI or raster exports.
- Install: `git clone https://github.com/Kein-chronicle/image-crop-bounds-clamp.git ~/.claude/skills/image-crop-bounds-clamp`
