# CEOS Homecoming Visual Audit Report — after-review-polish-3

- Capture set: `after-review-polish-3`
- Source branch: `feature/hero-intro-reveal`
- Capture basis: local dev server + Playwright emulation
- Generated at: 2026-06-26T16:36:59
- Viewports: mobile 390x844, mobile 430x932, desktop 1440x900
- Device note: screenshots are not actual iPhone Safari captures.

## Feedback Coverage

| Area | Status | Notes |
|---|---|---|
| Featured Nodes dummy data | PASS | Landing preview uses 6 of 15 dummy nodes; `/nodes` lists all 15 with shared approved profile image. |
| `/nodes` return target | PASS | Back CTA points to `/#featured-nodes`; title uses `당신의 연결점들, / 참석자 사전공개`. |
| Featured Nodes fade | PASS | Bottom fade strengthened; CTA remains outside fade. |
| Timetable TPO chip | PASS | TPO line is a no-wrap chip on the top border of the timetable card. |
| Timetable row alignment | PASS | 390px coordinate QA showed max column delta of 1px using time-right / number-left / content-left. |
| MC carousel photos | PASS | Six provided MC photos are rendered in the carousel, duplicated for marquee continuity. |
| Tickets polish | PASS | Deadline card uses dark metallic alert styling; mobile ticket card gap increased. |
| Private Invitation copy | PASS | Base body tone lowered, `프라이빗 네트워크 이벤트` emphasized, external-limit sentence removed. |
| Referral CTA behavior | PASS | Private/Final referral CTA uses shared link-copy flow instead of opening application modal. |
| Final CTA stars | PASS | Sparkle layer contrast and glow are increased with reduced-motion fallback. |
| Application modal copy/fields | PASS | Title subcopy removed, optional/required fields updated, placeholder toned down, media consent included. |
| Application complete page | PASS | `/apply/complete` route added with requested title, copy, and three buttons. |

## Mobile Observations

- Featured Nodes now shows four preview cards before fade, using the shared profile image and anonymous `Early Node` labels.
- Timetable chip remains centered in the 390px capture without horizontal page scroll.
- MC carousel shows live event photos with dark overlay treatment.
- Application modal capture shows the top of the scrollable form; the modal scroll behavior was intentionally not changed.
- Tickets section has a clearer urgent deadline card and more separation between mobile cards.

## Remaining Risks

- Actual backend save, payment, and invite-code delivery are not connected; application submit is UI-only and routes to `/apply/complete`.
- `/nodes` remains anonymous placeholder data and does not expose real attendee data.
- Actual iPhone keyboard-open behavior was not directly verified in this audit pack.
- Application modal scroll-lock behavior was intentionally not modified per request.
