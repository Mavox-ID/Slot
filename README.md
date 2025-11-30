# 🎰 Classic Slot Machine - Pure HTML/CSS/JS

<p align="center">
  <img src="https://img.shields.io/badge/Website-https://mavox_id.github.io/Slot-blue" alt="Website https://mavox-id.github.io/Slot">
  <img src="https://img.shields.io/badge/Made by-Mavox ID-blueviolet" alt="Canvas Size">
  <img src="https://img.shields.io/badge/License-MIT-grayblue" alt="Canvas Size">
</p>

A sleek, purely frontend implementation of a classic 3-reel slot machine game built with **HTML**, **CSS**, and vanilla **JavaScript**. Experience the thrill of the spin directly in your browser\!

### Online website game: [**Classic Slot Machine**](https://mavox-id.github.io/Slot)

-----

## ✨ Features

  * **Classic 3-Reel Layout:** Authentic slot machine visuals with three spinning reels.
  * **Interactive Lever:** Pull the handle using a **mouse drag** or **touch gesture** to initiate the spin, simulating a real slot machine mechanic.
  * **Vibrant UI/UX:**
      * **Animated Symbols:** Reels spin and settle with engaging acceleration and deceleration effects.
      * **Winning Animations:** Flashing lights, a glowing win line, and a "💰" animation celebrate winning combinations (three identical symbols).
      * **Responsive Design:** Optimized for both desktop and mobile screens using CSS media queries.
  * **Pure Frontend:** No external libraries or frameworks—just clean, native web technologies.

-----

## 🚀 Getting Started

This project is a single-file application (`index.html` structure), making it incredibly easy to set up.

**Or just open a online game**: [Slot](https://mavox-id.github.io/Slot)

### Prerequisites

You only need a modern web browser (Chrome, Firefox, Safari, Edge, etc.).

### Installation

1.  **Clone the repository** (assuming you upload this code to a Git repository):

    ```bash
    git clone https://github.com/YourUsername/your-repo-name.git
    cd your-repo-name
    ```

2.  **Open the file:** Simply open the `index.html` file in your preferred web browser.

    ```bash
    # For example, on a Mac:
    open index.html
    ```

-----

## 🕹️ How to Play

1.  **Locate the Handle:** Find the red-topped lever on the right side of the machine.
2.  **Pull Down:**
      * **Desktop:** Click and **drag the handle downwards**.
      * **Mobile:** **Touch and drag the handle downwards**.
3.  **Release:** Release the drag/touch to trigger the spin.
4.  **Wait for the Results:** The reels will spin sequentially and stop.
5.  **Win\!** If all three symbols align (e.g., three 7️⃣'s or three 🍒's), you win, and an animation will play\!

-----

## 🛠️ Technology Stack

| Technology | Purpose |
| :--- | :--- |
| **HTML5** | Structure and semantic markup for the game elements. |
| **CSS3** | Extensively used for styling, responsiveness, gradients, shadows, and keyframe animations (`@keyframes titleGlow`, `winPop`). |
| **JavaScript (ES6)** | Core game logic, handle dragging mechanics, reel spinning logic, and win detection. |

-----

## ⚙️ Core Logic Highlights

The game is primarily driven by the following JavaScript functions:

  * **`initializeSlotMachine()`**: Populates the reels with a long list of random symbols at startup.
  * **`startDrag()`, `drag()`, `endDrag()`**: Manages the drag-and-drop mechanics for the lever handle, allowing the user to "pull" it.
  * **`pullHandle()`**: The main function that resets the handle and initiates the reel spins with slightly staggered final results.
  * **`spinReel(reelId, finalSymbol, duration)`**:
      * This function handles the visual spinning effect using `setInterval` to rapidly change the reel position (`reel.style.top`).
      * It implements a **deceleration mechanism** (`speed *= 0.92`) to create a realistic slow-down before the reel locks into the predetermined `finalSymbol` position using a smooth CSS transition.
  * **`checkSlotMachineWin(symbols)`**: Compares the three final symbols to determine if they match, triggering the visual win effects if successful.

-----

## 📄 License

This project is open-source and available under the [MIT](LICENSE) License.
