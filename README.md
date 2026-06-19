# SpatialThoughts AI Skills

Claude Code skills for cloud-native geospatial analysis, published by [SpatialThoughts](https://spatialthoughts.com).

## Available Skills

### `cloud-native-remote-sensing`

A guide for writing cloud-native remote sensing code in Python. Covers STAC search, loading data with `odc-stac` / XArray / Dask, Sentinel-2 preprocessing, spectral indices, zonal statistics, supervised classification, and more.

**When to use:** Invoke at the start of a session before writing or editing any remote sensing analysis code — e.g. when creating a new notebook, adding a new workflow, or debugging an existing one.

## Installation

### Option A: Claude Code Plugin (recommended)

Add this repo as a plugin marketplace source, then install the skill:

```
/plugin marketplace add spatialthoughts/spatialthoughts-ai-skills
/plugin install cloud-native-remote-sensing@spatialthoughts-ai-skills
```

Once installed, invoke the skill with:

```
/cloud-native-remote-sensing
```

### Option B: Copy the skill file into your project

Place `SKILL.md` directly in your project's `.claude/skills/cloud-native-remote-sensing/` directory:

```bash
mkdir -p .claude/skills/cloud-native-remote-sensing
curl -o .claude/skills/cloud-native-remote-sensing/SKILL.md \
  https://raw.githubusercontent.com/spatialthoughts/spatialthoughts-ai-skills/main/skills/cloud-native-remote-sensing/SKILL.md
```

### Option C: Copy the contents into CLAUDE.md

Append the skill content to your project's `CLAUDE.md`:

```bash
curl https://raw.githubusercontent.com/spatialthoughts/spatialthoughts-ai-skills/main/skills/cloud-native-remote-sensing/SKILL.md >> CLAUDE.md
```

## Python Stack

The skill covers these packages:

- `pystac-client` — STAC catalog search
- `odc-stac` — load STAC items to XArray
- `xarray` + `rioxarray` — raster data model and geospatial ops
- `dask` / `dask.distributed` — lazy parallel computation
- `geopandas` — vector data
- `duckdb` — querying cloud-native vector files (GeoParquet, Parquet)
- `scikit-learn` — machine learning and classification
- `xvec` + `exactextract` — zonal statistics

## Source Course

This skill is derived from the [Cloud Native Remote Sensing with Python](https://spatialthoughts.com/courses/python-remote-sensing/) course by SpatialThoughts.
