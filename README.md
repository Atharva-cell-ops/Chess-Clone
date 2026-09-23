# ♟ Chess Clone

A real-time multiplayer chess game built with **Node.js**, **Socket.IO**, and **Chess.js** — styled after [chess.com](https://chess.com).

![Chess Clone Screenshot](https://img.shields.io/badge/status-playable-brightgreen)

## Features

- **Real-time multiplayer** — two players connect via WebSocket
- **Drag & drop** piece movement
- **Server-side validation** — all moves validated by Chess.js on the server
- **Spectator mode** — third+ connections can watch the game
- **Board flipping** — black player sees the board from their perspective
- **Chess.com-inspired UI** — classic green & cream board, dark sidebar

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Server | Node.js + Express |
| Real-time | Socket.IO |
| Chess Logic | Chess.js |
| Templating | EJS |
| Styling | Vanilla CSS |

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14+)

### Installation

```bash
# Clone the repo
git clone https://github.com/Atharva-cell-ops/Chess-Clone.git
cd Chess-Clone

# Install dependencies
npm install

# Start the server
npx nodemon
```

Open **two browser tabs** at `http://localhost:3000`:
- First tab → **White**
- Second tab → **Black**
- Any additional tabs → **Spectator**

## Project Structure

```
Chess-Clone/
├── app.js                  # Express + Socket.IO server
├── package.json
├── public/
│   └── js/
│       └── chessgame.js    # Client-side game logic
└── views/
    └── index.ejs           # Game UI template
```

## How It Works

1. The server assigns the first connection as **White** and the second as **Black**
2. Players drag pieces to make moves — moves are sent to the server via Socket.IO
3. The server validates each move using Chess.js and broadcasts the updated board state
4. Invalid moves are rejected server-side

## License

MIT
