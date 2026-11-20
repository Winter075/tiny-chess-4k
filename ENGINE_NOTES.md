# Engine notes authored in this session
fixed node budget is 75000, no wall clock
the board is a 120 square mailbox
off board squares are marked with a newline
white pieces are upper case, black lower case
PeSTO tables are tapered by phase
phase is tracked incrementally during moves
search is negamax with alpha beta and PVS
the transposition table is keyed by five fields
one killer move is kept per ply
quiet moves gain a history bonus
history bonus is capped at 256
null move pruning uses a verification search
late move reductions start after the fourth quiet move
quiescence extends checks up to two plies
promotions are searched in quiescence
iterative deepening runs from depth one to thirteen
the root reopens with a full window after fail high
the node counter is sampled every 512 nodes
repetition is tracked with a path set
mate scores are adjusted by distance from root
stalemate is scored as zero
king capture is the terminal test in the tree
the env legal list supplies root moves only
FEN is parsed into the mailbox
UCI squares map through the mailbox offsets
black to move is handled by rotating the board
the engine posts one move per game loop
no randomness and no runtime file reads
main.py is packed from engine.py by makefun compress
history ordering was the score positive change
the gauntlet result was three wins and three losses
