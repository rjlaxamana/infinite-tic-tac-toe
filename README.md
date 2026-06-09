# ∞ Tic Tac Toe

A minimalist take on tic tac toe where the board never fills up — because marks don't last forever.

![infinite-ttt](https://img.shields.io/badge/deploy-vercel-black?style=flat-square&logo=vercel)
![no dependencies](https://img.shields.io/badge/dependencies-none-lightgrey?style=flat-square)
![vanilla js](https://img.shields.io/badge/built%20with-vanilla%20js-f7df1e?style=flat-square&logo=javascript&logoColor=black)

## How it works

Each player can only have **3 marks on the board at once**. On your fourth turn, your oldest mark is automatically removed before your new one is placed — keeping the board perpetually alive and forcing both players to rethink their position every single turn.

The mark about to be evicted **glows amber** so you always know what's at risk.

## Rules

- Standard tic tac toe win condition (3 in a row)
- Each player is limited to 3 marks at a time
- On turn 4+, your oldest mark is removed before placing a new one
- The glowing mark is always the next to be removed
- You cannot place on an occupied cell

## Modes

| Mode | Description |
|------|-------------|
| **PvP** | Two players, same device |
| **PvC** | Play against the computer |

The computer uses a one-step lookahead strategy: it wins when it can, blocks when it must, avoids moves that let you win immediately, and otherwise prioritizes center and corners.

## Stack

- Pure HTML, CSS, and vanilla JavaScript — no framework, no build step
- Single `index.html` file (~430 lines)
- Google Fonts (Inter) loaded via CDN

## Deploy to Vercel

```bash
# Clone the repo
git clone https://github.com/your-username/infinite-ttt.git
cd infinite-ttt

# Deploy (requires Vercel CLI)
npx vercel
```

Or connect the repository directly at [vercel.com/new](https://vercel.com/new) — no configuration needed beyond what's already in `vercel.json`.

## Run locally

No build step required. Just open `index.html` in a browser:

```bash
open index.html
# or serve it with any static file server
npx serve .
```

## Project structure

```
infinite-ttt/
├── index.html   # the entire game
└── vercel.json  # Vercel routing config
```

## License

MIT
