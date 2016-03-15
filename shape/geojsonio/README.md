# Convert and Create Map Data with GeoJson.io

Go to http://geojson.io to explore this open-source web tool to convert, edit, and create GeoJSON map data. The tool was originally developed by Tom MacWright, and is supported by Mapbox.com.

### Convert a CSV spreadsheet of point data into GeoJSON

Use any spreadsheet tool and prepare a list of coordinate points (known as features). You must include column headers **lat** and **lon**, or a fuller spelling, such as *latitude* and *longitude*. The order of the columns does not matter. Also, you can add more headers to identify each point (example: name) and include more details (known as the properties of the features).

![](name-lat-lon-info.png)

Save your spreadsheet in generic CSV format. *Hint:* see [Save Spreadsheet as CSV chapter](../../transform/csv/index.html) in this book.

Example: download this [sample CSV file](name-lat-lon-info.csv)

Drag the CSV file into the GeoJSON.io map window. Flip between the JSON and Table tabs to view or edit the data.

![](dataviz-geojsonio-640.gif)

Select the Save menu and export into GeoJSON format.

Optional: Login to GeoJSON.io with your GitHub account and save directly to your repository.


### Convert Shapefile or KML polygons into GeoJSON

Polygon boundary data is often shared as ArcGIS Shapefiles (.shp) or Keyhole Markup Language (.kml) files. Drag any of these (and other) files into the http://GeoJSON.io map window. Flip between the JSON and Table tabs to view or edit the data.

Select the Save menu and export into GeoJSON format.

![](geojson-save-as.png)

### Create GeoJSON data with drawing tools

Use the http://GeoJSON.io drawing tools to create points, polygons, and polylines. Flip between the JSON and Table tabs to view or edit the data.

### Learn more about GeoJSON.io

Read about more advanced features and view the code at https://github.com/mapbox/geojson.io




[Improve this book:](../../gitbook/improve.md) Select text to insert comments, or suggest edits on GitHub.

[Data Visualization for All](http://datavizforall.org)
is copyrighted by [Jack Dougherty and contributors](../../introduction/who.md)
and distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0). You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizForAll.org.

![Creative Commons by-nc image](../../cc-by-nc.png)
