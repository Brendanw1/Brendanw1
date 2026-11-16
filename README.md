```text
                 _^_                                         _^_
                /| |                                         | |\
              // |=|                                         |=| \
             /|  | |\                                     //| |  \
            / |  | |  \                                   /  | |  |\
           /  |  |=|  |\                               //|  |=|  | \
          /|  |  | |  |  \                             /  |  | |  |  \
        // |  |  | |  |  |\                         //|  |  | |  |  |\           _/
       /|  |  |  |=|  |  |  \\                   ///  |  |  |=|  |  | \        _/
      / |  |  |  | |  |  |  |  \_             _//  |  |  |  | |  |  |  \      /
     /  |  |  |  | |  |  |  |  |  _____________  |  |  |  |  | |  |  |  |\   _/
     |  |  |  |  | |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  |  |  |  _/
=================|+|=========================================|+|===========
   ###/\/\/\/\/\/|/|/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/|/|/\/\/\/\/###
                 | |                                         | |
                 | |                                         | |
                #####                                       #####
  ~~~~     ~~~      ~~~~~~      ~~      ~~~~       ~~~~      ~~~      ~~~~~      ~~~
        ~~        ~~~~       ~~        ~~~~~~      ~~      ~~~~~      ~~        ~~~~

      Golden Gate Bridge, San Francisco  ·  home while I finish my M.S. at USF
```

# Brendan Waterval

I build machine learning systems end to end, from ingestion through models, evaluation gates
and a live product, mostly on sports data. Every model I ship has a test written before I look
at its result, and the ones that fail don't ship.

M.S. in Data Science and AI at the University of San Francisco (July 2027), where my practicum
is as the data scientist for USF Baseball's staff. B.S. in CMDA from Virginia Tech, with three
years on the student baseball analytics team.

[LinkedIn](https://www.linkedin.com/in/brendan-waterval) · brendanwaterval@gmail.com

## Featured

**[GOAT-Pro](https://github.com/Brendanw1/goat-pro)** · [goatpro.dev](https://goatpro.dev)
An open MLB and AAA research site on public Statcast data, 2020–2026.
- Pitch-shape and strikeout models (Whiff+, K+, Prevention+) that beat naive baselines at
  predicting next season, using player-grouped folds and clustered bootstrap intervals.
- Value and fielding models checked against outside references: Framing+ r .89–.97 against
  Savant, WAR r .92 / .81 against Baseball-Reference.
- Every model has a pre-registered test in a public results log. Models that fail ship
  labelled "descriptive", or don't ship at all.

**[GOAT-Pro Hoops](https://github.com/Brendanw1/goat-hoops)** · [hoops.goatpro.dev](https://hoops.goatpro.dev)
NBA analytics built on ESPN's public feed and refreshed daily: ingestion, a Python pipeline,
pre-built JSON on Cloudflare R2, and a Next.js front end.
- A per-shot expected-eFG model (gradient boosting, no shooter identity) that beats a
  zone-average baseline on held-out log loss, and Box Plus/Minus split into offense and
  defense, each checked against an external impact model.
- Empirical-Bayes shrinkage on 39 player rates, with exposure (minutes vs attempts) chosen by
  held-out error.
- A win-probability model that failed its calibration test twice. Diagnosing it turned up a
  silent defect in the source feed (late corrections out of time order in about 90% of
  games); fixing it at the source also fixed four other features. The model stays off the
  site.
- Built with coding agents working under written rules: shared work logs, pre-registration,
  a drift check before every publish, and a per-stat source registry (feed call → method →
  code → test → reference).

**[draft-intelligence](https://github.com/Brendanw1/draft-intelligence)** · [live site](https://vt-draft-intelligence.vercel.app)
MLB Draft projections for about 10,700 D1 prospects, built on public data. The pick model beats
a naive baseline by 17% in year-out backtests. I also built a career WAR model and left it out
because it failed the checks I set for it.

**[pitch-classes-statcast](https://github.com/Brendanw1/pitch-classes-statcast)**
A label-free pitch classifier (after Maloof, Haumacher and Bonicki, 2026) tested on 2.1 million
Statcast pitches. Its three pitch classes match Statcast 97.6% of the time and don't drift
between ballparks, and once a pitch's shape is known, its name barely predicts outcomes.

## Team work (private data)

These use TrackMan and team data, so the code stays private. I'm working on write-ups that only
use aggregate numbers.

**BaseballGOAT.** Pitcher and hitter grades on about 7 million D1 pitches. I adapted a
topological pitch tagger so pitches are graded by class instead of by human tag, and the grades
got more stable.

**D1 defensive metrics.** Framing, catcher arm, blocking, and range in runs saved, checked on
players who changed teams and against official NCAA stats.

## Also

- **[pitch-tipping](https://github.com/Brendanw1/pitch-tipping)**: MediaPipe pose estimation on
  a pitcher's set position, looking for differences between pitch types a hitter could read.
- **[capstone-play-calls](https://github.com/Brendanw1/capstone-play-calls)**: a sideline
  play-call tracker Virginia Tech men's basketball used during games instead of pen and paper.
- **[LaneLine](https://github.com/Brendanw1/LaneLine)**: an iOS bike navigation app for San
  Francisco that routes around stressful streets and steep hills (DataSF, OpenStreetMap).
- **[ticket-price-tracker](https://github.com/Brendanw1/ticket-price-tracker)**: resale prices
  from six sites with hidden fees added back, and a text when one drops below my target.
- **[bruteplot](https://github.com/Brendanw1/bruteplot)**: a matplotlib wrapper for bold,
  colorblind-safe charts that returns normal Figure and Axes objects.

**Stack:** Python, SQL (DuckDB), R · LightGBM, XGBoost, scikit-learn, mgcv · TypeScript,
Next.js, Shiny · Vercel, Cloudflare R2 · coding agents and MCP tool servers
