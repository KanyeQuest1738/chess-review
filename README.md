# Chess Game Review

A chess.com-style game review page that runs entirely in the browser.

- Step through games with an evaluation bar, evaluation graph and labelled moves.
- Retry your mistakes: Stockfish scores each move you try and checks that it is legal.
- Load new games: fetch a month of games from chess.com by username, or drop / paste a PGN.
  Analysis runs locally with Stockfish 19 (WebAssembly). Nothing is sent to a server.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The page (layout, review logic, built-in example games) |
| `chess.js` | Chess rules library (move legality, PGN reading), BSD-2-Clause |
| `stockfish-19-lite-single.js` / `.wasm` | Stockfish 19 chess engine, GPL-3.0 |

Piece images: cburnett set (via chessground, GPL), embedded in `index.html`.

## Host your own copy on GitHub Pages

1. Sign in to GitHub with your own account.
2. Open this repository and click **Fork** (or: **Code › Download ZIP**, then create a new repository and upload the files).
3. In your copy, open **Settings › Pages**.
4. Under **Build and deployment**, set **Source** to *Deploy from a branch*, **Branch** to `main`, folder `/ (root)`, and click **Save**.
5. Wait about one minute. The site address appears at the top of the Pages settings:
   `https://<your-username>.github.io/<repository-name>/`

To change the default username used by the page, edit `let ME = "MetDeymen";` in `index.html`.
