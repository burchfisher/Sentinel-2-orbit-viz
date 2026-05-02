# Sentinel-2 Orbit Visualization

An interactive HTML visualization of the tandem orbits of **Sentinel-2A** and **Sentinel-2B**, showing their cumulative swath coverage over a 7-day repeat cycle.

[![Sentinel-2 tandem orbit visualization](https://github.com/user-attachments/assets/e6a93b7c-77d5-4a78-b3be-3095a702af97)](https://burchfisher.github.io/Sentinel-2-orbit-viz/)

## 🌍 Live Demo

**[View the visualization →](https://burchfisher.github.io/Sentinel-2-orbit-viz/)**

## About

The Sentinel-2 mission, operated by the European Space Agency (ESA) as part of the Copernicus program, consists of two identical satellites — Sentinel-2A and Sentinel-2B — flying in the same sun-synchronous orbit at 786 km, positioned 180° apart. Together, they image the Earth's land surfaces, large islands, and coastal waters with a 290 km swath, achieving a global revisit time of 5 days at the equator (and more frequently at higher latitudes).

This visualization illustrates how the two satellites' orbital paths combine over 7 days to produce near-complete global coverage.

This visualization renders a 3D globe with orbit wires, satellite markers, modeled swath accumulation, day-side illumination, and a 7-day timeline scrubber. It is designed as an educational tool rather than an operational acquisition planner.

### Constellation Continuity

The visualization is labeled for **Sentinel-2A and Sentinel-2B**, the original tandem pair (launched 2015 and 2017). The orbital configuration shown is identical for the next-generation pair:

- **Sentinel-2C** launched on 5 September 2024 and is now gradually replacing Sentinel-2A.
- **Sentinel-2D** is planned to launch around 2028 and will replace Sentinel-2B.

Because the 2C/2D pair occupies the same 786 km sun-synchronous orbit with the same 180° phasing and 5-day combined revisit cycle, the orbital geometry and coverage pattern shown here remain representative of the active constellation going forward.

## Features

- Fixed default view toward the descending, sunlit acquisition side
- Drag-to-rotate 3D globe
- Descending-pass-only swath accumulation
- Day-side illumination aligned with the sun-synchronous orbit geometry
- 7-day timeline with day tick labels
- 5-day combined-constellation revisit note in telemetry
- Coverage counter for land area covered within the normal systematic latitude band, shown as `56S-83N`
- Orbit Cycles counter for elapsed shared-orbit periods
- Cyan and magenta swaths for the two active satellite tracks

## Model Notes

The visualization uses:

- Sentinel-2 altitude of 786 km
- 290 km swath width
- 143-orbit / 10-day repeat cycle for each individual satellite
- Two satellites phased 180 degrees apart, producing a combined 5-day revisit cycle
- Orbit Cycles reports elapsed orbital periods of the shared orbit, not the sum of individual spacecraft orbits
- Area-weighted 0.5 degree land coverage grid
- TopoJSON land geometry rasterized through D3
- Explicit antimeridian handling for swath rendering and coverage accounting

The swaths are visualized across the `56S-83N` latitude band used for the normal systematic acquisition domain. The coverage percentage reports land area covered within that band; the real mission also acquires inland and coastal waters along the swath.

Cloud cover, exact acquisition planning, instrument duty cycles, special-request polar acquisitions, and detailed orbital perturbations are outside the scope of this model.

## Built With

This visualization was created using [OpenAI Codex](https://openai.com/codex/) and is rendered with:

- [**Three.js**](https://threejs.org/) — 3D rendering of the globe and orbital paths
- [**TopoJSON**](https://github.com/topojson/topojson) — compact encoding of world map geometry
- [**D3**](https://d3js.org/) — geographic projection and land-mask rasterization
- Plain HTML, CSS, and JavaScript

The output is a self-contained HTML artifact — all code, styling, and dependencies are bundled into a single `index.html` file with no external build step or server required.

## Running Locally

```bash
git clone https://github.com/burchfisher/Sentinel-2-orbit-viz.git
cd Sentinel-2-orbit-viz
open index.html   # or just double-click the file
```

## Repository Contents

- `index.html` - complete editable visualization
- `README.md` - project overview and usage notes
- `LICENSE` - MIT license

## License

MIT License. See `LICENSE` for details.
