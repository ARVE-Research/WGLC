# WGLC
The WWLLN Global Lightning Climatology

This repository contains global lightning stroke density and stroke power calculated from georeferenced stroke count data from the World Wide Lightning Location Network (WWLLN). The real-time raw stroke count data were reprocessed by WWLLN to remove artifacts and improve geolocation, which resulted in the "AE" georeferenced and timestamped stroke count data. These data were then gridded at 0.5 degree 5 arc-minute and hourly resolution, converted into density, and corrected for detection efficiency using the WWLLN global gridded detection efficiency maps. Mean, median, and standard deviation of stroke power are also provided at 30-minute resolution. The corrected hourly rasters were then aggregated into monthly totals and into a multi-year monthly mean climatology. The data cover the period 2010-2020 and will be updated in the coming years.
 
The data are stored in a NetCDF (version 4) files and have the following attributes:

- Spatial extent: Entire Earth
- Spatial reference system (SRS): Unprojected (geographic, WGS84)
- Spatial resolution: available in two resolutions; see table below
- Temporal extent: 2010-2020
- Temporal resolution: See "timestep" below

*Variables included in this release*
| Variable | Description | Units | Timestep | Spatial resolution |
| -------------- | ----------- | ----- | -------- | ------------------ |
| density        | lightning stroke density  | strokes km<sup>-2</sup> d<sup>-1</sup>  | day, month  | 30 minute, 5 minute |
| power_mean     | mean stroke power | MW | month | 30 minute |
| power_median   | median stroke power  | MW  | month | 30 minute |
| power_SD       | standard deviation of stroke power  | MW | month  | 30 minute  |

(4018 time steps for daily data; 108 for monthly data; 12 for the climatology)

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].
