#Edit, Dissolve, and Join with MapShaper.org

*By [Jack Dougherty](../../introduction/who.md), last updated March 30, 2016*

MapShaper (http://MapShaper.org) is another versatile open-source mapping tool, developed and maintained by [Matthew Bloch on GitHub](https://github.com/mbloch/mapshaper). Using the web interface, users can:
- Import and export map layers in multiple formats: Shapefile, GeoJSON, CSV, and more
- Simplify (or smooth out) geographic details to reduce map file size
- Edit geography with powerful commands (dissolve, clip, join files, etc.)

This free and easy-to-learn MapShaper.org web tool has replaced *many* of my map preparation tasks that previously required expensive and hard-to-learn ArcGIS software, or its free but still-challenging-to-learn cousin, QGIS. Even advanced GIS users may discover MapShaper.org to be a quick alternative for some common time-consuming tasks.

The examples below focus on polygon boundary data to illustrate common map editing tasks. But MapShaper.org also works with other data layers, such as tables, points, and lines.

##Import and convert map boundary files

To follow the next few examples below, download the [Connecticut town boundary map in GeoJSON format](CT-towns.geojson).

1. Drag any map layer into the http://MapShaper.org browser window.
  - Import GeoJSON (.geojson or .json), TopoJSON, CSV, or Shapefile formats
  - For Shapefiles, import the .shp (features), .dbf (attribute data), and .prj (projection) files. Reminder: the WGS84 projection is most portable across multiple platforms.

2. Click the Export button and select Shapefile, GeoJSON, TopoJSON, or CSV

  ![](mapshaper-convert-640.gif)

##Edit data for specific polygons

To edit data for any polygon in MapShaper.org:
- Click the "i" information button
- Select the polygon
- Click inside its pop-up info window to directly edit the data

  ![](mapshaper-edit-info.png)

##Simplify map boundaries to reduce file size

If your data visualization project displays a zoomed-out state or national or world map, small geographic details that are invisible at these zoom levels may not be necessary. Consider using the Simplify command to reduce the file size, which may help your interactive web map to load faster for web visitors. The example below began with a detailed map of Connecticut town boundaries (1:100,000 scale) at 2MB, which MapShaper simplified -- without visibly sacrificing details at the statewide zoom level -- to a reduced size of about 200KB.

1. Import the map layer as described above. Click the Simplify button to review options, and in most cases, accept the default settings. Click Next.

2. Slide the Simplify button from 100 percent down to an appropriate number for your map zoom level. If important geographic details disappear, you may have gone too far.

3. Look in the upper-left corner and click on recommended Repairs to your map file.

4. Complete the process by clicking Simplify once again. Export your file in the preferred format for your project.

![](mapshaper-simplify.png)

##Dissolve internal polygons to create an outline map
MapShaper.org also includes a Console button to type in commands for common map editing tasks. Imagine that you begin with a boundary map that includes internal polygons, but your goal is to remove all of them to create an outline map.

Click the Console button, which opens a window to type in commands. Enter the command below, then press return. Close the Console window and Export your outline map.

```
-dissolve
```

![](mapshaper-dissolve-simple-640.gif)

##Clip a map to match an outline layer
Imagine that you start with a polygon map of all towns in Connecticut, and an outline map of Hartford County, a larger region that includes some (but not all) of those smaller towns. Your goal is to create a polygon map of all towns inside Hartford County. In other words, we will "clip" the statewide town map using the county outline map.

To follow this example, download the [Connecticut towns map](CT-towns.geojson) and the [Hartford County outline map](HartfordCounty.geojson), both in GeoJSON format. (If necessary, right-click or control-click on each link to save each file.)

Refresh the browser to start a new session in http://MapShaper.org.

1. Drag the CT-towns.geojson map to import to MapShaper.

2. Drag the HartfordCounty.geojson map to MapShaper, and click Import to add this second layer.

3. In the drop-down menu, select the first map (CT-towns) to display it as the active layer.

4. Click the Console button, type or paste in the command below, and press enter.
```
-clip HartfordCounty.geojson
```

5. The command above instructs MapShaper to clip the active map layer (CT Towns) using the second layer (the outline of Hartford County).

![](mapshaper-clip-640.gif)


##Remove unwanted data columns

If your polygon map contains unwanted data columns, enter the "-filter-fields" Console command to keep only the columns you list. The example below deletes all columns *except* "town":

```
-filter-fields town
```

##Join data columns with a polygon map

A common mapping task is to join (or merge) new data columns into a polygon boundary map, and MapShaper.org makes this very easy. Imagine that you have two files:
- Connecticut town boundary map
- a spreadsheet of town population data

Your goal is to unite these files, so that you can later display them in a thematic polygon map. Since these two files share a common column of data -- the town names -- you can join them together into one merged file.

![](mapshaper-join-table-concept.png)

To follow this example, download two files:
- [Connecticut towns simplified map in GeoJSON format](CT-towns-simple.geojson)
- [Connecticut towns population data in CSV format](CT-towns-popdensity.csv)

If necessary, right-click or control-click on the links to save each file.

Refresh the browser to start a new session in http://MapShaper.org.

1. Drag the CT-towns-simple.geojson boundary file into MapShaper. Select the "i" info button and click on any polygon to confirm that the column header is "town".

2. Open the CT-towns-popdensity.csv file with any spreadsheet tool and confirm that first column header also is "town". Close this file.

3. Drag the CT-towns-popdensity.csv file into MapShaper.org, and select the Import button to add it as a second layer. This table layer will appear as rectangular cells, because it does not contain geographic information.

4. Click the drop-down menu and select the map to display it as the active layer.

  ![](mapshaper-join-select-map-layer.png)

5. Click the Console button, type this command, and press return:
```
-join CT-towns-popdensity.csv keys=town,town
```
This command instructs MapShaper to join the active map layer to the CSV table layer, based on their shared column of data, labeled as "town" in both files. In this example, 169 rows are merged together.

  ![](mapshaper-join-console.png)

6. Click the Console button to close the command window. Select the "i" info button and click any polygon to confirm that it now contains the new table data. Export the file in your preferred format.

  ![](mapshaper-join-confirm.png)

###More about joins

1. If you don't have a CSV table that matches the columns in your boundary map data, you can easily create one. Upload the boundary map to MapShaper.org, and export in CSV format, and open with any spreadsheet tool. To efficiently match data columns in the CSV spreadsheet, use the [VLOOKUP method in this book](../../transform/vlookup/index.html).

2. The simple join example above uses identical keys (town, town) because the two columns headers are the same. But if you need to join data where the headers are not the same, enter the first key (the polygon map) and the second key (the CSV table).

3. When joining data, keep track of the number of matching rows. For example, if the polygon map contains 169 rows (one for each town in Connecticut), but the CSV table contains only 168 rows of population data, MapShaper will join all of those with matching names, and then display this message:
```
Joined 168 data records
1/169 target records received no data
```

##Merge selected polygons with join and dissolve commands

 Another common task is to merge selected polygons in a boundary map, which you can do in MapShaper with the join and dissolve commands you learned above. Imagine that you wish to create regional "cluster" boundaries from smaller polygon areas. For example, the [Connecticut Department of Public Health](http://www.ct.gov/dph/cwp/view.asp?a=3123&q=397740) has grouped individual towns, such as Bloomfield and West Hartford, into regional health districts. Your task is to begin with a statewide polygon map of all town boundaries, and to create a new polygon map that displays these regional clusters.

 To follow this example, [download the Connecticut towns simplfied GeoJSON map file](CT-towns-simple.geojson). (If necessary, right-click or control-click on the link to save the file.)

 Refresh the browser to start a new session in http://MapShaper.org.

1. Import the CT-towns-simple.geojson map file into http://MapShaper.org.

2. Export in CSV format. This steps creates a spreadsheet that lists all of the polygon town names, without geographic details.

  ![](towns-export-csv.png)

3. Open the CSV file with any spreadsheet tool. Copy the contents of the "towns" column, paste it into a second column, and change the header of this second column to "merged".

4. In the new "merged" column, create new listings for towns you wish to merge together. In this example, Bloomfield and West Hartford are merged into Bloomfield-West Hartford. Leave other towns unchanged.

  ![](CT-towns-merged-csv.png)

5. Save this spreadsheet in CSV format with a new file name, such as: CT-towns-merged.csv.

6. Drag this new CT-towns-merged.csv file into MapShaper, and click Import.

7. Use the drop-down menu to manage multiple layers in MapShaper. Since the CSV file has no geography, it appears as a series of rectangular cells. Instead, select the CT-towns-simple.geojson map to display it as the active layer.

  ![](mapshaper-two-layers.png)

8. Click on the Console button, type in both of the commands below, and press Return at the end of each line:

```
-join CT-towns-merged.csv keys=town,town
-dissolve merged
```

  How to understand the commands above:
  - The first line "joins" the active layer (the polygon map) to the CSV spreadsheet, with "keys" to match their shared data columns, which are both labeled as "town".
  - The second line dissolves the polygons of towns listed in the "merged" column of the CSV file. In this simple example, only Bloomfield and West Hartford are dissolved into a combined "Bloomfield-West Hartford" regional health district, and all of the other polygons remain the same.

  ![](mapshaper-towns-merged.png)

Click the Console button to close its window. Select the "i" information button to inspect your merged polygons. Export the map in your preferred format.


##Learn more advanced MapShaper methods

- See the MapShaper GitHub project wiki (https://github.com/mbloch/mapshaper/wiki/) for more command references and tips about map simplification
- *TO DO*: illustrate concept of a point-to-polygon spatial join. When using the join command, "If the keys= option is missing, Mapshaper will perform a point-to-polygon or polygon-to-point spatial join."



[Improve this book:](../../gitbook/improve.md) Select text to insert comments, or suggest edits on GitHub.

[Data Visualization for All](http://datavizforall.org)
is copyrighted by [Jack Dougherty and contributors](../../introduction/who.md)
and distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0). You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizForAll.org.

![Creative Commons by-nc image](../../cc-by-nc.png)
