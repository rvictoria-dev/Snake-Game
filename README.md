# Snake Game

### ₊⊹ About

Snake Game is a reimagining of the classic Snake game, created to practice JavaScript and the Canvas API. The game runs directly in the browser, without any external libraries, and is drawn square by square on a 300x300-pixel canvas. The snake moves using the arrow keys, grows with each piece of food, and passes through the edges of the board, reappearing on the opposite side. The score is updated in real time, and the game restarts automatically when the snake touches its own body. 

https://github.com/user-attachments/assets/2727f315-0c87-421a-adff-b30f0e8317bc

---

### ★ Features

-  Control the snake using the arrow keys (↑ ↓ ← →)

-  Reverse movement block: the snake cannot immediately move in the opposite direction

-  Red food appears at random locations on the board

-  The snake grows with each piece of food

-  Score updated in real time

-  “Infinite” edges: the snake exits on one side and reappears on the other

-  Automatic restart when the snake touches its own body

-  Game designed in `<canvas>` with a 15x15 grid

-  Card-style layout with a soft gradient, dark grid, and Poppins font

---

### .ᐟ.ᐟ How It Works

1. **Board:** The 300x300-pixel canvas is divided into a 15x15 grid of squares, and each square measures 20 pixels.

2. **Snake:** This is an array of coordinates (`snake`), where the first item is the head. It starts at the center of the board and moves to the right.

3. **Game loop:** A `setInterval` runs every 150 ms. On each cycle, the head moves one square in the current direction, and a new position is added to the beginning of the array.

4. **Infinite edges:** The `%` operator causes the snake to reappear on the opposite side when it goes off the edge of the board.

5. **Food and growth:** If the head reaches a food position, the snake grows (the tail is not removed) and a new piece of food appears in a random location. Otherwise, the last item in the array is removed, and the snake simply moves.

6. **Collision:** If the snake’s new head position is already part of its body, the page reloads and the game restarts.

7. **Drawing:** Each cycle, the canvas is cleared, and the food and snake are redrawn, with the head in red and the body in green.

8. **Controls:** The `onkeydown` event reads the arrow keys and changes the direction, ignoring commands that would cause the snake to turn around on itself.

9. **Score:** The score is the length of the snake minus 1 and is updated on the screen every cycle.

---

### ⚙️ Tech Stack

- **HTML5** 

- **CSS3** 

- **JavaScript (Vanilla)** 

- **Google Fonts:** Poppins font (400, 500, and 600)

---

### 🖿 Project structure

snake-game/
├── index.html
├── style.css
├── script.js
└── README.md

---

### 📖 What i learned

- How to draw on a canvas with `getContext("2d")` and `fillRect()`

- How `setInterval` creates a game loop that moves, checks and draws every 150ms

- How the snake is stored as an array of `{x, y}` cells

- How `unshift()` adds a new head and `pop()` removes the tail

- How the % operator wraps the snake around the edges

- How `onkeydown` controls direction without allowing reverse turns
