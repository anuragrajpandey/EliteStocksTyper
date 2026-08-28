# ⌨️ EliteStocks Typer

A minimal, blazing-smooth typing test — built as a single self-contained HTML file. No build step, no dependencies, no backend. Just open it and type.

![theme](https://img.shields.io/badge/theme-dark%20%2B%20amber-f5a623?style=flat-square)
![deps](https://img.shields.io/badge/dependencies-zero-brightgreen?style=flat-square)
![font](https://img.shields.io/badge/font-Inter-black?style=flat-square)

---

## ✨ Features

- **Live typing feedback** — every letter animates in with a smooth, spring-based pop as you type, colored instantly for correct / incorrect
- **Glowing amber caret** that glides precisely between letters, no jumping or flicker
- **Two text sources**
  - **Random** — endless procedurally-generated common-word passages, timed at 15s / 30s / 60s / 120s (30s by default)
  - **Custom text** — paste in any passage of your own and type it out at your own pace
- **Live stats** — WPM, accuracy, and time/elapsed update every second with a subtle scale "bump" animation
- **Smart backspace** — correcting a word restores it fully; backing past a completed word un-scores it cleanly so your stats never double-count
- **Autofocus on load** — the test is ready to type into the instant the page opens (desktop). No click, no tap, no setup
- **Animated results screen** — a staggered reveal of WPM, accuracy, characters typed, and time, with a one-tap restart
- **Restart anywhere** — press `Tab` at any time to instantly reset the test
- **Selection-safe UI** — all interface text is unselectable and tap-highlight-free, so it feels like a native app rather than a webpage, while input fields remain fully selectable/editable
- **Fully responsive** — scales cleanly from desktop down to mobile

---

## 🎨 Design

Matches the **EliteStocks** brand: near-black background (`#0a0a0a`), warm amber accent (`#f5a623`), soft radial glow lighting, and **Inter** as the sole typeface across the interface. Every transition uses `cubic-bezier` easing tuned for a springy, premium feel rather than linear/robotic motion.

| Token | Value |
|---|---|
| Background | `#0a0a0a` |
| Panel | `#131313` |
| Accent (amber) | `#f5a623` |
| Text | `#f5f5f5` |
| Muted text | `#6b6b6b` |
| Error | `#e5484d` |
| Font | Inter (400 / 500 / 600 / 700 / 800) |

---

## 🚀 Usage

1. Open `elitestocks-typer.html` in any modern browser — that's it, no server required.
2. Start typing immediately — the cursor is focused automatically on load.
3. Switch modes:
   - **Random** → pick a duration (15s / 30s / 60s / 120s) and type until time runs out.
   - **Custom text** → paste your own passage, click **Use this text**, and the test ends automatically once you finish the last word.
4. Press **Tab** anytime to restart with a fresh passage.
5. Results (WPM, accuracy, characters, time) appear automatically when a test finishes — click **Try Again** to go again.

---

## 🛠️ Tech Stack

Just three files' worth of code, all inlined into one HTML document:

- **HTML** — structure only, no frameworks
- **CSS** — custom properties (CSS variables) for theming, `cubic-bezier` transitions, no external UI libraries
- **Vanilla JavaScript** — no dependencies, no build tools, ~250 lines of logic handling state, scoring, and rendering

> Because it's a single static file, you can host it anywhere — GitHub Pages, Netlify, S3, or just double-click it locally.

---

## ⚙️ Customization

A few quick things you can tweak directly in the file:

- **Word bank** — edit the `WORD_BANK` string near the top of the `<script>` block to change the vocabulary used in Random mode.
- **Default duration** — change the `active` class on the `30s` button in the time pill, and update `duration: 30` in `freshState()`.
- **Colors** — everything runs off the CSS variables defined in `:root` at the top of the `<style>` block.
- **Max custom text length** — controlled by the `.slice(0, 400)` cap in `tokenizeText()`.

---

## 📄 License

Free to use, modify, and ship as part of your own projects.

---

Built for **EliteStocks** — clean, fast, minimal.
