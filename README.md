# Sentinel-2 Orbit Visualization

An interactive HTML visualization of the tandem orbits of **Sentinel-2A** and **Sentinel-2B**, showing their cumulative swath coverage over a full 8-day repeat cycle.

[![Sentinel-2 tandem orbit visualization](https://github.com/user-attachments/assets/8f8be46b-50e2-4db5-b64c-2c6b59ffde29)](https://burchfisher.github.io/Sentinel-2-orbit-viz/)

## 🌍 Live Demo

**[View the visualization →](https://burchfisher.github.io/Sentinel-2-orbit-viz/)**

## About

The Sentinel-2 mission, operated by the European Space Agency (ESA) as part of the Copernicus program, consists of two identical satellites — Sentinel-2A and Sentinel-2B — flying in the same sun-synchronous orbit at 786 km, positioned 180° apart. Together, they image the Earth's land surfaces, large islands, and coastal waters with a 290 km swath, achieving a global revisit time of 5 days at the equator (and more frequently at higher latitudes).

This visualization illustrates how the two satellites' orbital paths combine over 8 days to produce near-complete global coverage.

### Constellation Continuity

The visualization is labeled for **Sentinel-2A and Sentinel-2B**, the original tandem pair (launched 2015 and 2017). The orbital configuration shown is identical for the next-generation pair:

- **Sentinel-2C** launched on 5 September 2024 and is now gradually replacing Sentinel-2A.
- **Sentinel-2D** is planned to launch around 2028 and will replace Sentinel-2B.

Because the 2C/2D pair occupies the same 786 km sun-synchronous orbit with the same 180° phasing and 5-day combined revisit cycle, the orbital geometry and coverage pattern shown here remain representative of the active constellation going forward.

## Built With

This visualization was created using [Claude Design](https://www.anthropic.com/claude) (Anthropic) and is rendered with:

- [**Three.js**](https://threejs.org/) — 3D rendering of the globe and orbital paths
- [**TopoJSON**](https://github.com/topojson/topojson) — compact encoding of world map geometry

The output is a self-contained HTML artifact — all code, styling, and dependencies are bundled into a single `index.html` file with no external build step or server required.

## Running Locally

```bash
git clone https://github.com/burchfisher/Sentinel-2-orbit-viz.git
cd Sentinel-2-orbit-viz
open index.html   # or just double-click the file
```

## Repository Contents

- `index.html` — the complete, self-contained visualization

## License

Free to use and adapt. Attribution appreciated.
