# Zuoluoji Park (左羅紀公園) | Zuozhen Layered-Stamp Trail

An interactive family travel guide for Zuozhen District, Tainan, Taiwan.
First-place winner of the 2026 Chuang-Jian Nanfang (創見南方) competition, "Badlands Play for Kids" (惡地童遊) track.

🔗 Live site: https://cueeeee.github.io/zuozhen/

## What it is

Visitors follow one of two routes (Old Street Route / Gongguan Community Route) through 14 stations in Zuozhen. At each station they press a layered stamp onto the same card, and the stamps stack up into one complete picture of Zuozhen.
This website is the on-site companion:

- **3D map**: Built with three.js. The badlands terrain, roads, river and every station's building are procedurally generated and placed according to real Google Maps positions. The five halls of the Zuozhen Fossil Park have indoor scenes.
- **Progressive unlock via QR codes**: Each station's QR code opens `?s=<stationId>`. Visitors only see stations up to the one they've reached, and answering a quiz question unlocks the next one.
- **Single HTML file**: No build step. Served directly by GitHub Pages.

## Project structure

```
zuozhen/
├── index.html   Main page: 3D guide + all stations (HTML, CSS and JS in one file)
├── about.html   Static "About the project" page (example of adding a sub-page)
├── CLAUDE.md    Development rules for AI agents
├── AGENTS.md    Points to CLAUDE.md
└── README.md    This file
```

## Rules for AI agents

See [`CLAUDE.md`](./CLAUDE.md) (`AGENTS.md` points to the same file). It covers the project's purpose, file naming and placement, where each part of `index.html` lives, the visual style, the format for adding new stations or sub-pages, and the rules an AI must follow when making changes.

## Local preview

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000/
