# Tiny chess engine (make.fun bounty "tiny-chess-01")

A chess engine in Python that plays through the make.fun env protocol
(`MAKEFUN_ENV_URL`: POST /game, /move, /resign).

`main.py` is the packed entrypoint produced by the official tool
(`node cli/makefun.mjs compress`) from the readable source `engine_source.py`
(9,616 bytes), which is **not** committed to this repository; it travels with
the submission bundle (`makefun bundle` packs it beside the transcripts).

Engine sketch (readable source): bitboard-free 64-square board, full legal
move generation (castling, en passant, promotions), negamax alpha-beta with
transposition table, quiescence search (captures + check evasions), null-move
pruning, late move reductions, check extensions, killer moves, iterative
deepening under a fixed node budget (fully deterministic: no clock, no
randomness). Evaluation: material + piece-square tables, pawn structure
(doubled/passed pawns), pawn shield, bishop pair, rook on open files,
endgame king table.

License: MIT (see LICENSE).

[![make.fun](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/curiousdiscoveries2-eng/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/curiousdiscoveries2-eng/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01)

Entry for the [make.fun bounty tiny-chess-01](https://make.fun/bounty/tiny-chess-01).



