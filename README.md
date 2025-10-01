# Water Temperature Estimation using Landsat-8 & Landsat-9
## Overview
This repository presents an analysis of surface water temperature estimation using Landsat-8 OLI/TIRS and Landsat-9 OLI-2/TIRS-2 data.
The workflow applies cloud and cirrus masking, water body detection using the Normalized Difference Water Index (NDWI), and retrieval of surface temperature (ST_B10) from Landsat thermal bands.
By combining cloud-free water pixels from both Landsat-8 and Landsat-9 (2024–2025), this study generates spatiotemporal water temperature maps and time series for a user-defined Region of Interest (ROI) in Sri Lanka.
This approach provides valuable insights for water quality monitoring, climate variability studies, aquatic ecosystem management, and resource planning.

## Datasets Used
1. Landsat-8 Collection 2 Level-2 (LC08/C02/T1_L2)
 - Surface reflectance & thermal band data (30m resolution).
 - ST_B10 used for Land/Water Surface Temperature (LST/WST).

2. Landsat-9 Collection 2 Level-2 (LC09/C02/T1_L2)
 - Similar specifications to Landsat-8.

3. Time Period: January 2024 – December 2025


### Water Temperature Maps (July 2024–2025): Contour-filled maps showing spatial variation in surface water temperature.
<img width="925" height="590" alt="image" src="https://github.com/user-attachments/assets/0c6a1d40-3152-4e92-8687-462ac14484ba" />

### Smoothed Water Temperature Maps:7-day rolling averages highlighting seasonal dynamics.
<img width="959" height="590" alt="image" src="https://github.com/user-attachments/assets/054c6319-1ffa-4ca2-9f3e-990738edadf7" />

### Time Series Plot:Mean water temperature trends across the ROI.
<img width="571" height="416" alt="image" src="https://github.com/user-attachments/assets/7c2c4d08-60fb-4e53-a6d3-7e28c9e207a2" />

## Tools & Libraries
1. Google Earth Engine (GEE): Remote sensing data access & processing.
2. Python API (xee): Bridge between Earth Engine and xarray.
3. geemap: Interactive ROI selection & GEE integration.
4. xarray: Multidimensional data handling.
5. matplotlib: Visualization of maps & time series.

 ## Notes & Considerations
a. Only open-water pixels are considered (NDWI masking).
b. Clouds and shadows are masked to avoid erroneous values.
c. Water bodies with small surface area may appear noisy due to pixel size (30m).
d. Surface temperature retrieval assumes atmospheric correction applied in Level-2 data.

 ## References
1. USGS Landsat-8/9 Collection 2 Level-2 Science Products Documentation.
2. Gao, B. (1996). NDWI – A Normalized Difference Water Index for Remote Sensing of Water Resources. Remote Sensing of Environment.
3. Weng, Q. et al. (2004). Estimation of land surface temperature from Landsat ETM+ data. Remote Sensing of Environment.
