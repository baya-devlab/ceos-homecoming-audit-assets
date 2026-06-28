# CEOS Homecoming Revert Extra Node Profiles QA Pack

Purpose:
Visual QA package for the targeted rollback of the five extra `/nodes` profiles and AI-generated portrait assets.

Source branch:
hotfix/revert-extra-node-profiles

Capture basis:
local dev server + Playwright/Chrome emulation with API requests intercepted to avoid DB writes.

Viewports:
- mobile 390x844
- mobile 430x932
- desktop 1440x900

Notes:
- Only the five extra node profiles and their generated image assets were removed.
- Existing NODE N•001 through NODE N•010 data/photo/placeholder mapping was restored to the pre-expansion state.
- Screenshots are not actual iPhone Safari captures.
