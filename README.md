# PepperChess — tiny chess engine (make.fun tiny-chess-01)

A from-scratch 0x88 chess engine in a single self-extracting `main.py`
(4,089 bytes): negamax alpha-beta/PVS, Zobrist transposition table,
quiescence, null-move pruning, LMR, killer + history ordering, PST eval.
Searches a fixed 100,000 nodes per move — fully deterministic, no clock,
no randomness. Talks HTTP JSON to the make.fun env
(`MAKEFUN_ENV_URL`): `POST /game`, `POST /move`, `POST /resign`.

Build: the readable engine lives in `chess-dev/engine.py` (dev only, not
part of this snapshot); `chess-dev/pack.py` minifies, lzma-compresses and
escapes it into `main.py`. MIT licensed. Original work, not a sunfish fork.
