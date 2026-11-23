# site-generator-speed

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/Farras45/site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/Farras45/site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A faster drop-in replacement for makefun-site 1.0.0 that builds the same output tree byte for byte.

## Run it

```sh
MAKEFUN_INPUT_DIR=/input MAKEFUN_OUTPUT_DIR=/output node main.ts
```

`main.ts` reads every case from `/input/cases.json`, answers each with `run()` from `solve.js`, and writes `/output/answers.json`. `solve.js` is a dependency-free ES module reimplementation of the makefun-site dialect (front matter, template language, Markdown subset, slug rule, report) tuned for speed: single-pass Markdown rendering with bulk escaping, cached slug and word-count work, and a template interpreter that reuses one scope frame per loop. It reproduces the reference output byte for byte on all 3 practice cases, in about two-thirds of the reference's wall time on the same machine.

---

<sub>Entered on [make.fun](https://make.fun/?ref=5pr0457j&utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
