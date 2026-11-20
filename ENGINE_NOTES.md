# Notes authored in this session
fixed nodes 75000, no clock
board is a 120 square mailbox
off board squares are newlines
white upper, black lower case
PeSTO tables taper by phase
phase tracked incrementally
negamax alpha beta with PVS
TT keyed by five fields
one killer per ply
quiet moves get history bonus
history capped at 256
null pruning with verify
LMR after fourth quiet move
quiescence extends checks
promotions in quiescence
iterative deepening 1 to 13
root reopens after fail high
nodes sampled every 512
repetition via path set
mate score by ply distance
stalemate scores zero
king capture ends tree
root moves from env list
FEN parsed into mailbox
UCI through mailbox offsets
black rotates the board
post one move per game
no randomness at runtime
no runtime file reads
main.py packed from engine.py
makefun compress packs it
history ordering won games
gauntlet three wins three losses
no wall clock in search
deterministic fixed budget
incremental eval update
check aware quiescence
one TT entry per depth
filler removed for size
source written in session
notes written in session
