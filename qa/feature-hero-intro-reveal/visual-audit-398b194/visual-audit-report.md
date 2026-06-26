# CEOS Homecoming 2026 Visual Audit Pack

Capture set: `visual-audit-398b194`  
Source branch: `feature/hero-intro-reveal`  
Source app commit: `971683f192ae91f48e04e0f7359385f44fda3e71`  
Capture basis: local current screenshot set copied from the same source commit, plus generated crops/contact sheets  
Device basis: Playwright-style viewport screenshots, not a physical iPhone  
Primary mobile viewports: `390x844`, `430x932`  
Desktop viewport: `1440x900`

## Purpose

This pack is for visual alignment before additional UX copy or layout revisions. The application source, UI copy, CSS, and behavior were not modified for this audit pack. Only QA images, contact sheets, and this report were added.

## Contact Sheets

- `contact-sheet-mobile-flow.png`: mobile 390 flow overview with full-page and major section captures.
- `contact-sheet-modal-flow.png`: Wanted empty state, People Graph loading/result/error, and application modal states.
- `contact-sheet-desktop.png`: desktop full-page, Tickets, and LOOKING FOR captures.
- `contact-sheet-all.png`: index sheet of all individual captures and detail crops.

## Individual Captures

### Mobile full-page

- `full-mobile-390.png`
- `full-mobile-430.png`

### Mobile section captures

- `wanted-section-390.png`
- `why-next-node-390.png`
- `looking-for-390.png`
- `featured-nodes-390.png`
- `timetable-390.png`
- `tickets-390.png`
- `faq-final-390.png`

### Wanted / People Graph states

- `wanted-empty-warning-390.png`
- `people-graph-loading-390.png`
- `people-graph-result-390.png`
- `people-graph-result-error-390.png`

### Application modal

- `application-modal-390.png`
- `application-modal-430.png`
- `application-modal-validation-390.png`

### Desktop

- `full-desktop-1440.png`
- `tickets-desktop-1440.png`
- `looking-for-desktop-1440.png`

### Additional detail captures

- `looking-for-card-detail-390.png`
- `tickets-card-detail-390.png`
- `why-centered-check-390.png`
- `section-transition-mobile-390.png`
- `floating-cta-state-390.png`

## Current State Observations

### Wanted

Well-working visual state:

- The Wanted section is very minimal and focused. The bridge copy, headline, input, and primary button are the dominant elements.
- The black-navy background helps the section feel like a focused entry point after the cinematic hero.
- The CTA color is clear and visually prominent without introducing an extra application CTA in the early funnel.

Potentially awkward visual state:

- The Korean headline line break reads cleanly overall, but the section is visually sparse enough that any small copy or spacing imbalance becomes noticeable.
- The bottom `NEXT` cue is present, but it is quiet. It reads as a secondary navigation hint rather than a major action.
- In the empty warning state, the red helper text is visible and does not collide with the input or button.

### Wanted Journey / People Graph

Well-working visual state:

- The People Graph loading modal has a strong central scanning-device feel. The 3D assets are arranged clearly and the loading text is centered.
- The result state uses `85%` as a visual anchor. The copy is framed as request clarity rather than a guaranteed person match.
- The result error state shows the invalid contact field in red, and the error message is close enough to the field to be understood.

Potentially awkward visual state:

- On result screens, the large `85%` is highly dominant. It creates a strong sense of numerical certainty even though the surrounding copy is cautious.
- The contact form fields in the result modal feel compact and slightly dense on mobile, but they remain readable.
- The loading state uses a large amount of dark empty space above and below the modal, which supports the premium tone but may also make the state feel quiet.

### Why Next Node

Well-working visual state:

- The section reads as a philosophical bridge and is centered around text hierarchy rather than cards.
- The event info card at the bottom gives the section a grounded, factual endpoint.
- The blue/purple highlight inside the sentence is restrained and helps mark the key idea.

Potentially awkward visual state:

- The long Korean paragraphs create multiple large line blocks on mobile. They are readable, but the section feels text-heavy compared with Wanted.
- The lower `NEXT` cue sits after a long text and card composition. It is visible, but not visually loud.
- The background transition from Wanted into Why remains very dark, so the section change is more tonal than dramatic.

### LOOKING FOR

Well-working visual state:

- The dossier / confidential file mood is distinct and visually memorable.
- Mobile cards are compact and use the `WANTED NODE / CONFIDENTIAL / LOOKING FOR` structure consistently.
- The black/redacted silhouette is preserved and reinforces the private, classified tone.
- The lower fade-out suggests more cards continue beyond the visible set.

Potentially awkward visual state:

