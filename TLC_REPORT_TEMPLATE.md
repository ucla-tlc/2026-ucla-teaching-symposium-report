# TLC academic program / event reports — web + PDF template

Use this checklist when building post-event survey reports (or similar artifacts) for TLC programs.

## Naming and URLs

- **Public URL / repo slug:** `{year}-{event-or-program-slug}-{artifact}`  
  Example: `2026-ucla-teaching-symposium-report`
- **Banner kicker (year first):** `{year} · {Event or program name} · {Artifact type}`  
  Example: `2026 · UCLA Teaching Symposium · Post-Event Survey Report`
- **Official event title:** Use the full published name everywhere (title tag, `<h1>`, footer, appendix source lines).

## Hero (banner)

1. **Kicker** — year, program/event, artifact type (see above).
2. **`<h1>`** — full official event name (subtitle included if part of the brand).
3. **Event description** — `.hero-event-desc`; program leads enter text or pull from the event website. Use **past tense** for post-event reports.
4. **Event attendance block** — `.hero-event-stats` grid:
   - Event date
   - RSVPs / registered (fill when known; use em dash + helper text until then)
   - Attended (reconciled), with in-person / remote breakdown if applicable
   - Attendance yield (attended ÷ registered when registration is known)
5. **Survey meta line** — collection dates, n, anonymity.

## Page structure

- **Section 1 Overview** — always visible (not in a section accordion).
- **Sections 2+** — wrap in `<details class="report-section">` with numbered `<summary>` for quick navigation.
- **Print / Save as PDF** — `printReport()` opens all `<details>` before printing.

## Demographics and charts

- Prefer **tables + one complementary chart** per topic; avoid redundant encodings (e.g. do not pair a detailed role table with a faculty vs. non-faculty doughnut).
- For division/school: **100% stacked bar** for top-level groups; detailed sub-rows stay in the table only.
- Likert / distribution charts: shared color key in collapsible `<details class="likert-color-key">`.
- Charts: decorative + `role="img"`, expandable data tables, click-to-enlarge modal with **raised `devicePixelRatio`** in popup for sharp rendering.

## Methodology (standard bullets)

- Event date
- Survey field dates
- Test / internal response exclusion
- Response rate denominator rules (e.g. TLC staff exclusion)
- Participation-mode and sub-sample limitations

## Accessibility

- Skip links, focus styles, table captions/`scope`, reduced motion, keyboard-operable disclosures.

## Deploy

- Single-file HTML (+ Chart.js CDN) as `index.html` for GitHub Pages.
- Do not commit raw survey exports unless explicitly approved.
