# Link Games

Play now: https://cmercadozelaya.github.io/chess-link/

A small suite of two-player games you play entirely through a shared link — no accounts, no installs. Start a game, send the link to whoever you're playing against, and take turns making moves. Both players see the board update live as moves are made.

Currently includes:

- **Chess** — the classic strategy game.
- **Connect Four** — drop discs and race to connect four in a row.

## How it was made

- It's a handful of static HTML files — no build step, no server to run, just static code hosted with GitHub Pages. `index.html` is the game picker; each game lives on its own page (`chess.html`, `connect-four.html`).
- [chess.js](https://github.com/jhlywa/chess.js) handles the chess rules (legal moves, check, checkmate, etc.), so that game didn't need to be programmed from scratch. Connect Four's rules are simple enough to be handwritten.
- [Firebase Realtime Database](https://firebase.google.com/products/realtime-database) syncs moves between players instantly, which is what makes each board update live without refreshing. Each game stores its data separately so they don't interfere with each other.
- Sound effects are generated on the fly with the browser's built-in Web Audio API, rather than using audio files.
