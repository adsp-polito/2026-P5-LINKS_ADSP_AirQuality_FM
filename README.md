# High-Resolution Urban Air Quality Mapping with Foundation Models

**Applied Data Science Project — Politecnico di Torino**  
**Study areas:** Turin and/or Milan, Italy | **Target resolution:** ~1 km, daily | **Status:** Research proposal

## Overview

Urban air pollution varies considerably over short distances, while monitoring stations provide measurements at relatively few locations. This project investigates whether pretrained environmental and Earth-observation foundation models can combine ground observations, satellite data, meteorology, and geographic features to estimate daily near-surface pollutant concentrations across urban areas.

The primary objective is **same-day air quality mapping (nowcasting)**. One-day-ahead forecasting may also be explored.

## Objectives

- Estimate **NO₂, SO₂, O₃, PM₁₀, and PM₂.₅** concentrations over Turin and/or Milan.
- Generate georeferenced daily maps at approximately **1 km resolution** (potentially 500 m).
- Evaluate adaptations of **Aurora** and the **Copernicus Foundation Model (COPFM)**.
- Compare predictions against coarse-resolution baselines using independent monitoring-station observations.

## Data and methodology

| Data source | Purpose |
| --- | --- |
| Ground monitoring stations | Reference pollutant measurements and validation |
| Sentinel-1, -2, -3, and -5P | Radar, optical, thermal, and atmospheric observations |
| CAMS | Coarse atmospheric estimates and baseline predictions |
| ERA5-Land | Meteorological predictors |
| Elevation and land-cover data | Terrain and urban context |

The proposed workflow comprises data alignment and quality control, foundation-model adaptation for surface concentration regression, daily map generation, and independent evaluation. Spatial and temporal splits will be designed to limit information leakage.

**Note:** Satellite atmospheric-column measurements, such as Sentinel-5P products, are not direct measurements of ground-level pollutant concentrations and require appropriate interpretation.

## Evaluation

Performance will be assessed at independent monitoring stations using **MAE, RMSE, and R²**, reported separately by pollutant and study area. The evaluation will also compare results with coarse-resolution baselines and inspect whether predicted spatial patterns are environmentally plausible.

The research target is to **match or improve baseline accuracy** while providing more spatially detailed maps. No model performance results are reported at this stage.

## Planned deliverables

- Reproducible benchmarks for foundation-model and baseline approaches.
- Daily georeferenced pollutant concentration maps.
- Evaluation metrics and spatial visualizations.
- Implementation code, reproducibility instructions, and a technical report.

## Project status

This repository is at the **proposal stage**. Model implementation, experimental results, dependencies, and execution instructions will be documented as they become available.

## Team

**Politecnico di Torino — Applied Data Science Project**

- **Seyedmostafa Seyedi:** Research, model development and training, documentation.
- **Cristian Sician:** Project coordination, data exploration, evaluation and testing.

## References

1. [Aurora: A Foundation Model of the Atmosphere](https://arxiv.org/abs/2405.13063)
2. [Towards a Unified Copernicus Foundation Model for Earth Vision](https://arxiv.org/abs/2503.11849)
3. [Urban Air Pollution Forecasting: A Machine Learning Approach Leveraging Satellite Observations and Meteorological Forecasts](https://arxiv.org/abs/2405.19901)

**License:** Not yet specified. Data and pretrained models remain subject to their respective usage terms.
