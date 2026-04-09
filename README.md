# 🌸 Window Garden Idle

> *A cozy idle game about growing flowers on a sunny windowsill.*

---

## Description

Window Garden Idle is a relaxing browser-based idle/incremental game set on a small apartment windowsill. Plant flowers, collect pollen, and watch your little garden come alive — even when you step away.

The focus is atmosphere over complexity. A living day/night sky cycles overhead, pollen drifts past the glass, a bee occasionally visits, and your plants sway gently in a breeze you can almost feel. There are no timers counting down, no fail states, and no pressure — just a window, some soil, and time.

---

## Features

- **Three plant types** — Daisies, Tulips, and Sunflowers, each with different costs and pollen rates. Sunflowers get a bonus during daylight hours.
- **Living day/night cycle** — A full sky simulation moves through Dawn → Day → Dusk → Night on a 5-minute loop, with a sun/moon arc, stars, clouds, and sunbeam rays. Growth rates shift with the light.
- **Pollen particles** — Tiny floating particles drift upward from the sill, growing denser as your garden expands.
- **Water Plants** — A manual boost giving ×3 pollen generation for 30 seconds, with a cooldown.
- **Bee Friend upgrade** — Unlocks an animated bee that flies across the window and auto-waters your plants every 45 seconds.
- **Six upgrades** — Rich Soil, Bee Friend, Night Bloom, Sunbeam Glass, Golden Pollen, and Greenhouse, each stacking multiplicatively.
- **Offline progress** — Pollen accumulates while you're away (up to 4 hours, at 55% efficiency). You're greeted with how much you earned on return.
- **Auto-save** — Garden state is saved to `localStorage` every 30 seconds and on tab close.
- **Main menu** — New game / Continue / Reset, with a confirmation step before wiping your save.

---

## How to Play

1. Open `window-garden-idle.html` in any modern browser — no install, no server needed.
2. Press **Start Garden** from the main menu. Your first Daisy is already potted.
3. Watch pollen accumulate in the top-left counter.
4. Spend pollen on more plants using the panel on the right.
5. Buy upgrades as they become affordable to accelerate your garden.
6. Hit **Water Plants** for a quick burst when you want to push ahead.
7. Leave the tab open — or close it and come back later. Your garden grows either way.

---

## Plant Reference

| Plant      | Base Cost | Pollen/sec | Notes                              |
|------------|-----------|------------|------------------------------------|
| 🌼 Daisy    | 10        | 0.3        | Great early-game stacker           |
| 🌷 Tulip    | 75        | 2.0        | Solid mid-game earner              |
| 🌻 Sunflower| 400       | 12.0       | ×1.5 during Day (×3 with Sunbeam) |

Costs scale up by 12–16% per purchase (standard idle formula).

---

## Upgrade Reference

| Upgrade         | Cost    | Effect                              |
|-----------------|---------|-------------------------------------|
| 🌱 Rich Soil     | 150     | All generation ×1.5                 |
| 🐝 Bee Friend    | 300     | Bee auto-waters every 45s           |
| 🌙 Night Bloom   | 650     | Removes night-time penalty          |
| 🔆 Sunbeam Glass | 1,200   | Sunflower day bonus ×2 (becomes ×3) |
| ✨ Golden Pollen | 3,500   | All generation ×2                   |
| 🏡 Greenhouse    | 15,000  | All generation ×3                   |

---

## Technical Notes

- Single HTML file, no dependencies, no build step.
- Runs on a `requestAnimationFrame` loop with delta-time; progress is frame-rate independent.
- All rendering is DOM/CSS — no canvas.
- Fonts loaded from Google Fonts (Nunito). Works offline if fonts are cached.
- Save key: `wgIdle2` in `localStorage`.

---

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Requires CSS `clip-path` and `backdrop-filter` support for full visual fidelity.

---

## Credits

Made with HTML, CSS, and vanilla JavaScript.  
Font: [Nunito](https://fonts.google.com/specimen/Nunito) by Vernon Adams (Google Fonts).

---

*go touch some grass 🌿*
