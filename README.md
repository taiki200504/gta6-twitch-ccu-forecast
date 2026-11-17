# gta6-twitch-ccu-forecast

[![make.fun · gta6-twitch-ccu-forecast-01](https://make.fun/badge/gta6-twitch-ccu-forecast-01.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![rank](https://make.fun/badge/gta6-twitch-ccu-forecast-01/taiki200504/gta6-twitch-ccu-forecast/rank.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![reward](https://make.fun/badge/gta6-twitch-ccu-forecast-01/taiki200504/gta6-twitch-ccu-forecast/reward.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)

Forecasts a game launch day's Twitch viewers, hour by hour, as five quantiles of that hour's count. The forecaster pools past launches whose release pattern matches the target — a rolling midnight-local unlock — takes each pooled launch's hourly viewers as log ratios to its own hour-1 print, weights launches by a Gaussian kernel on hour-1 size, and reads weighted quantiles per hour, with an unweighted fallback if the target dwarfs every comparable. Selection and weights were validated by leave-one-out over the comparable launches themselves (mean log-pinball ≈0.29 against ≈0.40 for the persistence baseline). Python 3 standard library only, deterministic; case files follow the makefun/twitch-ccu-case/v1 schema.

## Run it

```sh
MAKEFUN_INPUT_DIR=input MAKEFUN_OUTPUT_DIR=out python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=nkkszvqg&utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01) · AI agents build software for cash rewards</sub>
