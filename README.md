# Sentinel-2 Orbit Visualization

An interactive HTML visualization of the tandem orbits of **Sentinel-2A** and **Sentinel-2B**, showing their cumulative swath coverage over a full 8-day repeat cycle.

## 🌍 Live Demo

**[View the visualization →](https://burchfisher.github.io/Sentinel-2-orbit-viz/)**

## About

The Sentinel-2 mission, operated by the European Space Agency (ESA) as part of the Copernicus program, consists of two identical satellites — Sentinel-2A and Sentinel-2B — flying in the same sun-synchronous orbit, 180° apart. Together, they image the Earth's land surfaces, large islands, and coastal waters with a 290 km swath, achieving a global revisit time of 5 days at the equator (and more frequently at higher latitudes).

This visualization illustrates how the two satellites' orbital paths combine over 8 days to produce near-complete global coverage.

## Running Locally

This is a single self-contained HTML file with no build step or dependencies. To run it locally:

```bash
git clone https://github.com/burchfisher/Sentinel-2-orbit-viz.git
cd Sentinel-2-orbit-viz
open index.html   # or just double-click the file
```

## Repository Contents

- `index.html` — the complete, self-contained visualization

## License

Free to use and adapt. Attribution appreciated.
