# Data licence and attributions

Unless stated otherwise below, everything in this repository and on the published site — code, derived data, parameters, documentation and UI assets — is licensed under **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**; full text in `LICENSE`, summary at https://creativecommons.org/licenses/by-nc-sa/4.0/.

Share-alike follows from the GEM inputs (CC BY-NC-SA 4.0). The full source-by-source matrix with compliance notes is `docs/LICENSING.md`.

## Exception: OpenStreetMap-derived database (ODbL 1.0)
The road graph (the `osm` section of the packed bundle in `public/bundle/`) and any other layer derived from OpenStreetMap (fire stations, administrative boundary, building mask) form a **derivative database of OpenStreetMap** and are licensed under the **Open Database License 1.0** (https://opendatacommons.org/licenses/odbl/1-0/), not CC BY-NC-SA. Map data © OpenStreetMap contributors, https://www.openstreetmap.org/copyright. The section is kept separate in the bundle so this exception stays clean.

## Attributions
| source | licence | attribution / changes |
|---|---|---|
| harta.dupacutremur.ro register (Re:Rise) | Re:Rise own data, used with credit | "Date: harta.dupacutremur.ro (Re:Rise)". Addresses, internal ids and names are not redistributed in the client bundle. |
| GEM Global Exposure Model v2026.0.0 (summaries) | CC BY-NC-SA 4.0 | Yepes-Estrada et al. 2023, doi 10.5281/zenodo.8117363. Used as a cross-check of the derived background stock. |
| GEM Global Vulnerability Model v2026.0.0 (Romania) | CC BY-NC-SA 4.0 | Nafeh, Aljawhari & Silva 2025, doi 10.5281/zenodo.8391742. Loss ratios used for economic loss. |
| ESRM20 exposure, model (incl. fragility) and vulnerability database | CC BY 4.0 | Crowley et al. 2021, EFEHR TR002, doi 10.7414/EUC-EFEHR-TR002-ESRM20. Changed: disaggregated to the 1 km census grid, rescaled to the 2021 census, register buildings subtracted; logncdf mean/stddev converted to median/β. |
| Eurostat Census 2021 1 km grid v3 | CC BY 4.0, © European Union 2026 | "Source: Eurostat, Census 2021 grid v3, clipped and reprojected; modified by eq_simulator, Eurostat is not responsible for the modified data." |
| OpenStreetMap | ODbL 1.0 | © OpenStreetMap contributors (see exception above). |
| FEMA Hazus 6.1 Earthquake Model Technical Manual | US Government work, public domain | Table numbers cited in `params/` and `docs/METHOD.md`. |
| ICCPDC 1977 digitisation (sibling project) | CC BY-NC 4.0 | Matei Sumbasacu, ICCPDC 1977 digitisation. |
| Published papers (GMPE, GMICE, casualty model) | cited only | Parameters are cited from the papers; no PDF is redistributed. |

## Phase 7 layers (experimental)

The flood footprint (`flood_*`, `cell_flood_frac`, `osm/edge_flooded`, `fs_flooded`, `hosp_flooded`) and the liquefaction classes (`liq_*`, `cell_liq_frac`, `reg_liq`) are derived databases: OpenStreetMap streets and rivers (ODbL), the Copernicus DEM GLO-30 (Produced using Copernicus WorldDEM-30 (c) DLR e.V. 2010-2014 and (c) Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved.), the PAAR Bucuresti Annex 7.3 street list (public administrative document) and the outline of the Primaria Sector 6 dam-break map (reuse pending; the map itself is not redistributed). They are approximations and are labelled so in the application.
