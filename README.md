# Snake Game

A single-page Snake game served by a tiny local web server. No dependencies beyond Python 3.

## Project layout

```
snake_game/
├── server.py          # Minimal static file server (Python standard library only)
├── public/
│   └── index.html     # The game (HTML + CSS + JavaScript in one page)
└── README.md
```

## Requirements

- Python 3.7 or newer (check with `python3 --version`)
- Any modern web browser

## Start the server

1. Open a terminal and go to the project folder:

   ```bash
   cd /path/to/snake_game
   ```

2. Start the server:

   ```bash
   python3 server.py
   ```

   You should see:

   ```
   Snake game running at http://localhost:8000  (Ctrl+C to stop)
   ```

3. Open <http://localhost:8000> in your browser.

### Use a different port

If port 8000 is already in use, pass a port number:

```bash
python3 server.py 8080
```

Then open <http://localhost:8080>.

## Stop the server

Press `Ctrl+C` in the terminal where the server is running.

## How to play

| Action        | Keys                         |
| ------------- | ---------------------------- |
| Move          | Arrow keys or `W` `A` `S` `D` |
| Pause/resume  | `Space`                      |
| Start/restart | `Space`, `Enter`, or click the button |
| Touch screens | Swipe on the board           |

- Two pieces of red food are always on the board. Eat one to grow and score a point; a new one appears right away.
- Any new piece of food has a 20% chance to be **super food** (glowing gold). Eating it grows the snake by 2 segments and scores 2 points.
- The snake speeds up as your score rises.
- Hitting a wall or your own body ends the game.
- Your best score is saved in the browser.

## Troubleshooting

- **`Address already in use`** — another program is using the port. Run with a different port, e.g. `python3 server.py 8080`.
- **`python3: command not found`** — install Python 3 from <https://www.python.org/downloads/> (on Windows, try `python server.py`).
