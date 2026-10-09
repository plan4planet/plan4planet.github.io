# Plan4Planet visual identity

Use this when you make anything that carries the Plan4Planet name: a slide, a poster, a social card, a document, a web page. It is short on purpose. The names, the wordmark rule, the colours and the two fonts are the whole identity. Everything else here is habit.

Handing the job to an AI agent? Paste this file into the prompt. The HTML templates and the render script that produced the poster, the share card and the speaker cards are in the Assets folder under Comms / Branding in the Plan4Planet shared drive (kit subfolder); they render with headless Chrome. Ask the agent to keep every rule here and to ask before adding a colour, a font or a decoration.

## Names

- Plan4Planet is the community. One word, numeral 4, capital P twice. Never "Plan 4 Planet", "Plan-4-Planet" or "Plan for Planet".
- Planning for a Better Planet is the event. The full event name is "Planning for a Better Planet, AAAI Fall Symposium 2026", with the AAAI words in that order.
- Tagline: "AI planning for climate decisions." With the full stop.
- Facts to carry verbatim: November 5 to 7, 2026. Westin Arlington, Arlington, Virginia. plan4planet.org.

## Wordmark

The wordmark is the word Plan4Planet set in Work Sans Bold, navy, with the 4 in the accent green. That is the whole rule. On a navy or dark background the letters go white and the 4 stays green. Never set the 4 in navy, never set the whole word in green, never add a gradient, outline or shadow. The wordmark can stand alone without the logo.

Files in this repository, under assets/identity: wordmark-navy.svg (vector, any size), wordmark-reverse.svg (white, for dark backgrounds), wordmark-navy-2400.png and wordmark-reverse-2400.png (transparent), wordmark-tagline-2400.png (with the tagline).

## Logo

The tree. Use assets/identity/plan4planet-logo-transparent.png on light backgrounds and assets/images/plan4planet.png where transparency is a problem. Keep clear space around it of at least a quarter of its width. Do not recolour, crop, rotate, stretch or put it on a navy background. It sits beside or above the wordmark, never inside the letters.

## Colours

| Name | Hex | Use |
|---|---|---|
| brand (navy) | #003973 | headings, the wordmark, buttons, the thick rule at the top of a page or card |
| brand strong | #002a55 | hover states |
| secondary (steel blue) | #2f6690 | kickers, links, secondary headings, initials badges |
| accent (leaf green) | #3f8a46 | the 4 in the wordmark, small icons and dots, one label at most. Never large areas, never body text |
| ink | #14212e | body text |
| ink soft | #3d4a57 | bios, notes, affiliations, taglines |
| muted | #9aa5b1 | pending or disabled things |
| paper | #fdfdfd | page and card background |
| surface | #e9f0f6 | tinted panels, the registration band on the poster |
| surface 2 | #f1f5f9 | callout boxes |
| rule | #c9d6e3 | borders and thin rules |

Green is the accent and nothing else. If a design has more green than navy, it is wrong. The same values live as code in _sass/_tokens.scss.

## Type

- Work Sans, weight 700, for the wordmark, titles and headings. Tight letter spacing (about -0.015em on large sizes). Nothing else is set in Work Sans.
- Source Sans 3 for everything else: 400 for body text, 600 for names, labels, buttons and facts, 700 only for bold inside body text.
- Both are free Google Fonts and both are in the Google Docs and Google Slides font menus.
- Fallback stack when the fonts cannot load (email, old devices): Segoe UI, Roboto, Helvetica, Arial.
- Kickers (the small line above a title, such as "AAAI Fall Symposium 2026") are Source Sans 600, uppercase, letter spacing 0.14em, steel blue.

## Layout habits

- Paper background, a thick navy rule along the top edge, generous margins (about 8 percent of the width).
- One title in Work Sans, the tagline under it in Source Sans, facts in Source Sans 600 navy with a small green dot before each.
- Tinted surface panels for the call to action, never coloured backgrounds behind body text.
- No gradients, no drop shadows beyond the light card shadow (0 2px 6px rgba(0,57,115,0.12)), no rounded corners beyond 4 to 6 px.
- The AAAI logo appears full colour, unrecoloured, with clear space, only on event material, never altered.

## Writing

- Plain, direct, short sentences. No em dashes. No bold or italics inside copy that will be pasted elsewhere.
- Say what something is. Avoid "cutting-edge", "transformative", "seamless", "leverage", "empower" and the rest of the stock vocabulary.

## Files

- Wordmark, poster and transparent logo: assets/identity in this repository. The poster is poster-1080x1350.png (for feeds) and poster-letter.pdf (for email and print).
- Link-preview image for the site: assets/images/plan4planet_share.png, 1200 x 628.
- Colours and fonts as code: _sass/_tokens.scss.
- Avatars, banners, favicons, speaker cards, and the templates and render script that produce all of the above: the Assets folder under Comms / Branding in the Plan4Planet shared drive.
