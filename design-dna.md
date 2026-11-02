# Creations of the Ill Minded design DNA

Read this before any UI work on creationsoftheillminded.com. Of all the owner's sites this one is closest to having its own voice: square corners, a real print-study artwork on the cover, a zine-like index. What gives it away is the type (Space Grotesk + Space Mono, the most common "edgy" AI pairing) and a few copy habits.

Public-site rule: no fundraising or token-sale language anywhere (securities counsel has not cleared it). Keep "no money is being raised" true and visible.

## Audit, 2026-11-02 (live = `gh-pages` `67c7716`; `main` is `68e0920`)

**Score: 6/10 for looking like a default AI build.**

| Tell | Where (gh-pages `index.html`) |
|---|---|
| Space Grotesk + Space Mono from Google Fonts | line 2 (`<link>`), line 3 (`body{font-family:'Space Grotesk'}`) |
| Uppercase 11 px mono labels on everything (`.mono`) | line 3 (`.mono{font:11px 'Space Mono';text-transform:uppercase}`), line 40, 43, 47 |
| List of three in the cover kicker: "Companies. Software. Clothing. Built in public." | line 40 |
| Fragment couplet as the founder headline: "It starts with mine. It doesn't end there." | line 46 |
| Feature + pair + index: the three-tier "portfolio" structure every AI portfolio page uses | lines 43-47 |

Good and worth keeping: the blue/yellow print study as the cover, 0 px corners, 2 px ink rules, the filterable archive, and the yellow running header.

## What Ill Minded is made of

An open holding company that builds in public, presented as a **publication**: an issue, a contents page, dispatches from the founder. The material is **risograph and screen print**: two spot inks, misregistration, paper tooth, a stapled spine. The current cover artwork is exactly this and is the brand's source.

## References (human-made)

1. ***Emigre* magazine** (Zuzana Licko, Rudy VanderLans). A type foundry and a publication in one; the precedent for "a studio that publishes itself".
2. **Experimental Jetset** (experimentaljetset.nl). Strict grids, plain language, conviction.
3. **Hato Press** (London riso studio). Two-ink printing and its accidents.
4. ***Bloomberg Businessweek* under Richard Turley (2010–14)**. Business content treated with editorial nerve.
5. **Colors magazine** (Tibor Kalman era). A company that speaks through an editorial voice.

## Type

**ABC Arizona, Dinamo.** A variable family that moves from sans to serif ("Flare" in between): one family, many voices, which suits a holding company of very different companies. Use Arizona Sans for running text, Arizona Flare for headlines, Arizona Serif for dispatches from the founder. For the small labels, use Arizona Sans at text size in sentence case instead of a mono.

- Licence: Dinamo prices by company size and licence type; select "<3" people, desktop + web, at abcdinamo.com/buy/arizona for the quote. **Not priced in this audit; get the quote and the owner's approval before buying.**
- Until approved: system sans for text, `Georgia` for headlines. Not Space Grotesk, Space Mono, or another Google pairing.

## Palette (from the print-study cover; keep it)

The current tokens were sampled from a real artwork, so they stay. Name them by the inks.

| Token | Hex | Source | Use |
|---|---|---|---|
| `--riso-blue` | `#103BE8` | blue ink in the print study | cover, dispatch band |
| `--riso-yellow` | `#EFFF49` | yellow ink | header, contact band, highlights |
| `--ink` | `#11120E` | black gesture ink | text, rules |
| `--paper` | `#F7F8F2` | uncoated paper | background |
| `--focus` | `#FF5839` | keep for focus rings only | accessibility |

Rule: two inks per spread, like a riso run. A section uses blue or yellow with ink, never both plus a third colour.

## Grid and spacing

- Keep the publication grid: 32 px page margin, `1fr 3fr` statement split, 2 px ink rules between sections.
- 12-column grid, 26 px gutters. 5 px base (current spacing is 5-based: 15/20/25/35/50/60); keep it.
- Corners 0. Shadows none. Misregistration (a 2–3 px offset second ink) is allowed on display type as a print effect, sparingly.

## Copy

- Write as an editor's note, first person, specific: names, dates, numbers.
- Banned: lists of three ("Companies. Software. Clothing."), fragment couplets ("It starts with mine. It doesn't end there."), "not X but Y", "seamless", "elevate", anything that sounds like an offer to invest.

## Banned defaults

- Space Grotesk, Space Mono, Inter, Geist, JetBrains Mono, any Google Font chosen by default.
- Uppercase mono labels as the default label style.
- Pill badges, rounded cards, soft shadows, gradients.
- Centred hero.
- Emoji, lucide icons.
- Fundraising, token or "invest" language.

## Pre-ship checklist

- [ ] No banned font; labels in sentence case.
- [ ] Each section uses at most two inks from the table.
- [ ] The cover is a real artwork (the print study or a new real print), never AI-generated.
- [ ] Copy has no triplets, no fragment couplets, no investment language; "no money is being raised" is still on the page.
- [ ] Squint test with the logo covered: does it look like an issue of a magazine or a portfolio template? Fix until it is the magazine.
- [ ] Supreme director review by an independent reviewer against this file; fix before shipping.
