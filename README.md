sf-parks-and-slopes
======

With San Francisco being known for its hills, I thought it would be neat to map the larger slopes in the city along with the parks/recreation areas.

## Data used (all from [DataSF](https://datasf.org/opendata/)):
* San Francisco Neighborhoods - https://data.sfgov.org/Geographic-Locations-and-Boundaries/SF-Find-Neighborhoods/pty2-tcw4
* Slopes of 20 Percent or Greater - https://data.sfgov.org/Geographic-Locations-and-Boundaries/Slopes-of-20-Or-Greater/3vv2-nvev 
* Park/Recreation Land - https://data.sfgov.org/Culture-and-Recreation/Park-Lands-Recreation-and-Parks-Department/42rw-e7xk

## Process:
* Inspected data to be used, added data to directory
* Installed GDAL/OGR 
* Got information on Shapefiles with ogrinfo, inspect CRS for each
* Used ogr2ogr to convert the parks Shapefile to WSG84 (was NAD83)
* Converted Shapefiles to GeoJSON using ogr2ogr
* Simplified slope lines with Mapshaper
* Created a Leaflet web map using VS Code
* Used jQuery for multiple asyncronous requests/drawing multiple GeoJSON files to the map
* Layered and styled mapped features
* Added labels on top of map
* Committed work along the way

## Commands used in Command Line:
* cd - change directory
* mkdir - add new directory
* git status - checking the status of working tree
* git add & git commit - committing changes
* dir - list contents of current directory
* ogrinfo -so - get information about shapefiles (so flag means summary only)
* ogr2ogr - make CRS transformations, also used to convert file formats
