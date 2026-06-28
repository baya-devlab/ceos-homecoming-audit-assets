# CEOS Homecoming Nodes Profile Expansion QA

## Scope

- Branch: `feature/nodes-profile-expansion`
- Target: `/nodes` participant preview page
- Change type: replace five `/nodes` TBD cards with five generated-profile cards and images
- Explicitly unchanged: landing UI copy, tracking, DB/API routes, OG/meta, share-link logic

## New Profile Placement

| Card | Display name | Affiliation | Role | Image |
|---|---|---|---|---|
| NODE N•011 | NODE N•011 | 서강대학교 | CS/프로덕트 학생 | `/images/homecoming/nodes/node-photo-09.jpeg` |
| NODE N•012 | NODE N•012 | 수노앤컴퍼니 | Product Engineer | `/images/homecoming/nodes/node-photo-10.jpeg` |
| NODE N•013 | NODE N•013 | 이화여자대학교 | 브랜드/커뮤니티 학생 | `/images/homecoming/nodes/node-photo-11.jpeg` |
| NODE N•014 | NODE N•014 | 숨고 | Product Designer | `/images/homecoming/nodes/node-photo-12.jpeg` |
| NODE N•015 | NODE N•015 | 홍익대학교 | UX/UI 디자인 학생 | `/images/homecoming/nodes/node-photo-13.jpeg` |

## Automated QA Summary

| Check | Result | Notes |
|---|---|---|
| `/nodes` mobile 390 card count | PASS | 15 cards |
| `/nodes` mobile 430 card count | PASS | 15 cards |
| `/nodes` desktop 1440 card count | PASS | 15 cards |
| New nodes present | PASS | NODE N•011 through NODE N•015 found |
| TBD cards removed | PASS | No `TBD` cards found |
| New images loaded | PASS | 5/5 new images loaded in 390, 430, and 1440 checks |
| Horizontal overflow | PASS | scrollWidth matched clientWidth in all checked viewports |
| Landing Featured Nodes preserved | PASS | New tail nodes are not shown in landing Featured Nodes |
| Console errors | PASS | No browser console/page errors during QA run |

## Viewports

- Mobile: 390x844
- Mobile: 430x932
- Desktop: 1440x900

## Visual Notes

- The three new student profiles are interleaved with professional profiles in the final card group, avoiding a consecutive student-only run.
- Generated portraits use clean, neutral, smart-casual styling and load through the existing card image treatment.
- The two existing confidential placeholder cards remain unchanged.
- Landing Featured Nodes still uses the existing selected four cards.

## Verification

- `npm run lint`: PASS with existing fast-refresh warnings in shared UI components.
- `npm run build`: PASS.
- Playwright QA used local dev server at `http://127.0.0.1:4176`.
- API routes were intercepted during browser QA to avoid creating tracking/database rows.

