# CEOS Homecoming Wanted/Ticket Copy Polish QA Pack

Purpose:
Visual QA package for the Wanted funnel, People Graph result modal, Timetable title, Tickets card hierarchy, Private Invitation CTA removal, and share CTA copy polish.

Source branch:
hotfix/wanted-ticket-copy-polish

Capture basis:
local dev server + Playwright emulation with API requests intercepted to avoid DB writes.

Viewports:
- mobile 390x844
- mobile 430x932
- desktop 1440x900

Notes:
- App UI was modified only for the requested copy/ticket polish.
- Tracking/API/DB/OG/share URL logic was not intentionally modified.
- Screenshots are not actual iPhone Safari captures.
