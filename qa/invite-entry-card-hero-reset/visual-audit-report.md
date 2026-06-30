# CEOS Homecoming Invite Entry QA

## Scope

- Branch: `hotfix/invite-entry-card-hero-reset`
- URL basis: local dev server with Playwright emulation
- Invite test URL: `/?share=next-node&invite=SDWQA1`
- Normal test URL: `/?share=next-node`
- API writes were intercepted for QA; no production user data was modified.

## Viewports

- Mobile: 390 x 844
- Desktop: 1440 x 900

## QA Results

| Check | Result | Notes |
| --- | --- | --- |
| Invite overlay visual | PASS | Card-style overlay uses Private Invitation visual language. |
| Invite CTA copy | PASS | Button text is `NEXT NODE 입장하기`. |
| Hero paused while overlay is active | PASS | Video stayed paused at `0.000s` during overlay wait. |
| Hero restarts after invite continue | PASS | Video started at `0.665s` mobile and `0.698s` desktop after click wait. |
| Normal link no overlay | PASS | `?share=next-node` showed no invite overlay. |
| Referral autofill | PASS | Application modal included `서다원` referral display. |
| Mobile overflow | PASS | Overlay fits within 390 x 844 viewport. |

## Measured Values

```json
{
  "mobile": {
    "heroPaused": "true",
    "afterWait": { "currentTime": 0, "paused": true },
    "afterClick": { "currentTime": 0.665, "paused": false }
  },
  "desktop": {
    "heroPaused": "true",
    "afterWait": { "currentTime": 0, "paused": true },
    "afterClick": { "currentTime": 0.698, "paused": false }
  },
  "normal": {
    "overlayCount": 0,
    "videoState": { "currentTime": 1.698, "paused": false }
  }
}
```

## Captures

- `invite-overlay-mobile-390.png`
- `invite-overlay-desktop-1440.png`
- `invite-overlay-card-closeup-mobile-390.png`
- `invite-overlay-card-closeup-desktop-1440.png`
- `hero-after-entry-mobile-390.png`
- `hero-after-entry-desktop-1440.png`
- `application-modal-invited-mobile-390.png`
- `application-modal-invited-desktop-1440.png`
- `normal-landing-no-invite-mobile-390.png`
- `contact-sheet-invite-entry-card-hero-reset.png`
