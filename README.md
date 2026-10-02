# Classic Snake

A browser-based Snake game with a green LCD phone look, built with plain HTML, CSS and JavaScript. No libraries or frameworks.

**Play it here:** https://sunishaphadtare15.github.io/classicsnake/

\[Screenshot of the game](screenshot.png)

## Features

* Three difficulty levels (Easy, Medium, Hard), remembered between visits
* Score and high score saved in the browser with `localStorage`
* The game speeds up as you eat
* Pause and resume
* Works on desktop and mobile (keyboard, swipe gestures, or on-screen keys)
* Auto-pauses when you switch tabs

## Controls

|Action|Desktop|Mobile|
|-|-|-|
|Move|Arrow keys or WASD|Swipe on the screen, or use the on-screen keys|
|Pause / resume|Space|Pause button on the overlay|

## Tech used

* **HTML5 Canvas** to draw the game board
* **CSS** for the phone and LCD design, and for the responsive layout
* **JavaScript** for the game loop, input handling and collision detection
* **localStorage** for the high score and difficulty setting
* **GitHub Pages** for hosting

## How it works

* The board is a 20 x 20 grid, and the snake is an array of `{x, y}` cells with the head at index 0.
* On every tick a new head is added in the current direction. If the snake ate food, the tail is kept so it grows, otherwise the tail is removed.
* A `requestAnimationFrame` loop redraws the board every frame, and the snake only moves when enough time has passed (this time gets shorter as your score goes up).
* Key presses are stored in a small queue, so two quick turns are not lost, and 180 degree turns are blocked.
* A collision is detected when the new head is outside the grid or lands on a body cell.

## What I added

* Difficulty selector with saved preference
* Classic LCD phone redesign
* *(add your own features here, for example: sound effects, wrap-around mode, golden bonus food)*

## What I learned

* How a game loop works with `requestAnimationFrame`
* Drawing on a canvas and handling keyboard and touch input
* Saving data in the browser with `localStorage`
* Deploying a static site with GitHub Pages

## Run it locally

1. Download or clone this repo.
2. Open `index.html` in your browser. No install or build step is needed.

## Credits

Built with the help of AI tools, then studied, customized and extended by me.

