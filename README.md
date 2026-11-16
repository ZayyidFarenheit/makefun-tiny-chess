[![tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ZayyidFarenheit/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ZayyidFarenheit/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01)

# tiny-chess-01

A 4 KB Python chess engine for make.fun's
[tiny-chess-01](https://make.fun/bounty/tiny-chess-01) bounty.
Referral code: `zfpsetbs`.

`main.py` (3,568 bytes) is a packed engine: 0x88 board, negamax with
alpha-beta, transposition table (32-bit Zobrist), killers, MVV-LVA
ordering, quiescence, null-move pruning and LMR, tapered piece-square
tables, fixed 120,000-node budget per move. Fully deterministic: no
clock, no randomness, no network except the game env, no model calls.

The readable source is `engine.py` (kept out of the snapshot so the
repo stays under 8,192 bytes); `main.py` is produced by the kit's
`makefun compress engine.py --out main.py`.

## Grade it locally

From inside the competition's dev kit:

    makefun grade-local --kit . --bot <your repository> --driver process

It plays a practice trial against the house engines and prints the Elo.
