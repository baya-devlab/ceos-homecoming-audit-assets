# Visual Audit Report

## Scope

This package verifies the targeted rollback of only the five extra `/nodes` profiles added in PR #5.

Removed profiles:

- 서강대학교 CS/프로덕트 학생
- 수노앤컴퍼니 Product Engineer
- 이화여자대학교 브랜드/커뮤니티 학생
- 숨고 Product Designer
- 홍익대학교 UX/UI 디자인 학생

Removed runtime image assets:

- `/images/homecoming/nodes/node-photo-09.jpeg`
- `/images/homecoming/nodes/node-photo-10.jpeg`
- `/images/homecoming/nodes/node-photo-11.jpeg`
- `/images/homecoming/nodes/node-photo-12.jpeg`
- `/images/homecoming/nodes/node-photo-13.jpeg`

## Verification Summary

| Requirement | Result | Notes |
|---|---|---|
| New five profiles removed | PASS | No new five affiliations/roles/photo refs remain |
| New five AI image assets removed | PASS | `node-photo-09.jpeg` through `node-photo-13.jpeg` deleted |
| Existing 10 profiles preserved | PASS | NODE N•001-N•010 source mapping matches pre-expansion data |
| Existing photo/placeholder mapping preserved | PASS | 8 photo cards + 2 confidential placeholders restored |
| TBD cards restored | PASS | NODE N•011-N•015 return to TBD cards |
| Landing Featured Nodes preserved | PASS | Featured set remains NODE N•001, N•002, N•007, N•010 |
| `/nodes` mobile 390 | PASS | No horizontal overflow |
| `/nodes` mobile 430 | PASS | No horizontal overflow |
| `/nodes` desktop 1440 | PASS | No horizontal overflow |
| Image loading | PASS | Existing profile image URLs return image responses |
| `/nodes` fade-out | PASS | Last card tail fade class remains |
| DB/tracking/API untouched | PASS | No API/tracking/DB files changed |
| OG/share link untouched | PASS | No OG/meta/share URL files changed |

## Capture Method

- Source: local dev server
- Tooling: Playwright using system Chrome
- API handling: `/api/**` requests intercepted with 204 responses
- Device note: browser emulation, not physical iPhone/Safari

## Evidence

Automated result details are in `qa-results.json`.
