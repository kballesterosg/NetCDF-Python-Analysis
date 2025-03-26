# NetCDF-Python-Analysis
This repository contains Jupyter notebooks demonstrating how to manipulate, analyze, and visualize NetCDF files using Python. The examples focus on working with output files from the Weather Research and Forecasting (WRF) model, providing practical approaches for handling meteorological and environmental data.

<a href="https://drive.google.com/drive/folders/1rh2C5JX2ukLF_9G08z7Uj5OwgOCWfR9W" target="_blank">Link repositorio archivos NetCDF</a>

[Taller](https://github.com/kballesterosg/NetCDF-Python-Analysis/blob/main/Taller___Uniandes.pdf)


# Meteorological Variables in WRF Output Files (`wrfout`)

| Common Name              | WRF Variable Name (`wrfout`) | Brief Description                                           | Units                           |
|--------------------------|------------------------------|-------------------------------------------------------------|----------------------------------|
| 2-meter Temperature      | T2                           | Air temperature at 2 meters above ground                    | Kelvin (K)                       |
| Surface Temperature      | TSK                          | Skin (land surface) temperature                             | Kelvin (K)                       |
| 2-meter Relative Humidity| RH2                          | Relative humidity at 2 meters                               | %                                |
| Sea Level Pressure       | PMSL                         | Mean sea level pressure                                     | hPa (mb)                         |
| Surface Pressure         | PSFC                         | Atmospheric pressure at the surface                         | Pa                               |
| 10-meter U Wind          | U10                          | U-component (east-west) wind at 10 meters                   | m/s                              |
| 10-meter V Wind          | V10                          | V-component (north-south) wind at 10 meters                 | m/s                              |
| Wind Speed               | -                            | Calculated from U10 and V10                                 | m/s                              |
| Wind Direction           | -                            | Calculated from U10 and V10                                 | degrees (°)                      |
| Downward Shortwave Radiation | SWDOWN                | Incoming solar radiation at the surface                     | W/m²                             |
| Cloud Fraction           | CLDFRA                       | Cloud fraction at each model level                          | fraction (0 to 1)                |
| Accumulated Precipitation| RAINNC                       | Accumulated (non-convective) precipitation                  | mm                               |
| Convective Precipitation | RAINC                        | Accumulated convective precipitation                        | mm                               |
| Geopotential Height      | PH, PHB                      | Perturbation and base geopotential height (requires calc)   | m²/s² (calculate for height)     |
| Terrain Height           | HGT                          | Elevation of the model terrain                              | meters (m)                       |
| Latitude Coordinates     | XLAT                         | Latitude at each grid point                                 | decimal degrees (°)              |
| Longitude Coordinates    | XLONG                        | Longitude at each grid point                                | decimal degrees (°)              |

> Note: Some variables, such as wind speed and direction, must be derived from the U and V wind components.

