# Study Chess

A two-player chess game that runs entirely in the browser — no build step, no server, no dependencies. Built as a single HTML file with vanilla JavaScript implementing the full rules engine from scratch.

## Play it

Just open `chess.html` in any browser. Two players share the same screen and take turns clicking.

Or, if hosted on GitHub Pages:

```
https://your-username.github.io/your-repo-name/chess.html
```

## Features

- Full legal move generation for every piece (no illegal moves, no leaving your own king in check)
- Check, checkmate, and stalemate detection
- Castling (kingside and queenside)
- En passant
- Pawn promotion (choose queen, rook, bishop, or knight)
- Move log in simplified algebraic notation
- Captured piece tracker for both sides
- Click-to-select, click-to-move with legal move highlighting

## How to use

1. Click a piece belonging to the player whose turn it is
2. Legal destination squares light up — a dot for a quiet move, a ring for a capture
3. Click a highlighted square to make the move
4. Pass the device to the other player and repeat

## Tech

Plain HTML, CSS, and JavaScript — no frameworks, no libraries, no build tools. Everything (board state, move generation, check detection, rendering) lives in `chess.html`.

## Known limitations

- No AI opponent — this is local two-player only
- No draw detection by threefold repetition or the 50-move rule
- Move notation doesn't disambiguate when two identical pieces could reach the same square

## Possible next steps

- Online multiplayer (the move logic is already pure functions, so this mainly needs a WebSocket relay between two clients)
- An AI opponent
- Move undo / game save-and-resume
