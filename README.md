# WorstFish ♟️
WorstFish is a UCI-compatible chess engine that intentionally plays the **worst possible moves** using Stockfish as its evaluation backend.

Instead of choosing the best move, WorstFish chooses the move with the **lowest evaluation**, making it extremely weak and easy to beat.

Perfect for testing, debugging, or just having fun.

---

# Features

- UCI compatible
- Works with En Croissant, Arena, CuteChess, etc.
- Uses real Stockfish evaluation
- Always chooses the worst legal move
- Stable and lightweight
- Works as Python script or compiled EXE

---

# Requirements

- Python 3.10+
- Stockfish executable

Download Stockfish:  
https://stockfishchess.org/download/

---

# Folder Structure


WorstFish/
│
├─ WorstFish.py
├─ README.md
│
└─ bin/
└─ stockfish.exe


---

# Running from Python


python WorstFish.py


Test manually:


uci
isready
ucinewgame
position startpos moves e2e4
go depth 10


Expected output example:


bestmove f7f5


---

# Building EXE (Windows)

Install PyInstaller:


pip install pyinstaller


Build:


pyinstaller --noconfirm --onedir --console --add-data "bin;bin" WorstFish.py


Output:


dist/WorstFish/WorstFish.exe


---

# Using with En Croissant

1. Open En Croissant
2. Go to Engine Settings
3. Add Engine
4. Select WorstFish.exe
5. Start game

---

# How WorstFish works

Normal engine logic:


choose move with highest evaluation


WorstFish logic:


choose move with lowest evaluation


It evaluates all legal moves using Stockfish, then picks the worst one.

---

# Example Game


e4 f5

Qh5+ g6

Qxg6#


WorstFish loses quickly.

---

# Engine Info

Name: WorstFish  
Protocol: UCI  
Backend: Stockfish  

Strength: Extremely weak (intentional)

---

# Notes

WorstFish is NOT a chess AI.  
It is a UCI wrapper that makes Stockfish play badly on purpose.

---

# License

Free to use and modify.
