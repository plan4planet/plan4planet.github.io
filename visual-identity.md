# Plan4Planet visual identity

Use this when you make anything that carries the Plan4Planet name: a slide, a poster, a social card, a document, a web page. It is short on purpose. The names, the wordmark rule, the colours and the two fonts are the whole identity. Everything else here is habit.

Handing the job to an AI agent? Paste this file into the prompt. The HTML templates and the render script that produced the poster, the share card and the speaker cards are in the Assets folder under Comms / Branding in the Plan4Planet shared drive (kit subfolder); they render with headless Chrome. Ask the agent to keep every rule here and to ask before adding a colour, a font or a decoration.

## Names

- Plan4Planet is the community. One word, numeral 4, capital P twice. Never "Plan 4 Planet", "Plan-4-Planet" or "Plan for Planet".
- Planning for a Better Planet is the event. The full event name is "Planning for a Better Planet, AAAI Fall Symposium 2026", with the AAAI words in that order.
- Tagline: "AI planning for climate decisions." With the full stop, except in the browser and search-result title of the site, where it is set without it (the tagline key in _config.yml).
- Positioning line: "Verifiable climate decisions, not hallucinated ones." and "Without a data center's energy footprint." It carries the two selling points: these methods can be verified, and they do not need a data center's worth of electricity to run. It sits under the tagline. Set it on two lines where there is room, as in the email signature, and run the two sentences together on one line where there is not.
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
- Email signature (assets/identity/email-signature.html): green rule, wordmark, then the tagline in Source Sans 600 navy, then the two positioning lines in ink soft, then the links. The navy tagline is deliberate here, because the signature needs a middle step of hierarchy once the event name comes out of it.

## Google Slides

The reference deck is the symposium welcome deck, assets/slides/plan4planet-welcome.pdf. New decks should look like it. Sizes below are in points for the default Google Slides page (Widescreen 16:9, 10 x 5.625 in, 720 x 405 pt).

- Fonts: pick Work Sans and Source Sans 3 from More fonts. Set them once in Slide > Edit theme, so every layout uses them.
- Margins: 48 pt on every side. Nothing but the cover bar and full-bleed backgrounds goes past them.
- Backgrounds: light slides use #f7f9fb (a slightly cooler paper that projects better than #fdfdfd). One navy (#003973) statement slide per section at most. That is the only place body text sits on a colour.

| Element | Font | Size | Colour |
|---|---|---|---|
| Kicker (one short line above the title, typed in capitals) | Source Sans 3 Bold | 12 pt | green #3f8a46 on light, light green #a9d6ae on navy |
| Cover title | Work Sans Bold | 42 pt | navy |
| Statement title (navy slide) | Work Sans Bold | 36 pt | paper #fdfdfd |
| Slide title | Work Sans Bold | 28 pt | navy |
| Card title | Work Sans Bold | 15 pt | navy |
| Lead text, statements | Source Sans 3 Regular | 16 pt | ink soft on light, #d4e2ef on navy |
| Card text and bullets | Source Sans 3 Regular | 11 to 12 pt, never under 10 | ink soft |
| Card label (day, step, category) | Source Sans 3 Bold, capitals | 10 pt | steel blue |

The kicker is the slide's one green label, which keeps green within the accent rule above. Google Slides has no letter-spacing control, so type kickers and labels in capitals and leave the spacing at default.

Layouts to build in the theme (Slide > Edit theme):

1. Cover: light background, a 12 pt navy bar down the full left edge, kicker, cover title, a line of facts (dates, place, room) in lead text, and the tree logo large on the right. On event decks the AAAI Symposium Series logo sits under the facts.
2. Statement: navy background, kicker, statement title, one short paragraph. No logo.
3. Title and body: kicker and slide title stacked at the top left, body below.
4. Cards: kicker and title, then two to four cards in a row. Each card: paper fill, 0.5 pt rule-colour border (#c9d6e3), a 3 pt top border in navy, steel blue or green (in that order when cards stand for a sequence), corners rounded about 6 pt, 15 pt inner padding.
5. Section break: same as Statement, title only.

Habits: one idea per slide. Titles name the topic in the same grammar throughout. Speaker notes carry the script, not the slide. No slide numbers on the cover. No clip art, no stock icons beyond Google Slides' own simple shapes, no slide transitions other than fade.

## Google Docs

For memos, plans, handouts and anything shared in the Plan4Planet shared drive. The Community Directory Doc follows the same palette.

- Page: Letter, 1 in margins, or Pageless for documents that are read on screen only.
- Set the styles once, then Format > Paragraph styles > Options > Save as my default styles, so new documents start with them.

| Style | Font | Size | Colour | Spacing |
|---|---|---|---|---|
| Title | Work Sans Bold | 26 pt | navy | 0 before, 4 after |
| Subtitle | Source Sans 3 Regular | 13 pt | ink soft #3d4a57 | 0 before, 16 after |
| Heading 1 | Work Sans Bold | 18 pt | navy | 20 before, 6 after |
| Heading 2 | Work Sans Bold | 14 pt | navy | 16 before, 4 after |
| Heading 3 | Source Sans 3 Bold | 12 pt | steel blue #2f6690 | 12 before, 4 after |
| Normal text | Source Sans 3 Regular | 11 pt | ink #14212e | line spacing 1.15, 6 after |

- Links: steel blue #2f6690, underlined (the Google Docs default blue is not ours).
- Tables: header row filled with surface #e9f0f6 and set in Source Sans 3 Bold; borders 0.5 pt in rule #c9d6e3; cell padding 5 pt.
- Callouts: a one-cell table filled with surface 2 #f1f5f9, no border, or a 3 pt left border in navy for a note that must be seen.
- Header: the tree logo about 0.4 in tall beside the wordmark, on the first page only (Different first page). Footer: plan4planet.org on the left, the page number on the right, Source Sans 3 9 pt, ink soft.
- Kickers work the same way as in Slides: typed in capitals, Source Sans 3 Bold 10 pt, steel blue, above the title. Docs has no letter spacing either.
- Green appears only in the wordmark's 4 and, at most, one small label. Never as heading colour or table fill.

## Writing

- Plain, direct, short sentences. No em dashes. No bold or italics inside copy that will be pasted elsewhere.
- Say what something is. Avoid "cutting-edge", "transformative", "seamless", "leverage", "empower" and the rest of the stock vocabulary.

## Files

- Wordmark, poster and transparent logo: assets/identity in this repository. The poster is poster-1080x1350.png (for feeds) and poster-letter.pdf (for email and print).
- Link-preview image for the site: assets/images/plan4planet_share.png, 1200 x 628.
- Colours and fonts as code: _sass/_tokens.scss.
- Avatars, banners, favicons, speaker cards, and the templates and render script that produce all of the above: the Assets folder under Comms / Branding in the Plan4Planet shared drive.
