# Convert Map Data into GeoJSON format
*By [Jack Dougherty](../../introduction/who.md), last updated March 26, 2017*

## GeoJSON

GeoJSON is a relatively new and increasingly popular open format for map data. One advantage is its portability across many tools. GeoJSON files can be used with Leaflet map code, Google Maps JS API code, CartoDB map tools, and more. Also, your GitHub repository will automatically display any GeoJSON files in a map view. Click to view this [simple GeoJSON point data file on GitHub](https://github.com/JackDougherty/datavizforall/blob/master/shape/geojsonio/name-lat-lon-info.geojson).

GeoJSON data must follow a [structured format](http://geojson.org/), but the file name may end with either .geojson or .json.

The GeoJSON structured format orders coordinates in *longitude-latitude* format, the same as X-Y coordinates in mathematics. This is the opposite of Google Maps and several other web map tools, which order points in *latitude-longitude* format. For example, Hartford Connecticut is located at (-72.67, 41.76) in GeoJSON, but (41.76, -72.67) in Google Maps.


## Shapefiles

The shapefile format was created in the 1990s by ESRI, the company that developed ArcGIS software. Shapefiles typically appear as a folder of subfiles with suffixes such as .shp, .shx, .dbf, and others. Although government agencies commonly distribute map data in shapefile format, the standard tools for editing these files -- ArcGIS and its free and open-source cousin, QGIS -- are not as easy to learn as other tools in this book. For this reason, this book recommends converting shapefiles into one of the more friendlier formats below.

## Keyhole Markup Language (or KML)

The KML format rose in popularity during the late 2000s. Google Earth, a free and user-friendly tool, allowed many people to view and edit geographic data. KML files are commonly used in the Google Fusion Tables maps described in this book. Sometimes .kml files are distributed in a compressed .kmz format. See the chapter on [converting from KMZ to KML format](convert-kmz/index.html) in this book.

##
