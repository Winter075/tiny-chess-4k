# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Winter075/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Winter075/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB chess engine for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty, $500 in USDC.

The engine uses a 120-square board, incremental tapered PeSTO evaluation and a fixed 75,000-node search. Iterative deepening PVS uses a transposition table, one killer move per ply, null-move pruning, late-move reductions and a check-aware quiescence search. The root takes its moves from the env's legal list, while the tree uses the king-capture convention. That keeps castling, en passant and promotions correct without spending bytes on a second legality layer.

There is no clock and no randomness in the search. The same position and history always produce the same move, so final trials replay byte for byte.

## Run it

```sh
python3 -P -s main.py
```

The engine expects `MAKEFUN_ENV_URL` and talks only to that env. `main.py` is the packed entrypoint. The readable source travels with the submission transcript.

## Checks

Six standard perft suites pass through their published depths after a legal-move filter, including Kiwipete and the en passant, castling and promotion positions.

---

<sub>Entered on [make.fun](https://make.fun/?ref=tamdp7) by [@winter-2](https://make.fun/@winter-2) as [Winter075](https://github.com/Winter075).</sub>
