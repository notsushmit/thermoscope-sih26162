# `data` branch

Input state for the scheduled 2026 NRT update (`.github/workflows/nrt-update.yml` on `main`).
Not source code. The workflow overwrites this branch with a single commit
whenever the running FIRMS 2026 store changes, so its history is intentionally short.

- `data/raw/firms_gujarat_2026.csv` — running, deduplicated VIIRS_SNPP_NRT store for Gujarat (updated by the workflow)
- `data/raw/osm_*.csv`, `data/raw/wri_gppd_gujarat_thermal_plants.csv` — cached evidence sources (OSM, WRI GPPD)
- `data/processed/gujarat_cluster_integrated_evidence.csv` — fixed historical cluster evidence used for overlap joins
- `data/processed/models/source_classifier_lightgbm_v2.joblib` — locked classifier (predict-only, never retrained)
