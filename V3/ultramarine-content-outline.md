# Ultramarine Website — Content Source Doc

This document is the single source of truth for the website's copy. When making edits with Claude Code (or Claude in chat), point it at this doc and say "update the site to match this."

---

## INSTRUCTIONS FOR CLAUDE — read this first

- This document is the final source for site **copy** (words), not layout, colors, or structure.
- Update the HTML content to match the text in this doc exactly. Do not paraphrase or "improve" wording unless asked.
- Do **not** change layout, colors, spacing, animations, or component structure unless a change is explicitly requested outside this doc. This doc governs text only.
- Anything inside `[ ]` brackets is still a placeholder — flag it back to the person instead of inventing content for it.
- If a section below is left blank, leave the current placeholder text in the HTML untouched rather than guessing.
- Do not touch the email address, links, or copyright line unless explicitly told to.

---

## STATUS (as of 2026-08-12)

The site was reset to placeholder copy across every section so the real content can be dropped in later. Every `[ ]` bracket below is a slot waiting for actual text — none of it is final. The client's brief for the main nav sections is: **bio/about me, services, and logos of partner orgs.** The nav and sections were restructured to match:

- **Old nav:** About · Approach · Principles · Contact
- **New nav:** About · Services · Partners · Contact
- The **Principles** section was removed entirely (it wasn't part of the client's request). If the client wants a values/principles section later, it can be re-added as its own section.
- A new **Partners** section was added: a heading, an intro line, and a grid of 6 placeholder logo boxes to swap for real partner logos.
- Contact was kept (not explicitly requested by the client, but assumed necessary) — flag with the client if it should be dropped or folded into the footer instead.
- Site-wide font switched to **Proxima Nova** (including the `ultramarine` wordmark, which had briefly been set in a serif). See Typography note in section 1.
- The gold "sun" circle accent in the nav was removed — it read as out of place next to the wave.
- Partners section expanded from 6 generic slots to the 9 real partner names below, each wired to auto-load a logo file from a new `logos/` folder — see section 5 for the file-drop workflow.

---

## 1. Nav

Wordmark: `ultramarine` (sans-serif, same font stack as the rest of the site — see Typography note below)

Nav links (in order):
- About
- Services
- Partners
- Contact

*(Change link labels or add/remove links here if needed.)*

**Visual style:** Nav background is cream (`--neutral`), with a two-tone wave divider (sky blue over ultramarine) along the bottom edge, styled to echo the reference image `header.png`. (The gold "sun" circle from that reference was tried and then removed — it looked out of place.)

**Typography:** Site-wide font is `'Proxima Nova', 'Inter', sans-serif`. Proxima Nova is a licensed font (Adobe Fonts/Fonts.com) and isn't available on Google Fonts, so it's named first in the stack but currently renders as Inter (already loaded, a close visual match) until a licensed embed is added. If a Fonts kit or font files become available, wire those in to upgrade every heading, body copy, and the wordmark to real Proxima Nova automatically.

---

## 2. Hero

**Eyebrow label:** `[Your tagline / industry]`

**Headline:**
`[Headline — what you help clients achieve]`.
*(the highlighted word/phrase — currently "achieve" — is the `<mark>` highlight in the design; keep it short, 1–2 words)*

**Subheading / lede:**
`[One or two sentences describing who you work with and the outcome you help them reach.]`

**Primary button text:** Let's talk
**Secondary link text:** See how I work →

---

## 3. About

**Section heading:** Hi, I'm `[Your name]`.

**Pull quote:**
"`[A short, punchy quote that captures your philosophy or approach.]`"

**Bio paragraph 1:**
`[Two or three sentences about your background, expertise, and what makes your perspective valuable. Mention relevant experience, credentials, or history.]`

**Bio paragraph 2:**
`[One sentence describing the gap your business fills for clients.]`

**Signature line:** `[Location]` — `[who you work with, e.g. "working with clients nationwide"]`.

**Photo:** `[ photo ]`

---

## 4. Services

**Section heading:** Services
**Subheading:** `[A sentence describing the different ways clients typically work with you.]`

**Card 1**
- Label: `[Label 1]`
- Title: `[Service 1 name]`
- Description: `[One or two sentences describing this service and the outcome it delivers.]`

**Card 2**
- Label: `[Label 2]`
- Title: `[Service 2 name]`
- Description: `[One or two sentences describing this service and the outcome it delivers.]`

**Card 3**
- Label: `[Label 3]`
- Title: `[Service 3 name]`
- Description: `[One or two sentences describing this service and the outcome it delivers.]`

*(Currently 3 cards to match the existing layout. Say the word if the real offering needs more or fewer.)*

---

## 5. Partners

**Section heading:** Partners
**Subheading:** `[A sentence introducing the organizations you've worked with or partnered with.]`

**Logos:** 9 slots, one per named partner below. Each slot is coded to look for a specific file in the `logos/` folder — **drop a matching image in and it appears automatically, no code edit needed.** If the file isn't there yet, the partner's name shows as text instead (no broken-image icon).

| Partner | Expected file |
|---|---|
| Chan Zuckerberg Initiative | `logos/chan-zuckerberg-initiative.png` |
| Center for Houston's Future | `logos/center-for-houstons-future.png` |
| Prime Coalition | `logos/prime-coalition.png` |
| Global Industry Hub | `logos/global-industry-hub.png` |
| Deploy Action | `logos/deploy-action.png` |
| Industrious Labs | `logos/industrious-labs.png` |
| Stanford University | `logos/stanford-university.png` |
| CEA Consulting | `logos/cea-consulting.png` |
| OpenMinds | `logos/openminds.png` |

**How to add a logo:** save the company's logo image using the exact filename above (PNG or SVG, ideally with a transparent background) and put it in the `logos/` folder next to `V2.html`. Reload the page — the placeholder text is replaced by the image automatically. Logos render in grayscale and go full-color on hover, matching the rest of the site's hover treatment.

**To add or rename a partner:** tell Claude Code the new list and it'll update both the HTML slots and this table together.

---

## 6. Contact / CTA

**Eyebrow label:** Start a conversation
**Headline:** `[A one-line call to action inviting people to reach out.]`
**Button:** `[you@yourdomain.com]` *(mailto link — replace with the real address before launch)*
**Supporting note:** `[Response time note, e.g. "Usually replies within 2 business days."]`

---

## 7. Footer

Wordmark: ultramarine
Links: About · Services · Partners · Contact
Copyright line: © 2026 Ultramarine Consulting. All rights reserved.

---

## 8. Assets

- `Icon.png` — site favicon (linked in `<head>` as `icon` and `apple-touch-icon`).
- `logos/` — folder for partner logo images. See section 5 for exact filenames expected.
- `header.png` — reference image only, not embedded on the page. Its cream field and sky-over-ultramarine wave were used as the style reference for the nav bar redesign noted in section 1. Its serif wordmark and gold sun were tried and then dropped in favor of a sans-serif wordmark (see Typography note) and no sun accent.

---

## Open questions for [friend's name]

- [ ] Real name and headline/tagline for the hero and About section
- [ ] Real photo
- [ ] Real bio copy (background, credentials, what makes your approach different)
- [ ] The 3 services: names + descriptions (confirm 3 is the right number)
- [ ] The 9 partner logo image files themselves (names and filenames are already set up — see section 5)
- [ ] Confirm the contact email
- [ ] Confirm Contact should stay as its own section (it wasn't in the original 3-tab brief)
- [ ] Any other sections to add (e.g. testimonials, case studies, a resources/writing section)?
