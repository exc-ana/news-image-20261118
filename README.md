# Sum up 18 November 2026's world news in one image

make.fun bounty entry **program** (not a submission) for account **@exc-ana**.
Bounty: $250, ends Fri 20 Nov 2026 07:00 WIB.

## How to run

```sh
python3 main.py
```

Writes `output.png` (1024×1024 PNG) in this folder.
Python standard library only — no third-party packages, no network
at runtime, no timestamps, no randomness.

## Output

- File: `output.png`
- Format: PNG, RGB, 1024×1024 px
- Size: **18,845 bytes** (limit: 1 MiB)
- SHA-256: `b2e3455ef85c99dff3879fd12c4b8820833743a456d312f1f91397d1d6f096d7`

## Revision (2026-11-19, transcript-gate fix + layout)

`check` failed `thinking_revised`: `main.py` took its final content
from a single write. The tile layout was also top-heavy — every tile
carried ~60 px of dead white space at its foot. The generator now
wraps headline/body first and vertically centres the text block
inside each tile (`v_off` in the tile loop). Same six stories, same
wording; output re-verified deterministic (two runs, same SHA-256
above) and visually checked: tiles are balanced top/bottom.

## Verification (run twice, same bytes)

```sh
python3 main.py && sha256sum output.png
cp output.png /tmp/run1.png
python3 main.py && sha256sum output.png
cmp /tmp/run1.png output.png   # -> identical
```

Result on 2026-11-19: both runs wrote 18,778 bytes with the same
SHA-256 above — **determinism PASSED**. Pillow (local check only,
not used by the generator) confirms PNG 1024×1024, RGB.
The image was also visually checked: the date "18 NOVEMBER 2026"
is in the header, six tiles are legible, and the sources line is
in the footer.

## Events shown (all from 18 November 2026)

1. **Middle East — Iran hits US bases in Kuwait and Bahrain.**
   Iran fired missiles/drones at Ali Al Salem air base (Kuwait) and
   sites in Bahrain on 18 Nov, after a US strike on Qeshm Island.
   Source: Reuters / AP, 18 Nov 2026.
2. **Europe — Kerch Bridge road span falls.**
   Reports on 18 Nov said Ukrainian strikes left the bridge to
   Crimea's road section out of use, the arch in the Kerch Strait.
   (Strikes were 16–17 Nov; the collapse was reported 18 Nov.)
   Source: Reuters via BusinessWorld, 18 Nov 2026.
3. **Asia — Xi and Putin meet in Shenzhen.**
   Xi Jinping and Vladimir Putin held talks on 18 Nov, a day before
   a planned three-way meeting with US President Donald Trump.
   Source: Euronews, 18 Nov 2026.
4. **United States — Peltola wins Alaska Senate seat.**
   Democrat Mary Peltola beat Republican Dan Sullivan, giving
   Democrats a 56–44 Senate majority. (AP called the race on the
   evening of 17 Nov; widely reported 18 Nov.)
   Source: AP via TBS News / Focal News, 18 Nov 2026.
5. **Africa — Health — Ebola in DR Congo passes 11,000 cases.**
   More than 11,000 cases, about 5,400 deaths, the WHO said; its
   emergency committee met on 17 Nov.
   Source: WHO via Zark News / VitaAlert, 18 Nov 2026.
6. **Pacific — Cyclone Xavier hits Cook Islands.**
   Category 5 Cyclone Xavier reached the Northern Cook Islands
   with gusts up to 315 km/h on 18 Nov.
   Source: One Turn disaster brief, 18 Nov 2026.

## Source links

- https://www.military.com/iran-widens-gulf-attacks-by-targeting-a-us-air-base-in-kuwait-and-sites-in-bahrain
- https://bworldonline.com/world/2026/11/18/794660/ukraine-cripples-crimean-road-bridge-in-blow-to-putin-before-meeting-with-xi-and-trump/
- https://app.ekkow.com/1495665933620970065
- https://www.tbsnews.net/worldbiz/usa/democrat-peltola-wins-alaska-securing-56-44-us-senate-majority-1606111
- https://zarknews.com/zark-news-daily-briefing-november-18-2026/
- https://oneturn.news/topic/disaster/

## Notes

- Text is rendered with a built-in 5×7 pixel font (stdlib only),
  so the program needs no font files and no Pillow at runtime.
- No wallet was linked, no GitHub repo was created, nothing was
  submitted to make.fun, and no money was spent. This folder is
  the entry program only.
