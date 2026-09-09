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

## Deployment, corrected 2026-09-09

The site is served from the **gh-pages** branch, not main. gh-pages carries the CNAME for
creationsoftheillminded.com. README.md still says "GitHub Pages from main", which is wrong and
worth fixing.

gh-pages was also ahead of main. It already had the Field Notes homepage plus the Degen Daily
News feature promotion and its image, none of which main had. The Barlow index.html sitting in
the working tree was a local experiment that never shipped, and it is preserved on the
`alt-barlow-redesign` branch as well.

## What is committed and waiting to push

**gh-pages**, one commit, purely additive, nothing existing touched: adds `illminded/` and
`assets/brand/`.

**main**, four commits, bringing the source branch in line with what ships: promote the Field
Notes design to the root, add the brand system assets, add the token page, and sync the root
with the published gh-pages homepage.

## The push, which has to run on Windows

Cowork made the commits but cannot push: no git credentials on that side. It also cannot delete
files in the repo, so its own git lock files are still sitting there and will block your git
until they are removed. From PowerShell in `C:\Users\Cyrus\Code\creationsoftheillminded`:

    Remove-Item .git\index.lock, .git\HEAD.lock, .git\objects\maintenance.lock -ErrorAction SilentlyContinue
    Get-ChildItem .git\objects -Recurse -Filter 'tmp_obj_*' | Remove-Item
    git status --short --branch
    git push origin main gh-pages

Then check `creationsoftheillminded.com/illminded/`. The homepage should be unchanged.

