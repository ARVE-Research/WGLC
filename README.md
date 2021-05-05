# WGLC
## The WWLLN Global Lightning Climatology and timeseries

This repository contains global lightning stroke density and stroke power calculated from georeferenced stroke count data from the World Wide Lightning Location Network (WWLLN). The real-time raw stroke count data were reprocessed by WWLLN to remove artifacts and improve geolocation, which resulted in the "AE" georeferenced and timestamped stroke count data. These data were then gridded at 0.5 degree 5 arc-minute and hourly resolution, converted into density, and corrected for detection efficiency using the WWLLN global gridded detection efficiency maps. Mean, median, and standard deviation of stroke power are also provided at 30-minute resolution. The corrected hourly rasters were then aggregated into monthly totals and into a multi-year monthly mean climatology. The data cover the period 2010-2020 and will be updated in the coming years.

For a complete description of the data see:

Kaplan, J. O., & Lau, K. H.-K. (2021). The WGLC global gridded lightning climatology and timeseries. *Earth Syst. Sci. Data Discuss.*, 2021, 1-25. [doi:10.5194/essd-2021-89](https://doi.org/10.5194/essd-2021-89)
 
The data are stored in a [NetCDF](https://www.unidata.ucar.edu/software/netcdf/) (version 4) files and have the following attributes:

- Spatial extent: Entire Earth
- Spatial reference system (SRS): Unprojected (geographic, WGS84)
- Spatial resolution: available in two resolutions; see table below
- Temporal extent: 2010-2020
- Temporal resolution: See "timestep" below

**Variables included in this release**
| Variable | Description | Units | Timestep<sup>1</sup> | Spatial resolution |
| -------------- | ----------- | ----- | -------- | ------------------ |
| density        | lightning stroke density  | strokes km<sup>-2</sup> d<sup>-1</sup>  | day, month  | 30 minute, 5 minute |
| power_mean     | mean stroke power | MW | month | 30 minute |
| power_median   | median stroke power  | MW  | month | 30 minute |
| power_SD       | standard deviation of stroke power  | MW | month  | 30 minute  |

<sup>1</sup>4018 elements in the time dimension for daily data; 108 for monthly data; 12 for the climatology

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
