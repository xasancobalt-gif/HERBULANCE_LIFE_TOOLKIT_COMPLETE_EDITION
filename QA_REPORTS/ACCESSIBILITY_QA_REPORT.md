# HERBULANCE Accessibility QA Report

**Test date:** 15 November 2026  
**Automated engine:** axe-core 4.10.3 in Chromium 141  
**Rulesets:** WCAG 2.0 A/AA and WCAG 2.1 A/AA tags

## Result

**PASS for the executed automated checks:** 43 pages tested, zero remaining automated violations at the selected A/AA rulesets.

## Coverage

- 13 unified-application views: dashboard, library, systems, stages, search, Quick Actions, Learning Centre, glossary, references, personal learning, help, a book overview and chapter reader.
- All 30 independent volume entry pages.
- 13 unified-application views additionally checked in dark theme: zero violations.
- Keyboard checks covered search open/focus, Escape close, mobile menu activation and independent-volume reader-panel activation.
- Mobile overflow checked across all 30 independent volumes.

## Corrections applied

- Added a persistent non-colour underline cue to links in source volumes.
- Added a consistent visible keyboard focus indicator.
- Generated accessible names for unlabeled Book 08 checklist controls from their adjacent existing wording.
- Repaired invalid list semantics exposed by Books 08 and 30 without changing text.
- Added volume-scoped contrast corrections based on measured axe failures.
- Increased dark-theme eyebrow and destructive-action contrast in the unified shell.
- Added responsive containment and table scrolling, with scoped mobile header corrections.
- Retained reduced-motion behavior.

## Evidence

- `accessibility_runtime.json` — complete 43-page final axe run.
- `accessibility_dark_theme.json` — 13-route dark-theme result.
- `keyboard_qa.json` — keyboard interaction result.
- `book-accessibility.css` in the application assets — volume-scoped rendering corrections.

## Important limitation

Automated accessibility testing detects only part of WCAG conformance. This report does not claim formal certification. Before a broad public launch, conduct manual testing with keyboard-only users and representative screen readers (for example NVDA/Firefox, JAWS/Chrome, VoiceOver/Safari and TalkBack/Chrome), at 200–400% zoom, and with users who have disabilities. The 30 source interfaces differ substantially, so task-based human testing remains valuable even after a zero-violation automated run.
