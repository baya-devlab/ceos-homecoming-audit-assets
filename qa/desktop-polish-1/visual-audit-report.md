# CEOS Homecoming Desktop Polish 1 Visual Audit

## Scope

- Branch: `feature/desktop-polish`
- Base: latest `main` after production merge (`e47757a982fcc929bf6a169be48dad6860ab8a89`)
- Capture basis: local dev server + Playwright Core using system Chrome
- Production deploy: not performed
- Main merge: not performed
- Tracking/API/DB/env changes: not performed

## Viewports

- Desktop: `1440x900`, `1728x1117`
- Mobile no-regression: `390x844`, `430x932`

## Changes Checked

1. Desktop subcopy/font scale
   - Desktop-only CSS increases helper/subcopy text in landing sections and People Graph modal.
   - Mobile base text sizes were not changed.

2. Box/card glossy boundary
   - Desktop-only CSS strengthens glass panel borders, background separation, inner highlight, and subtle cyan glow.
   - The treatment stays dark navy/black glass rather than bright gray.

3. Hero video quality
   - Desktop now selects `/videos/ceos-hero-a4.mp4`; mobile keeps `/videos/ceos-hero-a4-mobile.mp4`.
   - Both MP4 assets are `496x864` H.264 according to macOS metadata, so desktop quality is still bounded by source resolution.
   - Desktop CSS adds mild contrast/saturation/brightness tuning to reduce low-quality perception without replacing the video.

4. Hero post-intro assets
   - Desktop-only positioning moves ghost assets inward from viewport edges.
   - Desktop-only animation increases peak visibility slightly while keeping the title-safe center clear.

5. Wanted modals
   - Desktop-only modal width, min-height, spacing, loader size, result label, score, helper copy, and CTA sizing were increased.
   - Mobile modal CSS was not changed.

6. Looking For readability
   - Desktop-only card positions were spread into a readable dossier board.
   - `PRODUCT BUILDER`, `AI OPERATOR`, `TECH LEAD`, `BRAND DESIGNER`, `MARKETER`, and `FOUNDER` are visible in the 1440 capture.

7. Featured Nodes desktop carousel
   - Desktop-only marquee/fade mask added.
   - Mobile grid remains unchanged.
   - Duplicate carousel cards suppress duplicate `node_card_view` tracking events.

8. Featured Nodes CTA center
   - CTA is centered under the desktop carousel.

9. Timetable width
   - Desktop restores `timetable-shell` to the same max-width rhythm as surrounding sections.
   - Mobile overflow-protection remains in place.

10. Tickets timer
   - Desktop-only timer card width/padding and timer number size were reduced.
   - Timer main/subcopy hierarchy was strengthened.
   - Countdown logic was not changed.

## QA Measurements

```json
{
  "mobile390": { "scrollWidth": 390, "innerWidth": 390, "overflowOk": true },
  "mobile430": { "scrollWidth": 430, "innerWidth": 430, "overflowOk": true },
  "desktop1440": { "scrollWidth": 1440, "innerWidth": 1440, "overflowOk": true },
  "desktop1728": { "scrollWidth": 1728, "innerWidth": 1728, "overflowOk": true }
}
```

## Known Risk

- This audit uses Chrome emulation, not manual inspection on a physical large desktop monitor.
- Hero source video is still only `496x864`; desktop can be improved perceptually but not made truly high-resolution without a higher-resolution source.
- Actual iPhone/Safari keyboard behavior was not retested because this task was desktop-only and mobile layout was protected via breakpoint-scoped changes.
