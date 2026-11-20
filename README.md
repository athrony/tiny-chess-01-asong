# Tiny Chess

Original MIT-licensed Python 3.13 chess engine for tiny-chess-01.

`main.py` contains the complete implementation in a bzip2-packed Latin-1
string. It uses only the Python standard library and the game environment.
Run it with `python3 -P -s main.py` and `MAKEFUN_ENV_URL` set.

Search uses iterative-deepening negamax, alpha-beta/PVS, quiescence with
check evasions, transposition bounds, null-move pruning, late-move
reductions, and capture, killer, and history ordering. Evaluation blends
opening and endgame piece-square scores with material and bishop pairs.
Each move has a deterministic 120,000-node budget. Search uses no clock.
The environment's legal list constrains the root move.

The protocol was checked against the official starter. All chess code was
written for this entry. The existing MIT license is retained.
