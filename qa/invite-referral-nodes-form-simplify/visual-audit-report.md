# Invite Referral Nodes Form Simplify Visual Audit

Capture basis: local dev server + Playwright emulation.

Viewports: mobile 390x844, mobile 430x932, desktop 1440x900.

Included captures:

- application-modal-desktop-1440.png
- application-modal-invited-mobile-390.png
- application-modal-normal-mobile-390.png
- featured-nodes-desktop-1440.png
- featured-nodes-mobile-390.png
- invite-overlay-desktop-1440.png
- invite-overlay-mobile-390.png
- nodes-desktop-1440.png
- nodes-mobile-390.png
- nodes-mobile-430.png
- nodes-sticky-desktop-1440.png
- nodes-sticky-mobile-390.png
- normal-landing-desktop-1440.png
- normal-landing-mobile-390.png
- private-invitation-desktop-1440.png
- private-invitation-mobile-390.png
- timetable-desktop-1440.png
- timetable-mobile-390.png

Observed checks:

- Invite overlay renders for QAIVT01 on mobile and desktop.
- Normal landing capture uses share URL without invite overlay.
- Application modal captures include normal and invited states.
- /nodes captures include N011-N016 profile additions and sticky CTA states.
- Timetable and Private Invitation sections are captured after row-description and CEOS intro button additions.

Notes:

- These screenshots are not real iPhone Safari captures.
- QA invite row uses QAIVT01 and must be cleaned from Neon after smoke tests.
