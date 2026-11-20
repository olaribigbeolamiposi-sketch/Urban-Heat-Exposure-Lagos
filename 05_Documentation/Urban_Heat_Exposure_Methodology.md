# Urban Heat Exposure Analysis — Lagos State, Nigeria

## 1. Project Overview

This project examines the spatial distribution of land surface temperature (LST) and vegetation cover across Lagos State, Nigeria, using Landsat 8/9 satellite imagery and Geographic Information Systems (GIS).

The analysis identifies relative surface-temperature patterns, assesses vegetation distribution, compares observed conditions across 20 Local Government Areas (LGAs), and investigates the relationship between NDVI and LST.

## 2. Study Area

**Location:** Lagos State, Nigeria

**Administrative units:** 20 LGAs

**Coordinate reference system:** WGS 1984 UTM Zone 31N

## 3. Data Sources

- USGS Landsat 8/9 Collection 2 Level-2 satellite imagery
- Lagos State administrative boundary
- Lagos LGA administrative boundaries
- ArcGIS Pro for geospatial processing and visualization

Three Landsat scenes acquired on January 28, February 5 and February 6, 2026, were used.

## 4. Methodology

### 4.1 Land Surface Temperature

Landsat surface-temperature Band 10 (ST_B10) data were converted to degrees Celsius using the published scale factor and offset.

The resulting temperature rasters were extracted to the Lagos State boundary and combined into a multi-date composite using the mean mosaic method.

### 4.2 Vegetation Analysis

The Normalized Difference Vegetation Index (NDVI) was calculated using Landsat red and near-infrared surface-reflectance bands, with quality masking applied.

The three NDVI scenes were clipped to Lagos State and combined into a multi-date vegetation composite.

### 4.3 Relative Heat Classification

The composite LST raster was classified into five relative temperature categories using an equal-area classification method:

1. Relatively coolest
2. Lower temperature
3. Moderate temperature
4. Higher temperature
5. Relatively hottest

These classes describe relative surface-temperature conditions rather than absolute heat-risk thresholds.

### 4.4 LGA-Level Analysis

Zonal statistics were used to calculate mean LST and NDVI values for Lagos State's 20 LGAs.

Valid-data coverage percentages were calculated to help assess the reliability and representativeness of LGA comparisons.

### 4.5 Vegetation–Temperature Correlation

Scatter plots and linear trendlines were used to examine the relationship between mean NDVI and mean LST.

Two comparisons were conducted:

- All 20 Lagos LGAs
- Eight LGAs with at least 50% valid coverage for both LST and NDVI

## 5. Key Findings

- **20 LGAs** were included in the analysis.
- Highest observed mean LST values included Agege (40.39°C), Ifako/Ijaye (40.06°C) and Surulere (40.06°C).
- Lowest observed mean LST values included Epe (32.52°C), Ibeju-Lekki (33.42°C) and Badagry (33.82°C).
- The all-LGA NDVI–LST correlation had an R² of approximately **0.69**.
- The eight-LGA coverage-filtered comparison had an R² of approximately **0.82**.
- Higher vegetation cover was generally associated with lower observed land surface temperatures.
- **786 pixels above 50°C** were flagged during the temperature quality review.

## 6. Limitations

The three Landsat scenes were acquired on different dates and therefore do not represent simultaneous conditions across Lagos State.

Some LGAs had incomplete valid raster coverage, which limits direct comparisons between locations.

Extreme temperature values require cautious interpretation because satellite and processing artifacts may affect individual pixels.

Land surface temperature describes the temperature of observed surfaces, not ambient air temperature.

The observed NDVI–LST relationship is correlational and does not independently establish causation.

## 7. Outputs

The project produced:

- Five-class relative urban heat map
- Multi-date NDVI vegetation map
- LGA-level temperature and vegetation statistics
- NDVI–LST correlation charts
- High-temperature quality-review dataset
- Final A3 landscape map in PDF and PNG formats

## 8. Conclusion

The analysis indicates spatial variation in observed land surface temperature across Lagos State and an inverse association between vegetation cover and surface temperature.

The findings provide a GIS-based overview of urban heat patterns while highlighting the importance of accounting for satellite data coverage and quality when interpreting local temperature differences.