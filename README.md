# 🎛️ SYNTHCALC

> *A retro-futuristic calculator drenched in synthwave neon.*

A fully functional calculator app built with pure HTML, CSS, and JavaScript. No frameworks. No dependencies. Just pixel-perfect neon glow, chunky buttons, and satisfying click feedback.

---

## ✨ Features

### 🎨 Visual Design
- **Synthwave aesthetic** — deep violet/black background with a scanline-overlaid CRT display
- **Neon glow system** — three accent colors (cyan `#00ffe7`, hot pink `#ff2d78`, yellow `#ffe600`) with layered `text-shadow` and `box-shadow` glows
- **Animated grid floor** — subtle perspective grid and horizon bleed evoke outrun style
- **Floating orbs** — pulsing ambient light sources that breathe in the background
- **Glossy button sheen** — each key has a top-half gloss layer for a physical, tactile feel
- **Scanline overlay** — CRT-style repeating lines on the display for retro authenticity
- **Blinking status dots** — three colored LEDs in the header blink in staggered sequence

### ⚙️ Functionality
- **Full arithmetic** — addition, subtraction, multiplication, division
- **Modifier keys** — `+/−` sign toggle and `%` percentage
- **Chained operations** — press an operator mid-chain to continue without hitting equals
- **Error handling** — division by zero displays `ERROR: DIV/0` in red glow
- **Precision fix** — results use `toPrecision(12)` to eliminate floating-point drift
- **Comma formatting** — large numbers automatically formatted with thousands separators
- **Responsive font sizing** — display text shrinks gracefully for long results
- **Calculation history** — last 20 results stored in a collapsible panel; click any entry to restore it
- **Keyboard support** — full numpad and keyboard input (see table below)
- **Ripple on click** — radial highlight emanates from exact click position on each button

---

## 🚀 Getting Started

No setup needed. Just open the file.

```bash
open calculator.html
```

Or drag `calculator.html` into any browser window.

---

## 📁 File Structure

```
synthcalc/
└── calculator.html    # Single self-contained file — all HTML, CSS & JS
└── README.md          # This file
```

---

## ⌨️ Keyboard Shortcuts

| Key(s)            | Action              |
|-------------------|---------------------|
| `0` – `9`         | Input digits        |
| `.`               | Decimal point       |
| `+`               | Addition            |
| `-`               | Subtraction         |
| `*`               | Multiplication      |
| `/`               | Division            |
| `Enter` or `=`    | Calculate result    |
| `Backspace`       | Delete last digit   |
| `Escape`          | Clear (AC)          |
| `%`               | Percentage          |

---

## 🛠️ Tech Stack

| Layer      | Choice                                                      |
|------------|-------------------------------------------------------------|
| Markup     | Semantic HTML5                                              |
| Styling    | Vanilla CSS (custom properties, keyframes, CSS Grid)        |
| Logic      | Vanilla JavaScript (ES6+)                                   |
| Fonts      | Google Fonts — *Orbitron* (display) + *Share Tech Mono* (body) |
| Storage    | In-memory (session history, no persistence needed)          |

Zero npm packages. Zero build tools. Zero external dependencies beyond Google Fonts.

---

## 🎨 Customization

All colors are defined as CSS custom properties at the top of the `<style>` block:

```css
:root {
  --bg:         #07050f;   /* Page background */
  --panel:      #0d0a1a;   /* Calculator surface */
  --border:     #2a1f4a;   /* Button borders */
  --pink:       #ff2d78;   /* Hot pink — equals button, errors */
  --cyan:       #00ffe7;   /* Cyan — operators, display text */
  --yellow:     #ffe600;   /* Yellow — clear button */
  --purple:     #9b5de5;   /* Purple — special keys, glow accents */
  --display-bg: #050310;   /* Display panel background */
  --btn-base:   #160f2e;   /* Default button background */
  --btn-hover:  #1f1545;   /* Button hover background */
  --text:       #e8e0ff;   /* Primary button text */
  --muted:      #4a3a6a;   /* Secondary / expression text */
}
```

Want a green terminal look? Swap `--cyan` to `#00ff41` and `--bg` to `#020c02`. Want a warm amber CRT? Use `--cyan: #ffb347` with `--bg: #0a0500`.

---

## 🧠 Logic Notes

- **Chained operations**: pressing an operator without hitting `=` first will evaluate the pending expression automatically, then start a new one.
- **`freshResult` flag**: tracks whether the display shows a completed result. The next number press starts fresh rather than appending.
- **Precision**: `toPrecision(12)` followed by `parseFloat` strips trailing zeros while keeping accuracy for standard calculations.
- **History**: stored in a simple in-memory array (most recent first, capped at 20 entries). Clicking a history row restores that result as the current value.

---

## 📸 Highlights

- **No frameworks** — ~300 lines of clean, readable JS
- **Single file** — drop `calculator.html` anywhere and it works
- **Keyboard-first** — designed to be used without touching the mouse
- **Accessible font scaling** — display auto-adjusts size for results up to 12+ digits

---

## 📄 License

MIT — use it, remix it, neon it up however you like.
