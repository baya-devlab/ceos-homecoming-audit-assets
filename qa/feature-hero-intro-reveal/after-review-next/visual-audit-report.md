# CEOS Homecoming After Visual Audit Report

- Branch: `feature/hero-intro-reveal`
- Basis: local dev server + Playwright emulation
- Capture set: `after-review-next`
- Captured at: 2026-06-26 13:44:09 
- Viewports: mobile 390px, mobile 430px, desktop 1440px
- Actual iPhone Safari: not directly captured

## Current Observations

### Wanted
- Wanted section is simplified around the bridge copy, headline, input, counter, and `이 사람 찾기` CTA.
- `검증된 사람` is underlined in the bridge copy.
- Empty submit state shows `만나고 싶은 사람에 대해 설명해주세요`.
- Input counter is visible and capped at 100 characters.

### People Graph Modal
- Loading screen removes the modal chrome and keeps the title, subtitle, three CEOS assets, progress bar, and sequential status text centered.
- Circular halos around the loading assets are removed.
- Result state uses `요청 명확도 85%` and avoids claiming a real person has been matched.
- Contact step uses separate required name, phone, and email fields with custom validation messages.

### Application Modal
- No partial lead autosave or public profile step is present.
- Required consent copy is shown with helper text.
- Validation state shows the required consent error and application contact errors.
- The modal remains long on mobile, so the audit includes top/default and validation-position captures.

### Why Next Node
- Copy now frames the next step around who the user meets.
- `다음 단계` is emphasized as requested.

### LOOKING FOR
- Section title is split into two lines.
- Cards use the requested hierarchy: `LOOKING FOR:`, emphasized role, number chip, center glyph, `WANTED NODE`, `CONFIDENTIAL`.
- Bottom fade remains active and partially hides the last-row continuation.

### Featured Nodes
- Section label is `FEATURED NODES`.
- Title is `새로운 가능성으로 이어질 연결점들`.
- Earlybird/consent/profile explanatory copy is removed from the landing section.
- `참석자 전체보기` links to `/nodes`, which is currently a placeholder page using anonymous cards only.

### Timetable
- Timetable is simplified to the requested program flow.
- The separate explanatory textbox below the subtitle is removed.
- `행사 이후 / Follow-up Node Matching` is highlighted.
- Facilitated Flow copy mentions invited professional MC support.

### Tickets
- Ticket subtitle starts with `※` and emphasizes Wanted request review.
- Countdown card is simplified around deadline and timer.
- Earlybird, Priority, and General ticket benefits reflect the requested lists.
- Earlybird original price is shown struck-through beside 19,000원.

## Known Risks / Notes

- Wanted lead data and application form data are UI-only; they are not saved to a backend.
- `/nodes` is a placeholder page and does not expose real attendee data.
- Actual iPhone keyboard-open behavior was not directly captured; Playwright/mobile viewport captures are provided.
- Application modal is intentionally long due to the number of fields; validation capture is focused on the lower validation area.
