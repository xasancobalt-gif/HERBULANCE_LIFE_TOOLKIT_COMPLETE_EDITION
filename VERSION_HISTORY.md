# Version History

## 1.0.0 — 15 November 2026

Initial Complete Digital Edition.

### Content

- Integrated all 30 owner-supplied winning HERBULANCE editions.
- Preserved 1,541 canonical chapters and their approved order.
- Added local indexes for 3,969 search records, 1,346 glossary records and 654 consolidated reference records.
- No substantive medical/scientific manuscript change was made during integration.

### Product features

- Unified welcome screen, dashboard and complete library.
- Seven life-system and seven life-stage pathways.
- Volume overviews, related-book pathways and indexed chapter reader.
- Global offline search, Quick Action Centre and Learning Centre.
- Local bookmarks, progress, history and goals with export/import/reset.
- Independent access to all 30 original-style volumes.
- Light/dark themes, responsive layouts, printing and accessibility support.

### Offline and technical work

- Produced successful static builds for all 25 Vite projects.
- Preserved standalone editions for Books 01, 08, 17, 18 and 30.
- Repaired supplied asset paths without changing binary assets.
- Removed required remote font dependencies.
- Replaced Book 18's Tailwind browser runtime with pixel-identical compiled local CSS.
- Corrected supplied JavaScript syntax defects in Book 08 and Book 30.
- Added shared local reader controls to every volume.
- Added accessibility semantics/contrast corrections and verified all 30 volumes at mobile width.

### Verification

- 30/30 source downloads checksum-match Google Drive metadata.
- 30/30 volumes pass hosted and offline `file://` runtime checks.
- 43/43 tested pages pass the selected automated WCAG A/AA axe checks; 13 dark-theme routes also pass.
- Content preservation and local-resource verification passed.

See `QA_REPORTS/` and `MANIFEST.sha256` for evidence.
