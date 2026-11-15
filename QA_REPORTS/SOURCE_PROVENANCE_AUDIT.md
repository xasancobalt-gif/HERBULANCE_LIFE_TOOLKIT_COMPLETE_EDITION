# HERBULANCE Source Provenance Audit

**Audit date:** 15 November 2026  
**Source authority:** Owner-supplied Google Drive folder  
**Result:** PASS for completeness, identity and traceability

## Findings

- The owner supplied one Google Drive folder as the authoritative set of winning editions.
- The folder contained exactly 30 top-level items: 29 ZIP packages and the standalone Book 08 HTML file.
- All 30 items were downloaded separately to `01_original_sources/drive_downloads/`.
- Every local download matches Google Drive's reported byte size and MD5 checksum.
- Correct Book 06 MD5: `e9678cd8b8f8be26cc483082471e0052`.
- The archives were extracted into isolated `02_extracted_sources/book-01/` through `book-30/` directories. Total extracted files: 1,340.
- No missing or duplicate volume number was found.
- Original downloads were not edited. Integration sources, production builds and release files are maintained in separate directories.
- All 25 React/Vite projects produced successful static builds. Books 01, 08, 17, 18 and 30 use their supplied standalone HTML editions.
- Integration-only corrections for Books 05, 06, 09 and 26 are recorded in `TECHNICAL_CHANGE_REGISTER.md`.

## Evidence

- `source_drive_manifest.csv` — Drive filename, item identity, size, timestamps and MD5.
- `01_original_sources/drive_downloads/` — immutable downloaded copies.
- `02_extracted_sources/book-NN/` — isolated audit/extraction copies.
- `04_audit_reports/build_logs/` — per-volume production build logs.
- `CONTENT_PRESERVATION_AND_RELEASE_VERIFICATION.md` — final preservation chain and per-volume verification.

## Provenance limitation

The winning designations originated in earlier owner sessions that are not directly accessible from this workspace. This audit therefore relies on the owner's explicit statement that the supplied Drive folder contains the selected winners. It does not substitute any alternative edition or infer winners from appearance or buildability.
