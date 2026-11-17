# BIC21203 Web Development - Lab 4a: Client-Side Scripting (JavaScript)

**Name:** Muhammad Syafiq
**Matric No.:** CI250113
**Programme:** Bachelor of Computer Science (Information Security), FSKTM, UTHM
**Session:** 2026/2027

## Overview

Three small pages that use plain JavaScript (no external libraries) to update page content, validate input and generate HTML elements. All text is written with `textContent`, and events are attached with `addEventListener()`.

| Folder | Task | Key concepts |
| --- | --- | --- |
| `q1/` | Interactive Text Changer | DOM selection, `changeMessage()`, click event |
| `q2/` | Smart Number Validator | `checkInput()`, `if...else if...else`, input validation |
| `q3/` | Dynamic Number Generator | `generateNumbers()`, `for` loop, `createElement()` |

## How to run

No build step or server is needed. Open the `index.html` file in a current desktop browser (Chrome, Edge or Firefox), or use VS Code Live Server.

### Q1 - Interactive Text Changer
1. Open `q1/index.html`. The paragraph shows "Welcome to my website!".
2. Click **Change Message**. The paragraph becomes "Hello there!".

### Q2 - Smart Number Validator
1. Open `q2/index.html`.
2. Type a value and click **Check**.
3. Test cases:

| Input | Expected message |
| --- | --- |
| `5` | The number is lower than 10 |
| `10` | The number is equal to 10 |
| `10.5` | The number is higher than 10 |
| `15` | The number is higher than 10 |
| `abc` | Please enter a valid number! |
| (empty or spaces) | Please enter a valid number! |

### Q3 - Dynamic Number Generator
1. Open `q3/index.html`.
2. Click **Generate**. An ordered list shows "The number is 1" to "The number is 5".
3. Click again. The list is cleared first, so there are no duplicates.

## Screenshots

### Q1 - Interactive Text Changer

| Before click | After click |
| --- | --- |
| ![Q1 before](screenshots/q1-before.png) | ![Q1 after](screenshots/q1-after.png) |

### Q2 - Smart Number Validator

| Input 5 | Input 10 | Input 15 |
| --- | --- | --- |
| ![Q2 input 5](screenshots/q2-5.png) | ![Q2 input 10](screenshots/q2-10.png) | ![Q2 input 15](screenshots/q2-15.png) |

| Input abc | Empty input |
| --- | --- |
| ![Q2 input abc](screenshots/q2-abc.png) | ![Q2 empty input](screenshots/q2-empty.png) |

### Q3 - Dynamic Number Generator

| Before click | After click |
| --- | --- |
| ![Q3 before](screenshots/q3-before.png) | ![Q3 after](screenshots/q3-after.png) |

## Brief explanation

- **Q1:** the paragraph and button are selected with `getElementById()`. `changeMessage()` sets the paragraph's `textContent`, and the click listener on the button calls it.
- **Q2:** the input is trimmed, converted with `Number()` and checked with `Number.isFinite()`, so empty values and text such as `abc` are rejected. An `if...else if...else` chain then picks the message, which is written to `#result`.
- **Q3:** `generateNumbers()` empties the list, then a `for` loop from 1 to 5 creates each `<li>` with `createElement()`, sets its text and appends it to the `<ol>`.
