# HERBULANCE Runtime, Offline and Responsive QA Report

**Test date:** 15 November 2026  
**Browser engine:** Chromium 141.0.7390.37 through Playwright 1.56.1  
**Release:** HERBULANCE LIFE TOOLKIT — The Complete Digital Edition 1.0.0

## Result

**PASS** for tested runtime, local `file://`, offline, route, search, independent-volume, responsive and keyboard interactions.

## Unified application checks

- Welcome screen opened and Start Exploring loaded the dashboard.
- Dashboard rendered four summary statistics.
- Library rendered exactly 30 book cards.
- Seven life-system cards and seven life-stage cards rendered.
- Book 01 overview rendered 12 chapters; Book 25 rendered 80 chapters.
- Global search for “sleep” returned 150 results in the hosted test.
- A search result opened the indexed chapter reader with full local text.
- Library, systems, stages, Quick Action Centre, Learning Centre, glossary, references, personal-learning, help, Book 01 and Book 30 routes opened without captured page errors.

## Independent editions

- All 30 `books/book-NN/index.html` pages returned successfully in the hosted test.
- All 30 displayed the shared LIFE TOOLKIT reader control.
- No console error, uncaught page error or failed required request remained.

## Actual local/offline checks

Tests used a browser context with networking disabled and opened the files with `file://` URLs.

- Root `index.html` opened.
- Dashboard and global search opened; “digestion” returned 121 local results.
- **All 30 independent volumes opened under `file://`.**
- All 30 displayed meaningful body content and the shared reader control.
- No volume attempted an HTTP/HTTPS resource request.
- No root application error or external network request was captured.

## Responsive checks

- Unified application tested at 390 × 844: mobile menu visible, drawer opened, no document-level horizontal overflow.
- Every independent volume tested at 390 × 844.
- Final result: 30/30 volumes had no document-level horizontal overflow or page error.
- Tables remain horizontally scrollable within their own containers where required.
- Scoped corrections were applied to Books 01, 05, 08 and 30 for previously clipped mobile controls.

## Keyboard interaction checks

- `/` opened global search and moved focus to the search field.
- Escape closed the search dialog.
- Mobile navigation opened by keyboard and updated `aria-expanded`.
- The independent-volume LIFE TOOLKIT control opened by keyboard and exposed its panel.
- Visible focus rules and reduced-motion support are included.

## Evidence

- `qa_runtime.json` — full hosted and `file://` runtime record.
- `responsive_books_mobile.json` — per-volume mobile dimensions and result.
- `keyboard_qa.json` — keyboard interaction result.
- `screenshots/` — desktop and mobile evidence captures.

## Limitations

Runtime QA used Chromium. Current Chrome, Edge, Firefox and Safari are expected to work because the application uses standard static HTML/CSS/JavaScript, but this report does not claim an executed test in every browser/OS combination. External citation links were not treated as offline dependencies and require a connection only when the user chooses to open them.
