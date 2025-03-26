# NetCDF-Python-Analysis
This repository contains Jupyter notebooks demonstrating how to manipulate, analyze, and visualize NetCDF files using Python. The examples focus on working with output files from the Weather Research and Forecasting (WRF) model, providing practical approaches for handling meteorological and environmental data.

<a href="https://drive.google.com/drive/folders/1rh2C5JX2ukLF_9G08z7Uj5OwgOCWfR9W" target="_blank">Link repositorio archivos NetCDF</a>

[Taller](https://github.com/kballesterosg/NetCDF-Python-Analysis/blob/main/Taller___Uniandes.pdf)


# Variables meteorológicas en archivos de salida WRF (`wrfout`)

| Nombre común           | Nombre en WRF (`wrfout`) | Descripción breve                                           | Unidades                         |
|------------------------|--------------------------|-------------------------------------------------------------|----------------------------------|
| Temperatura 2m         | T2                       | Temperatura del aire a 2 metros sobre el suelo              | Kelvin (K)                       |
| Temperatura del suelo  | TSK                      | Temperatura de la superficie terrestre                      | Kelvin (K)                       |
| Humedad relativa 2m    | RH2                      | Humedad relativa al nivel de 2 metros                       | %                                |
| Presión a nivel del mar| PMSL                     | Presión al nivel medio del mar                              | hPa (mb)                         |
| Presión superficial    | PSFC                     | Presión en la superficie del modelo                         | Pa                               |
| Viento U 10m           | U10                      | Componente U del viento a 10 metros                         | m/s                              |
| Viento V 10m           | V10                      | Componente V del viento a 10 metros                         | m/s                              |
| Velocidad del viento   | -                        | Calculada a partir de U10 y V10                             | m/s                              |
| Dirección del viento   | -                        | Calculada a partir de U10 y V10                             | grados (°)                       |
| Radiación solar        | SWDOWN                   | Radiación solar descendente en la superficie                | W/m²                             |
| Nubosidad              | CLDFRA                   | Fracción de nubosidad en cada nivel                         | fracción (0 a 1)                 |
| Precipitación acumulada| RAINNC                   | Precipitación acumulada (no convectiva)                     | mm                               |
| Precipitación convectiva| RAINC                   | Precipitación acumulada (convectiva)                        | mm                               |
| Altura geopotencial    | PH, PHB                  | Altura geopotencial perturbada y base                       | m²/s² (requiere cálculo para z)  |
| Altura sobre el nivel del mar | HGT              | Elevación del terreno del modelo                            | m                                |
| Coordenadas de latitud | XLAT                     | Latitud de cada punto de la malla                           | grados decimales (°)             |
| Coordenadas de longitud| XLONG                    | Longitud de cada punto de la malla                          | grados decimales (°)             |

> Nota: Algunas variables como velocidad o dirección del viento deben calcularse a partir de los componentes U y V.
