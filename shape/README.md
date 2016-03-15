# Shape Your Map Data

Interactive digital maps are made of different data layers. Generally speaking, at the bottom is the basemap, a layer of tiles that display the background imagery. On top of the basemap, we can place additional layers of map data, such as address points or polygon boundaries. All of these layers are connected with controls that allow us to seamlessly zoom or pan around the map.

** TO DO ** insert illustration for above

These top-most data layers come in various formats, designed for different generations of digital mapping tools over time. The three most common formats mentioned in this book are:

## Shapefiles

The shapefile format was created in the 1990s by ESRI, the company that developed ArcGIS software. Shapefiles typically appear as a folder of subfiles with suffixes such as .shp, .shx, .dbf, and others. Although government agencies commonly distribute map data in shapefile format, the standard tools for editing these files -- ArcGIS and its free and open-source cousin, QGIS -- are not as easy to learn as other tools in this book. For this reason, this book recommends converting shapefiles into one of the more friendlier formats below.

## Keyhole Markup Language (or KML)

The KML format rose in popularity during the late 2000s. Google Earth, a free and user-friendly tool, allowed many people to view and edit geographic data. KML files are commonly used in the Google Fusion Tables maps described in this book. Sometimes .kml files are distributed in a compressed .kmz format. See the chapter on [converting from KMZ to KML format](convert-kmz/index.html) in this book.

## GeoJSON

GeoJSON is a relatively new and increasingly popular open format for map data. One advantage is its portability across many tools. GeoJSON files can be used with Leaflet map code, Google Maps JS API code, CartoDB map tools, and more. Also, your GitHub repository will automatically display any GeoJSON files in a map view. Click to view this [simple GeoJSON point data file on GitHub](https://github.com/JackDougherty/datavizforall/blob/master/shape/geojsonio/name-lat-lon-info.geojson).

GeoJSON data must follow a [structured format](http://geojson.org/), but the file name may end with either .geojson or .json.

The GeoJSON structured format orders coordinates in *longitude-latitude* format, the same as X-Y coordinates in mathematics. This is the opposite of Google Maps and several other web map tools, which order points in *latitude-longitude* format. For example, Hartford Connecticut is located at (-72.67, 41.76) in GeoJSON, but (41.76, -72.67) in Google Maps.

*TO DO*
- insert some of this above?
- points (such as address locations, expressed in longitude-latitude coordinates)
- polygons (such boundary lines, expressed as a series of coordinate points)
- polylines (such as streets, expressed as a series of coordinate points)
- additional info (such as names and labels, expressed as properties of any feature above)
and more.
