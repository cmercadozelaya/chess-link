# Link Chess

Play the game: https://cmercadozelaya.github.io/chess-link/

A simple two-player chess game you play entirely through a shared link — no accounts, no installs. Start a game, send the link to whoever you're playing against, and take turns making moves. Both players see the board update live as moves are made.

## How it was made

- It's a single HTML file — no build step, no server to run, just static code hosted with GitHub Pages.
- [chess.js](https://github.com/jhlywa/chess.js) handles the chess rules (legal moves, check, checkmate, etc.), so the game itself didn't need to be programmed from scratch.
- [Firebase Realtime Database](https://firebase.google.com/products/realtime-database) syncs moves between players instantly, which is what makes the board update live without refreshing.
- Sound effects are generated on the fly with the browser's built-in Web Audio API, rather than using audio files.
