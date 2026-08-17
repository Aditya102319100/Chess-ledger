# The Ledger — Interactive Chess Engine

A fully playable two-player chess game built from scratch in  JavaScript — no chess libraries, no frameworks.

## Features
- Complete rule enforcement: legal move generation, check, checkmate, and stalemate detection
- Special moves: castling (kingside & queenside), en passant, and pawn promotion
- Legal-move filtering via board simulation — every candidate move is tested on a cloned board to confirm it doesn't leave the king in check
- Live algebraic notation (SAN) move log
- Captured-piece tracking for both sides
- Board flipping and check/last-move highlighting
- Fully custom CSS UI, no frameworks

## Tech Stack
HTML · CSS · JavaScript

## How to Run Locally
Just open `index.html` in any browser — no build step or dependencies required.

## How It Works
The board is represented as an 8x8 array. Move generation happens in two passes: first all *pseudo-legal* moves for a piece are generated (ignoring check), then each candidate is simulated on a cloned board and discarded if it would leave the king in check. This keeps the core rules engine dependency-free while still being fully rule-correct.

## Author
Aditya Gupta 
