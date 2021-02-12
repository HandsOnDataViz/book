## Other Leaflet templates (previously from ch 10)



## Leaflet Thematic Polygon Map with Clickable Info Window template {- #leaflet-polygon-map-click}
TODO: Decide whether to keep or not

Try it:
<iframe src="https://handsondataviz.github.io/leaflet-map-polygon-click/" width="100%" height=550></iframe>

#### View demo in new page {-}
- https://handsondataviz.github.io/leaflet-map-polygon-click/

**To Do**

- Insert internal references to prior steps in this book. See the Edit and Host Code Templates section in this book.
- Requires a free GitHub account to host your own version on the web.

#### Create Your Own: Fork a copy of the code template on GitHub {-}
- https://github.com/handsondataviz/leaflet-map-polygon-click
- Remember, if you have already forked one copy, go to your GitHub repository Settings to rename it, or create a new GitHub repo and use GitHub Desktop to upload template Files

#### Obtain a polygon boundary map in GeoJSON format {-}
- Find open data repositories to download maps in geojson and other formats
- If map is in shapefile or KML or other format, convert with http://geojson.io or http://mapshaper.org
- Import polygon map into http://mapshaper.org. In this example, map filename is: ct-towns-simple.geojson
  - See tutorial on Mapshaper.org to delete unwanted data columns or simplify file size
  - Export as CSV to create generic spreadsheet of polygon names. In this example, column header is "town"

#### Prepare your spreadsheet data and join with the polygon map {-}
- Open CSV with any spreadsheet tool to view data column of polygon names.
- Download or prepare your new spreadsheet data in rows to match polygon names.
- Insert columns of data into the CSV sheet. Use VLOOKUP function if needed.
- Save CSV with new name. In this example: ct-towns.csv
- Import ct-towns.csv as second layer into MapShaper.org.
- Use the drop-down to select the polygon map (ct-towns-simple.geojson) as the active, displayed layer.
- Click the Console and enter command to join the CSV table to the GeoJSON polygon, where the matching data columns are both named "town"
  ```
  -join ct-towns.csv keys=town,town
  ```
- Export the newly joined map with a new filename in GeoJSON format
- Change the file suffix from .json to .geojson to avoid confusion. The new joined map data file is now named: ct-towns-density.geojson

#### Upload your map data and edit template in your GitHub repo {-}
- The GitHub repo you created in the first step contains these files:
  - ct-towns-density-2010.csv (the spreadsheet joined into the polygon map)
  - ct-towns-density.geojson  (the joined map data file)
  - index.html  (the primary web page)
  - script.js   (code to operate the map, to be modified below)
  - style.css   (code that styles the map)
  - README.md   (edit to insert a link to your own version)
  - LICENSE     (terms of use for this free and open-source code)

- Upload your own map data geojson file
- Recommended: upload your own CSV spreadsheet file to
- In the script.js file, look for code comments labeled "Edit" to change references to geojson map data and its column headers, and also colors and ranges for the polygons and legend
- In GitHub, go to Branches and delete the existing "gh-pages" branch
- In GitHub, go to drop-down menu for Master branch, and type "gh-pages" to create new branch
- Content in the gh-pages branch will be hosted on the live web
- Edit the README.md link to point to your own gh-pages branch, in this format:
  `https://USERNAME.github.io/REPO-NAME/`


## Leaflet Thematic Polygon Map with Hover Info Window template {- #leaflet-polygon-map-hover}
TODO: Decide whether to keep or not

Try it:
<iframe src="https://handsondataviz.github.io/leaflet-map-polygon-hover/" width="100%" height=550></iframe>

#### View demo in new page {-}
- https://handsondataviz.github.io/leaflet-map-polygon-hover/

**To Do**

- Insert internal references to prior steps in this book. See the Edit and Host Code Templates section in this book.
- Requires a free GitHub account to host your own version on the web.

#### Create Your Own: Fork a copy of the code template on GitHub {-}
- https://github.com/handsondataviz/leaflet-map-polygon-hover/
- Remember, if you have already forked one copy, go to your GitHub repository Settings to rename it, or create a new GitHub repo and use GitHub Desktop to upload template Files

**TO DO**
- describe all steps, which are similar to click version



## Leaflet Thematic Polygon Map with Multi-Year Tabs template {- #leaflet-polygon-map-multi-year-tabs}
TODO: decide whether to keep or not

Try it:
<iframe src="https://handsondataviz.github.io/leaflet-map-polygon-tabs/" width="100%" height=550></iframe>

#### View demo in new page {-}
- https://handsondataviz.github.io/leaflet-map-polygon-tabs/

** To Do **

- Insert internal references to prior steps in this book. See the Edit and Host Code Templates section in this book.
- Requires a free GitHub account to host your own version on the web.
- describe all steps, which are similar to the prior chapter

#### Create Your Own: Fork a copy of the code template on GitHub {-}
- https://github.com/handsondataviz/leaflet-map-polygon-tabs/
- Remember, if you have already forked one copy, go to your GitHub repository Settings to rename it, or create a new GitHub repo and use GitHub Desktop to upload template Files

#### EXTRAS to move or remove {-}

from Leaflet Maps with Google Sheets

[Video](https://youtube.be/kUEfB8wD3Vk)

- Best to show points, polygons, and/or polylines, with table of points in map view
- Free and open-source code template, built on Leaflet and linked to Google Sheets
- Fork the code and host your live map on the web for free with GitHub Pages
- Geocode location data with US Census or Google, using script inside the Google Sheet
- Easy-to-modify data labels and map options in Google Sheet tabs or uploaded CSV files
- Upload your polygon and polyline GeoJSON files, and custom markers, to your GitHub repo
- Show multiple polygon layers, each with their own color legend and ranges (numerical or text)
- Responsive design resizes your maps to display inside most mobile devices

<iframe width="560" height="315" src="https://www.youtube.com/embed/-nGdrzMuUnI?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
