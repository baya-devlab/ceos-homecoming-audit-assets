# Timetable Overflow Fix Visual Audit

- Source branch: `feature/hero-intro-reveal`
- Capture basis: local dev server + Playwright Chromium emulation
- Capture timestamp: 2026-06-26 22:53:16
- Scope: Timetable horizontal overflow fix only
- Actual iPhone/Safari capture: no

## Overflow Cause

The Timetable grid was being influenced by long `max-content` marquee tracks inside the venue and MC carousels. The page-level scroll width stayed mostly safe, but the Timetable section's internal scroll width expanded far beyond the viewport, which made the section feel stretched on mobile.

## Fix Summary

- Added Timetable-only wrapper classes with `width: 100%`, `max-width: 100%`, `min-width: 0`, and `box-sizing: border-box`.
- Kept the TPO chip on one line while constraining it with viewport-aware `max-width`.
- Kept the Timetable subtitle as normal wrapping text with `white-space: normal` and `overflow-wrap: break-word`.
- Isolated the venue carousel and MC carousel moving tracks using fixed visible viewports, `overflow: hidden`, `contain: layout paint`, and absolutely positioned tracks.
- Kept Timetable rows, Follow-up row, venue carousel, and MC carousel visually intact.
- No non-Timetable UI/UX code was intentionally modified.

## Scroll Width QA

| Viewport | innerWidth | document.scrollWidth | body.scrollWidth | PASS/FAIL |
| -------: | ---------: | -------------------: | ---------------: | --------- |
| 390 | 390 | 390 | 390 | PASS |
| 430 | 430 | 430 | 430 | PASS |

## Timetable Layout Measurements

| Viewport | Selector | Width | Left | Right | Notes |
| -------: | --- | ---: | ---: | ---: | --- |
| 390 | `#timetable` | 390 | 0 | 390 | section clipped to viewport |
| 390 | `.timetable-shell` | 350 | 20 | 370 | content wrapper |
| 390 | `.timetable-subtitle` | 350 | 20 | 370 | wraps normally |
| 390 | `.event-info-chip` | 261.92 | 64.04 | 325.96 | one-line TPO chip |
| 390 | `.timetable-list` | 350 | 20 | 370 | program card |
| 390 | `.venue-preview-carousel` | 308 | 41 | 349 | visible carousel viewport |
| 430 | `#timetable` | 430 | 0 | 430 | section clipped to viewport |
| 430 | `.timetable-shell` | 390 | 20 | 410 | content wrapper |
| 430 | `.timetable-subtitle` | 390 | 20 | 410 | wraps normally |
| 430 | `.event-info-chip` | 284.17 | 72.91 | 357.09 | one-line TPO chip |
| 430 | `.timetable-list` | 390 | 20 | 410 | program card |
| 430 | `.venue-preview-carousel` | 348 | 41 | 389 | visible carousel viewport |

## Widest Elements

- Widest visible Timetable layout element at 390px: `#timetable` width `390`.
- Widest visible Timetable layout element at 430px: `#timetable` width `430`.
- The intentionally long moving track remains isolated: `#timetable .mc-carousel-track` width `2429.53` at 390px, but `#timetable.scrollWidth` is `390`.

## Included Captures

- `timetable-390.png`
- `timetable-430.png`
- `full-mobile-390.png`
- `section-transition-mobile-390.png`
- `contact-sheet-timetable-overflow-fix.png`
