# 🧠 Antigravity Memory Card Game

A modern, responsive browser-based memory card matching game built entirely with vanilla **HTML5**, **CSS3**, and **JavaScript (ES6+)**. Designed specifically for PC and laptop displays with sleek visuals, 3D card-flipping animations, procedural synthesizer sound effects, and persistent score tracking.

---

## 🎮 Gameplay & Core Features

- **Dynamic Card Shuffling**: Every game automatically shuffles a new deck using the Fisher-Yates algorithm.
- **3D Card Flip Mechanics**: Smooth CSS 3D transforms (`rotateY(180deg)`) with backface culling and elevation effects on hover.
- **Visual Feedback**:
  - **Match**: Small success pop animation with glowing emerald border.
  - **Mismatch**: Brief delay followed by a subtle shake animation before flipping back face-down.
  - **Victory**: Celebratory modal with accuracy recap and lightweight canvas confetti burst.
- **Anti-Cheat & Rapid-Click Protection**: The board automatically locks during card checks to prevent rapid clicking from breaking the game state.
- **Timer & Move Tracker**:
  - Timer starts automatically upon the player's first card flip.
  - Accurate move counter (1 move = 1 pair attempt).
  - Accuracy percentage calculation `(matches / moves) * 100%`.
- **Persistent High Scores**: Automatically saves and updates best times and lowest move counts for each difficulty level in `localStorage`.
- **Synthesizer Sound Effects (Web Audio API)**:
  - Procedural sound effects generated directly by the browser (no external `.mp3` or `.wav` files required).
  - Includes sounds for: Card Flip, Correct Match, Incorrect Match, and Victory Fanfare.
  - Quick toggle button (🔊 / 🔇) to mute/unmute audio with state remembered in `localStorage`.

---

## 🕹️ Difficulty Modes

Designed with tailored grid layouts for PC and laptop screens:

| Difficulty | Cards | Pairs | Grid Layout |
| :--- | :--- | :--- | :--- |
| **Easy** | 12 | 6 | 4 columns × 3 rows |
| **Medium** | 16 | 8 | 4 columns × 4 rows |
| **Hard** | 24 | 12 | 6 columns × 4 rows |

*Switching difficulty at any time immediately starts a fresh game and loads that difficulty's specific best score.*

---

## 📂 Project Structure

```text
js/
├── index.html        # Game layout, header, stats dashboard, grid wrapper & win modal
├── style.css         # Modern dark theme, CSS variables, 3D flip effects & animations
├── script.js         # Game state manager, Web Audio synth, canvas confetti & storage
├── prompt.md         # Original project requirements specification
└── README.md         # Comprehensive project documentation
```

---

## 🚀 How to Run

1. Simply double-click **`index.html`** or right-click and choose **Open with > Google Chrome** (or Microsoft Edge, Mozilla Firefox, Safari).
2. Alternatively, run a lightweight local static server:
   ```bash
   # Using Node.js
   npx serve .
   
   # Or using Python
   python -m http.server 8000
   ```
3. Open `http://localhost:8000` in your browser.

---

## 🛠️ Built With

- **HTML5**: Semantic tags, ARIA accessibility attributes, and modal dialog structure.
- **CSS3**: CSS Grid, Flexbox, Custom Properties (Variables), 3D Transforms (`preserve-3d`, `perspective`), and Keyframe Animations.
- **Vanilla JavaScript (ES6+)**: Object-oriented state architecture, Fisher-Yates shuffle, event delegation, and DOM manipulation.
- **Web Audio API**: Real-time audio waveform synthesis (Sine, Triangle, Sawtooth oscillators with exponential gain envelopes).
- **HTML5 Canvas API**: Lightweight particle simulation for confetti celebration.

