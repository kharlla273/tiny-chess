# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/kharlla273/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/kharlla273/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Tiny Chess — an original 0x88 chess engine in a single 3,432-byte `main.py` (an LZMA-compressed payload plus a two-line unpacker; MIT licensed). Practice Elo 1,451 on trial-0 (4 wins, 2 losses), above the sunfish baseline's 1,365.

Search: iterative-deepening alpha-beta with PVS and LMR, quiescence over captures/promotions and check evasions, transposition table, killer + history move ordering, check extensions, repetition detection. Eval: material + piece-square tables + bishop pair, with king middlegame/endgame phase interpolation. Fixed 80,000-node budget per move — fully deterministic (no clock, no randomness), so live and replay trials play identically.

Build: the readable source is `readable.py` (kept in the working tree, uncommitted); `main.py` is produced from it with the kit's `node cli/makefun.mjs compress readable.py`, which records the pair so the entry can be re-packed and verified byte for byte.

## Run it

```sh
MAKEFUN_ENV_URL=http://... python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=n305kcfc&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