- The first two rows are readable, but the lower cards fade/crop heavily. This reads as intentional continuation, but it could also be interpreted as content being cut off.
- The card board still has a structured two-column rhythm in places, even though rotation and offsets help.
- The opening headline is strong, but it occupies a lot of height before the card board begins.

### Featured Nodes

Well-working visual state:

- The section uses stacked profile-like cards with a consistent dark glass tone.
- Purple circular marks give the list a repeatable identity without becoming too decorative.
- The copy reads like curated people categories rather than guaranteed matches.

Potentially awkward visual state:

- The section is visually calmer than LOOKING FOR, so the transition from dossier cards into profile list feels like a drop in visual energy.
- The repeated card structure is readable but list-like. It is less cinematic than the previous section.
- Some card text is small in the full-page context, though the section capture remains legible.

### Timetable

Well-working visual state:

- The timetable section clearly presents event order and timing.
- The dark cards and thin dividers preserve the black-navy premium tone.
- The MC / host placeholder area at the bottom is visually separated from the main schedule.

Potentially awkward visual state:

- The timetable is long on mobile. It is understandable, but it takes more scroll time than the more atmospheric sections.
- The first descriptive cards above the schedule add context, but they also lengthen the section before the time list begins.
- The bottom visual cards are dark and subtle, so they may read as placeholders rather than strong content.

### Tickets

Well-working visual state:

- The timer and price cards are highly legible and provide a clear conversion zone.
- The Earlybird card stands out through the cyan border and gradient CTA.
- The three pass hierarchy is clear: Earlybird, Priority, General / Invitation.
- The `선착순 15명 · 6월 28일 마감` and `선착순 40명` badges are visible.

Potentially awkward visual state:

- The section is one of the longest mobile sections because the three ticket cards stack vertically.
- The timer block adds urgency, but it also pushes the first card lower.
- The floating CTA can appear during/after this section, adding another fixed conversion element near the bottom of the viewport.

### FAQ / Final

Well-working visual state:

- FAQ cards are compact and readable.
- The final CTA repeats the event identity and applies the cyan-to-purple CTA treatment.
- The section stays within the overall black/deep-navy tone.

Potentially awkward visual state:

- The FAQ block is functional and quiet. It does not carry the same cinematic intensity as Hero or LOOKING FOR.
- The final CTA appears after a long mobile journey, so its impact depends on user persistence through Tickets and FAQ.
- The floating CTA at the bottom may visually compete with final CTA buttons when both are visible.

### Application Modal

Well-working visual state:

- The modal uses a deep glassy navy panel and matches the landing tone.
- Fields are stacked cleanly for mobile and remain accessible in the long modal captures.
- Validation state clearly marks invalid email and phone examples.
- The pass selector and agreement checkbox are visible before the final submit button.

Potentially awkward visual state:

- The modal is field-heavy. It fits in a long capture, but users must scroll inside the modal on real mobile screens.
- Helper copy and multiple multi-line fields make the form feel more serious than lightweight.
- The validation messages are clear, but the red text adds visual density in the already compact modal.

### Floating CTA

Well-working visual state:

- The floating CTA is not present in the early Hero/Wanted/Why screenshots.
- It appears later in the journey where conversion intent is more appropriate.
- The bottom bar has a compact dark treatment and the CTA button remains high contrast.

Potentially awkward visual state:

- In long content sections, the fixed bottom CTA can cover a small portion of lower content.
- It is useful for conversion, but it adds persistent visual weight in the lower viewport.
- In final CTA territory, the floating CTA and page CTA may feel duplicative.

### Desktop Layout

Well-working visual state:

- The desktop captures preserve the wide cinematic dark tone.
- Tickets appear as a 3-column pricing layout and are easy to compare.
- Desktop LOOKING FOR uses a broader dossier spread, which reads more like a board than a vertical mobile list.

Potentially awkward visual state:

- The desktop full-page capture shows large vertical breathing room in some sections, which supports premium mood but can make the page feel long.
- The desktop LOOKING FOR section is visually stronger than the mobile section because the card spread has more lateral room.
- Desktop section rhythm is generally smoother than mobile because stacking pressure is lower.

## Background / Section Tone Observations

- The overall visual identity is now very dark: black navy, deep blue, and muted purple dominate.
- Section transitions are subtle rather than high-contrast. This helps the page feel cohesive, but it can also make section boundaries quiet.
- Tickets still use a dark background rather than a light section, so pricing remains integrated with the private-event mood.
- The strongest visual contrast points are Hero title, Wanted CTA, People Graph `85%`, Ticket price cards, and final CTA.

## Capture / Access Notes

- Vercel branch alias may still be protected by Vercel SSO. Vercel public paths are included for completeness but may require authentication.
- GitHub raw links from the public audit-assets repository should be the most reliable visual access path.
- Contact sheets exist specifically to reduce reliance on many individual image fetches.
