# $ILLMINDED landing page — handoff

Built 2026-09-09 in Cowork. Page lives at `illminded/index.html`, so the public URL is
`creationsoftheillminded.com/illminded/`. Self contained HTML, no build step.

Decisions made 2026-09-09:

- `publication-refined.html` was promoted to `index.html`. The site root is now the Field Notes
  design. The Barlow version stays as `index.barlow-rejected.20260907.bak.html`.
- The design comparison nav in the footer was removed from the root copy, since it pointed at the
  two candidate designs and does not belong on a live homepage.
- The token page is **live but unlinked** until the coin launches. No nav link, no collection
  strip entry, no contents row. It works if you share the URL.

## Blanks to fill before launch

Search `illminded/index.html` for `class="tbd"` and `data-tbd`:

| Placeholder | Where | Needs |
| --- | --- | --- |
| Total supply | Section 02, spec list | Final number |
| Contract address | Section 02, spec list | Address at deploy |
| Launch date | Section 02, spec list | Date |
| Non founder breakdown | Section 02, allocation table | LP / community / treasury split |
| Market cap threshold | Section 03, Rule 01 | The number founder tokens unlock above |
| Vesting schedule | Section 03, Rule 02 | Cliff and release cadence |
| Discord invite | Section 04, `data-tbd="discord-invite"` | Invite URL on the `.cta` href |

Also at launch: swap the `Band` entry in the spec strip under the cover for the real contract
address, and add the page to the running strip and contents index on the homepage.

## Brand system pulled in 2026-09-09

Exported from the Claude Design project "Creations of the Ill Minded brand system"
(project 0fdf9191-8bcd-41b3-8ed7-c77f3aefdfde).

| File | What it is |
| --- | --- |
| `assets/brand/brand-board.dc.html` | The full brand board as exported. Master mark, icon and one color, wordmark lockups, department patches, the $ILLMINDED coin, merch, favicon and avatar, tokens. |
| `assets/brand/illminded-roundel.svg` | The mech brain roundel on its own, template values resolved. |
| `assets/brand/marks-sprite.svg` | Hidden sprite with brain-full, brain-coin, brain-icon, mk-full, mk-icon for reuse. |

Tokens: paper `#F7F8F2`, ink `#11120E`, electric blue `#103BE8`, acid yellow `#EFFF49`,
accent red `#D32011`. Space Grotesk 700 headlines, Space Mono 700 labels.

The roundel is inlined in the page rather than linked, because the arc type and the ribbon need
Space Mono to load and an external SVG in an `img` tag cannot pull webfonts.

**The band legend `0X1LLM1ND3D` is artwork, not an address.** Leave the roundel art alone.

Coin object spec from board section 05, for when the physical coin gets made: obverse mech brain,
reverse struck zero, edge reeded at 60 ticks.

## Ready to run prompt — Claude Code CLI on this PC

Cowork could not commit or push. Its shell mounts this folder without delete rights, so git
cannot clear its own lock file and has no credentials here either. Run this from
`C:\Users\Cyrus\Code\creationsoftheillminded`.

---
Read AGENTS.md and README.md first.

A stale lock file is blocking git in this repo. Delete `.git\index.lock`, then run
`git status --short --branch` and show me the result before changing anything.

Work already done on disk, all of it uncommitted:

- `index.html` is now the Field Notes design, promoted from `publication-refined.html`, with the
  footer design comparison nav removed. The rejected Barlow version is kept as
  `index.barlow-rejected.20260907.bak.html`.
- `illminded/index.html` is a new $ILLMINDED token landing page, plus `illminded/HANDOFF.md`.
- `assets/brand/` holds the exported brand board, the roundel SVG and a marks sprite.
- `assets/editorial/` holds the cover and project images.
- `.gitignore` ignores `Claude outputs/`, a folder the Claude desktop app writes screenshots into.
- `publication.html`, `publication-refined.html`, `exhibition.html`, `gallery.html` and `AGENTS.md`
  are the rest of the 9/7 work.

Commit in three commits so the history reads clearly:

1. `git add index.html index.barlow-rejected.20260907.bak.html publication.html publication-refined.html exhibition.html gallery.html assets/editorial AGENTS.md .gitignore`
   then commit as "Promote Field Notes publication design to site root".
2. `git add assets/brand` then commit as "Add Creations of the Ill Minded brand system assets".
3. `git add illminded` then commit as "Add $ILLMINDED token landing page, unlinked pre launch".

Do not commit the `Claude outputs` folder. Then push to origin main and tell me the two URLs to
check: the site root and `/illminded/`.

Do not link the token page from the homepage. It stays unlinked until the coin launches. Do not
fill the TBD placeholders and do not change the disclaimer text.
---
