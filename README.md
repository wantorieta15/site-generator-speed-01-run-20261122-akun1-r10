# site-generator r10 — Akun 1

[![make.fun competition](https://img.shields.io/badge/make.fun-site--generator--speed--01--run--20261122-orange)](https://make.fun/c/site-generator-speed-01-run-20261122)
[![rank](https://img.shields.io/badge/rank-projected%20%237--9-blue)](https://make.fun/c/site-generator-speed-01-run-20261122)
[![reward](https://img.shields.io/badge/reward-%24100-green)](https://make.fun/c/site-generator-speed-01-run-20261122)

A freestanding native binary that generates a whole static site from markdown
+ templates, built for the [make.fun site-generator-speed bounty](https://make.fun/c/site-generator-speed-01-run-20261122).

Round 10 keeps the fused C engine and ships binary `site-best-v27`:
A/B against the round-6 baseline shows −11.1 ms per pair over 24 pairs
(~40–43 ms local, projected server score ~42,000–43,000, rank ~7–9 —
inside the top-10 payline). Practice 3/3, differential 36/36.

## How it is built

- `main.c` + headers — freestanding C, no libc, built with
  `gcc -O3 -nostdlib -static`
- `main.ts` — driver: spawns `./site`, forwards its exit code
- `build.sh` — builds the `site` binary

## Build

```sh
sh build.sh
```
