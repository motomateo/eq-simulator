# Third-party components

Every direct dependency is listed here; `python scripts/check_licences.py` fails when one is missing. Versions are pinned in `package-lock.json` and `requirements-lock.txt`. Build/test tools are not redistributed; runtime components shipped in `dist/` are marked **shipped**.

## JavaScript / TypeScript (npm)
| component | version | licence | use |
|---|---|---|---|
| typescript | 6.0.3 | Apache-2.0 | compiler (dev) |
| @fontsource-variable/work-sans | 5.3.0 | OFL-1.1 | source of the vendored Work Sans woff2 (dev; files copied to public/fonts/) |
| @types/geojson | 7946.0.16 | MIT | GeoJSON type declarations (dev) |
| maplibre-gl | 6.15.0 | BSD-3-Clause | map rendering (**shipped**, bundled by Vite, no CDN) |
| vite | 8.3.4 | MIT | bundler, dev server (dev) |
| vitest | 5.0.5 | MIT | unit tests (dev) |
| @playwright/test | 1.64.1 | Apache-2.0 | end-to-end tests (dev) |
| @axe-core/playwright | 4.11.0 | MPL-2.0 | accessibility checks in e2e (dev; axe-core 4.11.4, MPL-2.0; not shipped) |
| prettier | 3.9.10 | MIT | formatter (dev) |
| eslint | 10.13.0 | MIT | linter (dev) |
| @eslint/js | 10.0.1 | MIT | linter rules (dev) |
| typescript-eslint | 8.71.2 | MIT | linter TS support (dev) |
| globals | 17.13.0 | MIT | linter globals (dev) |
| @types/node | 26.6.5 | MIT | Node type definitions (dev) |
| lighthouse | 13.5.0 | Apache-2.0 | performance / accessibility audit of the built app, scripts/lighthouse.mjs (dev, Phase 8; not shipped) |

## Python (pip, data pipeline only — nothing shipped)
| component | version | licence | use |
|---|---|---|---|
| geopandas | 1.2.0 | BSD-3-Clause | vector geodata |
| pyogrio | 0.13.0 | MIT | GDAL I/O |
| shapely | 2.2.0 | BSD-3-Clause | geometry |
| pyarrow | 26.0.0 | Apache-2.0 | parquet |
| pandas | 3.0.6 | BSD-3-Clause | tables |
| numpy | 2.5.4 | BSD-3-Clause (+ 0BSD, MIT, Zlib, CC0-1.0 parts) | arrays |
| scipy | 1.18.1 | BSD-3-Clause | statistics |
| networkx | 3.7 | BSD-3-Clause | road graph |
| pyyaml | 6.0.3 | MIT | params/*.yaml |
| osmium | 4.3.2 | BSD-2-Clause | OSM .pbf reading (pyosmium) |
| tifffile | 2026.10.15 | BSD-3-Clause | Copernicus DEM GeoTIFF reading (s09, s10) |
| imagecodecs | 2026.10.10 | BSD-3-Clause | floating-point predictor codec of the DEM COG |
| pymupdf | 2.0 | AGPL-3.0 | PDF page images and GeoPDF georeferencing (PAAR, Primăria S6 maps); pipeline only, nothing shipped |
| matplotlib | 3.11.2 | PSF-based (matplotlib licence) | inspection plots of pipeline layers (dev) |
| pytest | 9.1.1 | MIT | tests (dev) |
| ruff | 0.17.1 | MIT | linter/formatter (dev) |

## Planned (added with their phase, in the same commit as their licence row)
- MapLibre GL JS 6.15.0 (BSD-3-Clause, **shipped**, bundled from npm) — Phase 6.
- Font: Work Sans variable (SIL OFL 1.1, **shipped**, `public/fonts/` latin + latin-ext, from @fontsource-variable/work-sans 5.3.0; Matei D087), placeholder until Re:Rise brand fonts. Mulish was removed.

## Online services used at runtime (not redistributed)
- Basemap vector tiles: OpenFreeMap (tiles.openfreemap.org, styles `dark` for the night theme and `positron` for the day theme; free, no key; data © OpenMapTiles, © OpenStreetMap contributors) — online only, attribution in the map control (D074). CARTO dropped: its tiles now require an API key (checked 2026-10-19).
