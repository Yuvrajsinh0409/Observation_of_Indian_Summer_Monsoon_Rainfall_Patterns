# Observation of Indian Summer Monsoon Rainfall Patterns

Research project analyzing spatio-temporal precipitation trends over the Indian subcontinent using satellite data from TRMM and GPM missions.

## Overview

This project performs diurnal trend analysis of extreme precipitation indices across India using 25+ years of satellite data (1998–2023). We apply non-parametric statistical methods to detect and quantify rainfall trends at 3-hour intervals across the Indian region — contributing insights relevant to flood prediction, agricultural planning, and climate adaptation.

This work resulted in two peer-reviewed publications presented at **IEEE CCIS 2024**.

## Published Papers

- **Diurnal Spatiotemporal Analysis of TRMM and GPM Satellite Data on Indian Region**
  Khyati Amin, Amit Thakkar, Yuvrajsinh Bodana, Hiteshri Shastri, Heli Hingrajiya
  *IEEE CCIS 2024* — DOI: [10.1109/CCIS63231.2024.10931871](https://doi.org/10.1109/CCIS63231.2024.10931871)

- **Hourly Trend Analysis of Spatio-temporal Precipitation Extremes Using TRMM and GPM Satellite Data on ETCCDI Indices for the Indian Region**
  Heli Hingrajiya, Amit Thakkar, Yuvrajsinh Bodana, Hiteshri Shastri, Khyati Amin
  *IEEE CCIS 2024* — DOI: [10.1109/CCIS63231.2024.10931921](https://doi.org/10.1109/CCIS63231.2024.10931921)

## Datasets

| Satellite | Period | Temporal Resolution | Spatial Resolution |
|-----------|--------|--------------------|--------------------|
| TRMM | 1997–2019 | 3-hour | 0.25° |
| GPM | 2020–present | 0.5-hour (resampled to 3-hour) | 0.1° |

Data was sourced from NASA's publicly available TRMM and GPM databases. Temporal interpolation was applied to standardize GPM to 3-hour intervals to maintain consistency with TRMM.

## Methodology

- **Diurnal stacking**: Satellite data organized into 8 three-hour time slots (00th–21st hour) per year
- **Mann-Kendall Test**: Non-parametric trend detection across each grid cell
- **Sen's Slope Estimator**: Quantifies the magnitude and direction of detected trends
- **ETCCDI Indices analyzed**:
  - RX1day, RX5day (maximum 1-day and 5-day precipitation)
  - r10mm, r20mm (heavy and very heavy precipitation days)
  - r95p, r99p (very wet and extremely wet days)
  - CDD, CWD (consecutive dry and wet days)

## Key Findings

- Precipitation shows an **upward trend during late night and early morning hours** (21:00–09:00) and a sharp decrease in the afternoon across most of India
- **West Rajasthan, West Gujarat, NW Jammu & Kashmir, and the Western Coast** show consistent upward trends across all indices and hours
- **West Bengal and North-East India** show the most significant decreasing rainfall trends
- A notable **shift in extreme rainfall activity from the Bay of Bengal toward the Arabian Sea** is observed in recent years
- GPM data confirms the coastal border of India has seen increased multi-day consecutive rainfall events, primarily during dawn hours

## Tech Stack

- **Languages**: Python
- **Data processing**: Climate Data Operators (CDO), NumPy, Pandas
- **Geospatial**: Gridded satellite data processing (0.1°–0.25° resolution)
- **Statistical methods**: Mann-Kendall, Sen's Slope, Yue-Wang, Hamed-Rao, Pre-Whitening tests
- **Visualization**: Matplotlib, spatial grid plots

## Authors

Khyati Amin · Yuvrajsinh Bodana · Heli Hingrajiya · Hiteshri Shastri
Guided by Dr. Amit Thakkar — CHARUSAT University, India
