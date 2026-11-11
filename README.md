# Skidmore Baseball Analytics, 2026

A season-in-review dashboard for Skidmore College baseball, built from the official 2026 cumulative stats. It's the baseball companion to the [Skidmore hockey dashboard](https://github.com/noahfighter883/skidmore-hockey-2026-27).

## What the 2026 season says

- **The record hides two different teams.** Skidmore went 18-15 overall, 13-5 outside the Liberty League but 5-10 in it.
- **Close games slipped away.** The team was 2-6 in one-run games while outscoring opponents by 53 runs on the year.
- **The offense was a strength.** A .847 team OPS and 7.5 runs per game. Eddie Galvao led regulars with a 1.154 OPS and was the only hitter near the top in both average and power.
- **Walks were the pitching staff's biggest problem.** The staff struck out 8.9 per nine but walked 5.0. Quinn Hocom led with 77 strikeouts in 49 innings, and Jack Collins had the best ERA among starters at 2.68.
- **The team ran well.** 84 steals in 101 attempts, including Mac Cady going 18 for 19.

## What's in the dashboard

- **Overview:** record, run differential, team OPS and ERA, and a "What stands out" summary.
- **Players:** OPS by hitter, plate discipline (walk rate vs. strikeout rate), power vs. average, stolen bases, pitcher strikeouts vs. walks, and pitcher workload colored by ERA.
- **Season:** run differential for all 33 games, with Liberty League games marked.
- **Data:** full batting and pitching tables, plus definitions.

Every chart has hover tooltips, and every summary number is computed from the CSVs, so updating the data updates the page.

## Data

The three files in `data/` are copied from the official stats at [skidmoreathletics.com](https://skidmoreathletics.com/sports/baseball/stats):

- `batting.csv`: cumulative batting stats for every hitter
- `pitching.csv`: cumulative pitching stats for every pitcher
- `games.csv`: game-by-game results, with a `conf` column flagging Liberty League games (Bard, Rensselaer, Ithaca, Vassar, Union)

## Running it

It's a single static page with no build step. The page loads the CSVs with `fetch`, so open it through a local server rather than double-clicking the file:

```
python3 -m http.server
```

Then visit http://localhost:8000.

To host it, import the repo into Vercel (no framework, no build command) or turn on GitHub Pages.
