```text
                   _._                                 _._
                   | |                                 | |
                ///| |                                 | |\\
              //   |-|\                               /|-|  \\\
           /// |   | | \\                           // | |  |  \\
         // |  |   | |  |\\                       //   | |  |  | \\\
      ///|  |  |   |-|  |  \\\                 /// |   |-|  |  |  | \\
    //|  |  |  |   | |  |  |  \\\           /// |  |   | |  |  |  |  |\\
  //  |  |  |  |   | |  |  |  |  \_________/ |  |  |   | |  |  |  |  |  \\
// |  |  |  |  |   | |  |  |  |  |  |  |  |  |  |  |   | |  |  |  |  |  | \\
===================|=|=================================|=|==================
                   | |                                 | |
  ~~~   ~~~~~     ~~   ~~~~      ~~~~   ~~~     ~~~~~   ~~    ~~~~   ~~~
```

# Brendan Waterval

I'm a grad student in data science at USF, and through my practicum I'm the data scientist for USF Baseball. Before
that I did my undergrad in CMDA at Virginia Tech and spent three years on the student baseball analytics team there.

Most of my work is college baseball with TrackMan data: pitch grades, defensive metrics, and figuring out which
numbers actually hold up from one season to the next. A lot of the time goes into checking my own models, like
whether a catcher's framing follows him when he transfers or just stays with his old team.

[LinkedIn](https://www.linkedin.com/in/brendan-waterval) · brendanwaterval@gmail.com

## Projects you can look at

**[draft-intelligence](https://github.com/Brendanw1/draft-intelligence).** MLB Draft projections for about 10,700
D1 prospects, built on public data. The pick model beats a naive baseline by 17% in year-out backtests. I also built
a career WAR model and left it out because it failed the checks I set for it.
[Live site](https://vt-draft-intelligence.vercel.app).

**[pitch-tipping](https://github.com/Brendanw1/pitch-tipping).** Runs MediaPipe pose estimation on photos of a
pitcher's set position and looks for differences between pitch types that a hitter could pick up on.

**[capstone-play-calls](https://github.com/Brendanw1/capstone-play-calls).** A sideline play-call tracker my
capstone team built for Virginia Tech men's basketball. The staff used it during games in place of pen and paper.

**[LaneLine](https://github.com/Brendanw1/LaneLine).** An iOS bike navigation app for San Francisco that routes
around stressful streets and steep hills, using DataSF and OpenStreetMap data.

**[ticket-price-tracker](https://github.com/Brendanw1/ticket-price-tracker).** Watches resale prices on six ticket
sites, adds the hidden fees back in so prices are comparable, and texts me when one drops below my target.

**[bruteplot](https://github.com/Brendanw1/bruteplot).** A small matplotlib wrapper for bold, outlined charts with a
colorblind-safe palette. It returns normal Figure and Axes objects, so it works with existing plotting code.

## Private work

These use TrackMan and team data, so the code stays private. I'm working on write-ups that only use aggregate
numbers.

**BaseballGOAT.** Pitcher and hitter grades on about 7 million D1 pitches. The most interesting thing I found is
that college pitch tags depend a lot on who is running the TrackMan: nearly identical pitches get different names
22% of the time across ballparks, compared with 3% within the same game. I adapted a topological pitch tagger
(Maloof et al., 2026) so pitches are graded by class instead of by tag, and the grades got more stable.

**D1 defensive metrics.** Framing, catcher arm, blocking, and range in runs saved, checked on players who changed
teams and against official NCAA stats.

I mostly work in Python, R, and SQL (DuckDB), with LightGBM, XGBoost, and mgcv for models, and Shiny or Next.js
when something needs a front end.
