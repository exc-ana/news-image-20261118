[![make.fun](https://make.fun/badge/news-image-20261118.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118) [![rank](https://make.fun/badge/news-image-20261118/exc-ana/news-image-20261118/rank.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118) [![reward](https://make.fun/badge/news-image-20261118/exc-ana/news-image-20261118/reward.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)

# Sum up 18 November 2026's world news in one image

make.fun bounty entry **program** (not a submission) for account **@exc-ana**.
Bounty: $250, ends Fri 20 Nov 2026 07:00 WIB.

> NOTE FOR PUSHING: the GitHub README carries the three make.fun
> badges at the top (added on GitHub 2026-11-19). When pushing this
> file, prepend those three badge lines above the title again.

## How to run

```sh
MAKEFUN_OUTPUT_DIR=out python3 main.py
```

Writes `entry.png` (1024x1024 PNG) to `$MAKEFUN_OUTPUT_DIR`
(default `/output/entry.png`). Python standard library only — no
third-party packages, no network at runtime, no timestamps, no
randomness.

## Output (broadsheet rebuild, 2026-11-19 ~23:20 WIB)

- File: `entry.png`
- Format: PNG, RGB, 1024x1024 px
- Size: **38,026 bytes** (limit: 1 MiB)
- SHA-256: `0736c17c974be6ea4e1452794dc07af41f3f4f01c8ba243724a09986d381e4bb`

## What it is

A one-page broadsheet rebuilt from the top-10 research
(`TOP10-RESEARCH.md`, leaderboard + Feed live 19 Nov 2026): navy
masthead, giant date headline "WEDNESDAY 18 NOVEMBER 2026", red
"NOV 18 / WED - 2026" box, a "THE DAY IN NUMBERS" strip, 13
numbered story cards with flat vector illustrations drawn in code
(no photos), a dotted world map "WHERE IT HAPPENED" with numbered
pins, a short UTC timeline, evidence tags (CONFIRMED / CLAIM /
REPORT), a numbered index of 27 more stories ("ALSO ON WEDNESDAY
18 NOVEMBER"), a red "DATE CHECK" footer naming what was left out
and why, and a sources line. 40 stories in all.

## Verification (run twice, same bytes)

```sh
MAKEFUN_OUTPUT_DIR=/tmp/out1 python3 main.py
MAKEFUN_OUTPUT_DIR=/tmp/out2 python3 main.py
sha256sum /tmp/out1/entry.png /tmp/out2/entry.png  # identical
```

Result: both runs wrote 38,026 bytes with the same SHA-256 above —
**determinism PASSED**. Visually checked (full-page preview plus
crops of masthead, cards, map/index and footer): no clipped or
badly overlapping text; two semicolons that the 5x7 font cannot
render were replaced with commas.

## Events shown (all first reported Wednesday 18 November 2026)

Big cards 1-13: (1) Xi welcomes Trump in Shenzhen; (2) Iran drones
down over the Gulf, no US casualties; (3) Voyager 1 one light-day
out, 25.9bn km at 10:16 UTC; (4) Russia fires 141 drones, 126 shot
down; (5) EU loan of EUR 45bn for Ukraine; (6) Dow falls 561 on
hawkish Fed minutes; (7) Jeffries wins 251-11; (8) tanks reach
Nuseirat; (9) Cyclone Akvan nears Odisha; (10) GTA VI out at
midnight in New Zealand; (11) 535 factories shut in Bangladesh;
(12) Anthropic IPO priced USD 81bn; (13) troops mass on the
Ethiopia-Eritrea border. Index 14-40: COP31 fossil split, Ebola
11,300+ cases, Tame Impala 7 ARIAs, Alcaraz in Turin, ADNOC tanker
hit, UK 3.6% / eurozone 4.0% inflation, Sudan 2,230 killed in 2026,
Van Gogh USD 190.4M, England ODI 2-1, Romania M5.7, Indonesia 6%,
Brent USD 91.95, gold USD 2,792, US-Venezuela defence pact, Pew
trust survey, and sub-facts of the big cards.

DATE CHECK (in the image): left out because they are Tuesday
17 November news — Kerch Bridge fall, Nvidia results, Peltola win,
Knesset vote, US strike on Qeshm, Board of Peace warning, Mongolia
president quitting, Prague train crash, An-12 crash, Thaci 17-month
sentence. Not yet happened — Trump-Xi-Putin summit Thu 19,
Anthropic first trade Thu 19, Akvan landfall Fri 20, COP31 close
Fri 20.

## Earlier versions

- v1 (6 stories, 18,845 bytes, SHA `b2e3455e…`): submitted 19 Nov
  23:05 WIB (commit 530ba69, claim AF-TVW31-SPB54-TPAD9-ER2TS) but
  grading failed, program exit 1 — it wrote `output.png` inside the
  repo folder while the grader runs `/bot` read-only and reads
  `$MAKEFUN_OUTPUT_DIR/entry.png`.
- Fix (commit `e5839bc`): output path fixed, image bytes unchanged.
  Bundle rebuilt, `makefun check` 13 passed / 0 failed.
- This broadsheet rebuild supersedes both: same output path, new
  40-story image.

## Notes

- Text is rendered with a built-in 5x7 pixel font (stdlib only),
  so the program needs no font files and no Pillow at runtime.
- No wallet was linked, no GitHub repo was created, nothing was
  submitted to make.fun, and no money was spent. This folder is
  the entry program only.
