# Tiny Chess — 4 KB Python chess engine

An original 0x88 chess engine in a single 4,063-byte `main.py`
(an LZMA-compressed payload plus a two-line unpacker; MIT licensed).

Search: iterative-deepening alpha-beta with PVS and LMR,
quiescence over captures/promotions and check evasions,
transposition table, killer + history move ordering, check
extensions, repetition detection. Eval: material + piece-square
tables + bishop pair, with king middlegame/endgame phase
interpolation. Fixed 80,000-node budget per move — fully
deterministic (no clock, no randomness), so live and replay
trials play identically.

Run: `MAKEFUN_ENV_URL=http://... python3 -P -s main.py`
