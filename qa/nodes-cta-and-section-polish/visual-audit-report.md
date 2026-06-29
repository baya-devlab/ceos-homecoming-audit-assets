# CEOS Homecoming Nodes CTA And Section Polish QA

Capture basis: local dev server + Playwright/Chrome emulation

Viewports:
- mobile 390x844
- desktop 1440x900

Scope:
- `/nodes` sticky top bar and sticky application CTA
- Timetable follow-up description emphasis
- Tickets timer height reduction
- Final CTA share button width alignment

Results:
- `/nodes` sticky bar remained fixed while scrolled.
- `/nodes` sticky CTA opened the existing application modal.
- `cta_click` and `application_modal_open` were observed with `cta_id: nodes_sticky_apply_click`.
- Final CTA share button copied `https://ceos-homecoming.vercel.app/?share=next-node`.
- Mobile and desktop horizontal overflow measured `0`.
- `/nodes` data/profile/image files were not changed.
- DB/API/schema files were not changed.
- OG/share URL constants were not changed.

Notes:
- Browser QA mocked local `/api/*` calls to avoid creating QA rows in Neon DB.
- Screenshots are Chrome emulation, not actual iPhone Safari captures.
