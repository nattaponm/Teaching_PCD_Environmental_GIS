# Teaching PCD Environmental GIS — Dataset v1

Canonical teaching dataset for Python, Pandas, GeoPandas,
air-quality GIS, meteorological station analysis,
spatiotemporal analysis, and spatial statistics.

## Build

- Dataset version: v1
- Build UTC: 2026-08-22T11:31:27.298476+00:00
- Course repository: https://github.com/nattaponm/Teaching_PCD_Environmental_GIS

## PCD raw teaching workbooks

- 2021.xlsx
- 2022.xlsx
- 2023.xlsx
- 2024.xlsx
- 2025.xlsx

Source:
nattaponm/training_PCD_data_GIS

## PCD/Air4Thai station layer

- processed/pcd_air4thai_stations.csv
- processed/pcd_air4thai_stations.geojson
- GeoPackage layer: pcd_stations

Station count:
173

## Thailand meteorological-station network

- processed/thailand_meteorological_stations_from_course_sources.csv
- processed/thailand_meteorological_stations_from_course_sources.geojson
- GeoPackage layer: met_stations_thailand

Active station count found in the embedded course source:
140

## OGIMET/WMO station layer

- processed/ogimet_wmo_stations_from_course_sources.csv
- processed/ogimet_wmo_stations_from_course_sources.geojson
- GeoPackage layer: ogimet_stations

Station count:
130

Important:
This station list is collected from existing course sources.
Do not describe it as a complete national WMO network
unless separately verified.

## Thailand administrative GIS

Source:
https://github.com/prasertcbs/thailand_gis

Canonical file:
processed/environmental_gis_course.gpkg

Layers:
- province
- amphoe
- tambon
- pcd_stations
- ogimet_stations

Canonical CRS:
EPSG:4326

## Student-use principle

Student notebooks should use the canonical course packages
from Teaching_PCD_Environmental_GIS and should not
re-download external environmental datasets.

## QC and provenance

See files under metadata/.
