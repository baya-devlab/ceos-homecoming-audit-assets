# CEOS Homecoming After Review Polish 2

- Branch: `feature/hero-intro-reveal`
- Basis: local dev server + Playwright emulation
- Capture set: `after-review-polish-2`
- Captured at: 2026-06-26 15:08:45 KST
- Viewports: mobile 390px, mobile 430px, desktop 1440px
- Actual iPhone Safari keyboard-open: not directly verified

## Feedback Coverage

| Item | Status | Notes |
|---|---|---|
| Wanted loading copy | PASS | 4 sequential centered steps, 4000ms loading retained. |
| Result wording | PASS | `연결 가능성` with input-based pseudo-random score in allowed range. |
| Result layout | PASS | Top result box removed; only contact area remains card-like. |
| Contact section title | PASS | `알림 받을 연락처` removed; validation retained. |
| Why tone | PASS | Body text toned down, key phrases stay white/bold. |
| LOOKING FOR hierarchy | PASS | TYPE strengthened; WANTED NODE/CONFIDENTIAL toned down. |
| LOOKING FOR fade | PASS | Fade starts lower; FOUNDER icon remains visible. |
| `/nodes` return target | PASS | Back CTA points to `/#looking-for`. |
| `/nodes` heading | PASS | Two-line title, subtitle removed, anonymous placeholders retained. |
| Featured Nodes fade | PASS | Bottom fade strengthened, CTA remains outside fade. |
| Timetable title/TPO/grid | PASS | Requested title line break, no-wrap TPO line, 3-column row alignment. |
| Timetable `&` wrapping | PASS | Mobile wraps with `&` at end of first line. |
| Facilitated Flow copy | PASS | Mobile line break after `위해`. |
| Tickets deadline/timer/chip | PASS | Smaller centered deadline copy, stronger timer pulse, border-hugging CEOS ONLY chip. |
| Priority benefits | PASS | Priority benefits match Earlybird list. |

## Mobile 390/430 Observations

- People Graph result shows `연결 가능성 73%` for the test Wanted input and keeps contact CTA accessible.
- Timetable TPO line stays on one line in the 390px capture without horizontal scroll.
- LOOKING FOR lower cards still read as continuation, with the FOUNDER icon visible before the fade.
- Tickets chips sit on the card top border; Priority no longer says `Open Mic 이용권`.

## Remaining Visual Risks

- Actual iPhone Safari keyboard-open behavior is still not directly verified; Playwright viewport/scale checks passed.
- `/nodes` is intentionally placeholder-only and does not expose real attendee data.
- Wanted lead and application form data are UI-only; no backend save or payment is connected.
