# HERBULANCE Technical QA Report

**Release:** 1.0.0  
**Date:** 15 November 2026

## Build and source result

- 30 authoritative owner-supplied items downloaded and checksum-verified.
- 1,340 extracted source files inventoried in isolated volume folders.
- 25 React/Vite projects built successfully with a relative `./` base.
- 5 supplied standalone editions retained for Books 01, 08, 17, 18 and 30.
- Every production volume contains an independently accessible `index.html`.
- Integration corrections for Books 05, 06, 09 and 26 and release corrections are fully recorded in `TECHNICAL_CHANGE_REGISTER.md`.

## Unified application

Implemented and tested:

- unified entry, welcome and dashboard;
- complete 30-volume library;
- seven systems and seven stages;
- volume relationships and chapter reader;
- global local search;
- Quick Action and Learning centres;
- glossary and reference centres;
- local progress, bookmarks, history and goals;
- export, import and reset;
- theme, print, responsive and accessibility behavior;
- shared in-book controls across all 30 editions.

## Dependency and offline result

- No required remote script, stylesheet, font, image or media dependency remains.
- Book 18 uses local, statically compiled Tailwind 4.1.17 CSS. Pixel comparison against the local browser-runtime rendering produced a zero-difference image.
- All local HTML and CSS dependencies resolve inside the package.
- The unified app and all 30 volumes were opened under actual offline `file://` conditions without captured external requests or errors.
- Core functionality uses no account, server, database, cloud storage, analytics or tracker.

## Syntax and runtime corrections

- Custom unified application and shared reader-control JavaScript pass Node syntax checks.
- All executable inline volume scripts pass browser parsing after documented Book 08 and Book 30 delimiter corrections.
- Books 07, 10, 14 and 29 supplied image paths were rebased to their existing local asset directories.
- Book 08's hosting-provider challenge injection was removed because it was unrelated to the manuscript and incompatible with offline operation.

## Assets, links and preservation

- Every canonical chapter title occurs in its final volume entry file.
- Normalized visible text matches the corresponding independently produced edition for all 30 books.
- All non-entry production assets match their release copies byte-for-byte.
- Book 27 retains 100 numbered SVG illustrations.
- External citation links are preserved as optional links; they are not required dependencies.

## Test evidence

See:

- `release_verification.json`
- `qa_runtime.json`
- `accessibility_runtime.json`
- `responsive_books_mobile.json`
- `keyboard_qa.json`
- `CONTENT_PRESERVATION_AND_RELEASE_VERIFICATION.md`
- `RUNTIME_OFFLINE_RESPONSIVE_QA_REPORT.md`
- `ACCESSIBILITY_QA_REPORT.md`

## Limitations

The executed browser test matrix used Chromium. Automated checks cannot establish clinical correctness, formal WCAG certification, storefront behavior or legal rights. Those limitations are disclosed in the scientific/safety audit and release status document.
