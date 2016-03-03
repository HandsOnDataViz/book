# Convert and Create Map Data with GeoJson.io

## What is GeoJSON?
GeoJSON is a relatively new and increasingly popular open format for map data, which can include:
- points (such as address locations, expressed in longitude-latitude coordinates)
- polygons (such boundary lines, expressed as a series of coordinate points)
- polylines (such as streets, expressed as a series of coordinate points)
- additional info (such as names and labels, expressed as properties of any feature above)
and more.

One big advantage of GeoJSON map data is portability across many tools. GeoJSON files can be used with Leaflet map code, Google Maps JS API code, CartoDB map tools, and more. Also, when you upload GeoJSON files into a GitHub repository, they are automatically displayed on a map.

Click to view the code of this simple GeoJSON file in a GitHub repo:

Click to view the map of the same GeoJSON file on GitHub:

GeoJSON files must follow a specific format, which must include coordinate data. The file name may end with .geojson or .json.

GeoJSON stores coordinates in *longitude-latitude* format, the same order as X-Y points in mathematics, which is the opposite of Google Maps, which uses *latitude-longitude* format. For example, Hartford Connecticut is located at (-72.67, 41.76) in GeoJSON, but (41.76, -72.67) in Google Maps.

## What is GeoJSON.io?

Go to http://geojson.io to try this open-source web tool for creating and converting GeoJSON map data. The tool was originally developed by Tom MacWright, and is supported by Mapbox.com.

### Convert a CSV spreadsheet of points into GeoJSON



### Convert Shapefile or KML polygons into GeoJSON
Drag any of these common geography file formats into the map browser:
- Shapefile
- KML
- CSV
- GeoJSON
- and others

Save to convert from one format above to another

![](geojson-save-as.png)



Click between the JSON and Table tabs to view and modify the geographic info.

Use the drawing tools to create points, polygons, and polylines, and the Table tab to insert data properties.

*TO DO* Show more




[Improve this book:](../../gitbook/improve.md) Select text to insert comments, or suggest edits on GitHub.

[Data Visualization for All](http://datavizforall.org)
is copyrighted by [Jack Dougherty and contributors](../../introduction/who.md)
and distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0). You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizForAll.org.

![Creative Commons by-nc image](../../cc-by-nc.png)
