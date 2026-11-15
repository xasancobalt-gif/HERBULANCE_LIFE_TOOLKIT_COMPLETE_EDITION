# Technical Testing Report

**Product:** HERBULANCE Book 28 — interactive HTML edition  
**Build system:** React 19 + Vite 7 + Tailwind CSS 4, compiled using `vite-plugin-singlefile`  
**Release:** 1.0

## Build status

- Production build command: `npm run build`
- Result: **Passed**
- Output: single-file `dist/index.html` with JavaScript and CSS inlined.
- External runtime dependency: none required after downloading the production HTML.
- Remote images: none.
- External font dependency for basic functionality: none (system font stack).
- Login/database/paid API: none.

## Implemented functionality reviewed

### Navigation and content

- Header navigation, persistent desktop sidebar, mobile navigation drawer and footer links.
- Hash-based route handling for home, start-here, contents, chapter, studio, glossary, evidence centre, FAQ, saved and about views.
- In-page anchor handling for contents and start-here sections.
- Previous/next chapter buttons and a complete 22-chapter contents index.
- Back-to-top controls.

### Reading tools

- Global local search across chapter text, titles, glossary, FAQs and key pages.
- Bookmark add/remove with local storage.
- Chapter completion tracking with progress percentage.
- Reading progress bar within chapters.
- Dark and light reading mode with stored preference.
- Chapter print stylesheet.
- Home page resume/continue controls.

### Learning tools

- Interactive labelled ear explorer with eight structures.
- Interactive vestibular exploration with four motion modes.
- Four illustrative audiogram patterns, selectable frequencies and explanatory notes.
- Noise-dose learning calculator based on an 85 dBA / 8-hour reference and 3 dB exchange rate, with explicit non-diagnostic framing.
- Flashcards with reveal and navigation.
- Fictional urgency-recognition scenarios with feedback.
- Thirteen printable worksheets with local autosave, clear/delete and print-to-PDF layout.

### Accessibility and responsiveness

- Semantic landmark structure, skip-to-content link and accessible labels.
- Keyboard-focus-visible styling.
- Escape closes search and worksheet overlays.
- Search keyboard shortcut (Ctrl/⌘ + K and `/`).
- Reduced-motion media query.
- Responsive CSS breakpoints for mobile, tablet and desktop.
- SVG diagrams include role and accessible descriptive labels; figures include captions.
- Status messages use an `aria-live` region.

### Data and privacy

- Local storage access is wrapped with error handling for restricted browser contexts.
- No user health entries are transmitted to a server.
- The experience does not attempt diagnosis.
- Source links use `rel="noreferrer noopener"` and open in a new tab.

### Printing

- General print sheet hides interface navigation.
- Worksheet print mode hides the app shell and presents the worksheet through a portal.
- Print colour variables are reset for legibility.
- Known variability: browser print-to-PDF engines differ in how they render SVG, checkboxes and text fields.

## Known technical limitations

- Local storage can be cleared by the browser/user and is not a medical record.
- The downloadable HTML captures the rendered document; in a development preview, download only after the site has been built and served from the production single-file edition.
- External references may move or show a redirect; URLs must be rechecked at each release.
- Automated browser-interaction testing and assistive-technology audit were not available in this build environment; the release should receive manual cross-browser, screen-reader and print testing before commercial distribution.
- No named clinical sign-off is included.

## Release verification checklist

| Check | Status |
|---|---|
| TypeScript/Vite production compilation | Passed |
| Single-file output generated | Passed |
| All 22 chapters included in data | Verified in source |
| Search index includes chapters, glossary and FAQ | Implemented |
| Bookmarks/progress local storage | Implemented |
| Dark/light mode | Implemented |
| Worksheet local persistence | Implemented |
| Print-specific CSS | Implemented |
| Responsive layouts | Implemented |
| Manual clinical review | Not performed |
| Full manual browser/assistive audit | Outstanding |

© 2026 HERBULANCE.
