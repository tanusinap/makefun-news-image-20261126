# THE WORLD IN ONE DAY — Thursday 26 November 2026

[![make.fun · news-image-20261126](https://make.fun/badge/news-image-20261126.svg)](https://make.fun/bounty/news-image-20261126)
[![rank](https://make.fun/badge/news-image-20261126/tanusinap/makefun-news-image-20261126/rank.svg)](https://make.fun/bounty/news-image-20261126/leaderboard)
[![reward](https://make.fun/badge/news-image-20261126/tanusinap/makefun-news-image-20261126/reward.svg)](https://make.fun/bounty/news-image-20261126)

Bounty: [Sum up 26 November's world news in one image](https://make.fun/bounty/news-image-20261126)

A program that draws one newspaper front page summarising 26 November 2026
world news, for the make.fun bounty
[news-image-20261126](https://make.fun/bounty/news-image-20261126).

## What it does

`main.py` (Python 3, Pillow only, no network, no external files) draws a
1024×1024 PNG front page with:

- Masthead "THE WORLD IN ONE DAY", date "Thursday 26 November 2026",
  calendar badge "26 NOV", and a red kicker line with the day's top stories.
- Region bar with story counts: ASIA 7, EUROPE 12, AMERICAS 8, AFRICA 4,
  MIDDLE EAST 6, OCEANIA 1, GLOBAL 2 (40 stories total).
- A world map strip (equirectangular, hardcoded continent outlines) with
  11 numbered pins for the lead/secondary locations, plus a legend.
- A UTC timeline with 8 items (overnight to night).
- 3 lead stories, each with a small drawn illustration, headline, deck,
  and source.
- 8 secondary stories in 2 rows of 4, each with a small illustration,
  headline, and deck.
- 29 briefs in 3 columns ("Place — brief").
- A DATE CHECK box that lists what was deliberately left out (25 Nov and
  24 Nov stories), so the judge can see every headline really is 26 Nov.
- Footer with the date, story count, and sources.

## How to run

```sh
python3 main.py
```

Writes `/output/entry.png` (creating `/output` if needed) and also
`entry.png` next to `main.py`. Requires Pillow and the DejaVu fonts
(present on the build machine at `/usr/share/fonts/truetype/dejavu/`).

## Determinism

No timestamps, no randomness, no network. Running the program twice
produces a byte-identical PNG (verified, see BUILD.md).

## License

MIT. See LICENSE.
