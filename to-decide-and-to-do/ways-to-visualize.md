Let's assume that you have some data that currently exists in (or could easily be transformed into) a table or spreadsheet. Perhaps the rows and columns contain categories, numbers, or locations, and looks similar to one of the following (*simple images to come*).

How do you want to visualize your data? Consider your options on this decision tree (*To Do: reorganize below into a table, add interactive 1oox100 thumbnails of each type (similar to this <a href="https://developers.google.com/chart/interactive/docs/gallery" target="_blank">Google Charts gallery</a> but smaller) to left of each as illustrative example)

<strong>"FLAT" VISUALIZATION:</strong> to insert a chart or map into a printed page or static PDF document, with no web interaction
<ul>
	<li>STOP. If you simply wish to create charts or maps that will lay "flat" inside a printed report or PDF file, then stop reading this book, go back to the 1990s, and buy a copy of Microsoft Excel (or even better, download the free and open-source <a href="https://www.libreoffice.org/" target="_blank">Libre Office application suite</a>). (*similar "flat" mapping applications*)</li>
</ul>
<strong>INTERACTIVE VISUALIZATION: </strong>While all of the data products in this book can be printed out on paper or turned into static PDF files, they are designed to add value through web interaction.

<strong>CHART</strong> your tabular data into a graphic visualization for web visitors to click and explore
<ul>
	<li>Simple Line chart — see <a href="https://support.google.com/drive/answer/190718?hl=en&amp;ref_topic=30240" target="_blank">Google Sheet line chart</a> (*add tutorial with Share HTML) or Google Fusion Table (*add tutorial with Share iframe)</li>
	<li>Custom Line chart, with annotations etc. (*add tutorial with GitHub template, to come)</li>
	<li>Simple Bar/Column chart — see <a href="https://support.google.com/drive/answer/190723?hl=en&amp;ref_topic=30240" target="_blank">Google Sheet bar chart</a> or <a href="https://support.google.com/drive/answer/190722" target="_blank">column chart</a> (*add tutorial with Share HTML); or Google Fusion Table bar/column chart (*add tutorial with Share iframe)</li>
	<li>Custom Bar/Column chart - see <a href="https://github.com/JackDougherty/gviz-bar-chart-sheet" target="_blank">bar chart template</a> and <a href="https://github.com/JackDougherty/gviz-column-chart-sheet" target="_blank">column chart template</a> (with stacked chart option) that draws data from Google Spreadsheet (*tutorial to come)</li>
	<li>Simple Scatter chart (displays X-Y pairs) - see <a href="https://support.google.com/drive/answer/190724" target="_blank">Google Sheet</a> (*add tutorial with Share HTML)</li>
	<li><a href="http://epress.trincoll.edu/dataviz/chapter/custom-scatter-chart/" target="_blank">Custom Scatter Chart with data series/tooltip options from Google Spreadsheet tutorial</a></li>
	<li>explore more in galleries for <a href="https://support.google.com/drive/topic/30240" target="_blank">Google Spreadsheets</a> or <a href="https://sites.google.com/site/fusiontablestalks/stories" target="_blank">Google Fusion Tables</a> or <a href="https://developers.google.com/chart/interactive/docs/gallery" target="_blank">Google Charts</a></li>
</ul>
<strong>MAP </strong>your spatial data for web visitors to search, zoom in, and explore the geography<em>
</em>

<strong>• Point maps</strong> display data for specific locations (usually street addresses or X-Y coordinates)
<ul>
	<li>Create a basic point map with BatchGeo or ZeeMaps (easy, but limited; *tutorial to come)</li>
	<li><a href="http://epress.trincoll.edu/dataviz/chapter/create-point-map-gft" target="_blank">Create an interactive point data map and geocode with Google Fusion Tables</a> (more steps, but more flexible)</li>
	<li>Create interactive point data map with textual data and legend  <a href="https://github.com/JackDougherty/FusionTable-Map-Checkboxes" target="_blank">template</a> *tutorial to come</li>
	<li>If needed, <a href="http://epress.trincoll.edu/dataviz/chapter/format-combine-addresses/" target="_blank">Format combine address terms for geocoding</a>, and <a href="http://epress.trincoll.edu/dataviz/chapter/extract-geo-open-refine" target="_blank">Extract geocoded latitude/longitude coordinates</a> with Open Refine</li>
</ul>
<b>• Line maps</b> display data for specific routes (such as walking or bicycling trails)
<ul>
	<li>details to come*</li>
</ul>
<strong>• Polygon maps</strong> display data for regions with boundary lines (such as census tracts, towns, states, or nations)
<ul>
	<li><a href="http://epress.trincoll.edu/dataviz/chapter/create-thematic-polygon-map" target="_blank">Create thematic polygon data map with Google Fusion Tables tutorial</a></li>
	<li><a href="http://epress.trincoll.edu/dataviz/chapter/convert-kml-filter" target="_blank">Convert to KML in Google Earth and Filter in Google Fusion Tables tutorial</a></li>
</ul>
<b>• Layered maps</b> combine two or more sets of points and/or polygons on the same interactive web page
<ul>
	<li>Combine multiple maps with the Google Fusion Tables Layer Wizard * <a href="http://fusion-tables-api-samples.googlecode.com/svn/trunk/FusionTablesLayerWizard/src/index.html" target="_blank">link here</a>, tutorial to come*</li>
	<li>or 2-layer map (point and polygon) with Google Fusion Tables <a href="https://github.com/JackDougherty/FusionTable-Map-2-layers" target="_blank">template</a>, tutorial to come*</li>
</ul>
<strong>• Search and Filter maps </strong>allow web visitors to search addresses and turn on/off data categories or layers
<ul>
	<li>Create a Search-and-Filter Map with Google Fusion Tables template by Derek Eder * <a href="http://derekeder.com/searchable_map_template/" target="_blank">link here</a> * tutorial to come*</li>
	<li>or Search-and-Filter 2-layer map (points and polygons) with GFT <a href="https://github.com/JackDougherty/FusionTable-Map-2-layers" target="_blank">template</a> with tutorial to come*</li>
</ul>
• <strong>ArcGIS Online maps</strong> for organizations that already have spatial data in this ESRI proprietary format
<ul>
	<li><a href="http://www.arcgis.com/home/webmap/viewer.html?webmap=3fbe2d92b92b47bdb55dd429b0dcc269&amp;extent=-72.7772,41.7101,-72.6004,41.8246" target="_blank">sample</a> by Dave Tatem; not free; requires purchase of ArcGIS software and ESRI credits *tutorial to come*</li>
</ul>
<strong>TABLE</strong> for web visitors to search, sort, or filter the underlying data
<ul>
	<li>Create a Sort-and-Filter HTML table with Google Fusion Tables template by Derek Eder * <a href="http://derekeder.com/fusion-tables-to-html-table/" target="_blank">link here</a>; *tutorial to come*</li>
</ul>
<strong>TIMELINE</strong> *to come

<strong>SHARE</strong> and publish your data visualization to the public web, and embed on popular websites
<ul>
	<li>If your data tool generates iframe code, then <a href="http://epress.trincoll.edu/dataviz/chapter/embed-iframe/" target="_blank">Embed iframe with WordPress plugin tutorial</a></li>
	<li><del>If your data tool generates HTML code, then <a href="http://epress.trincoll.edu/dataviz/chapter/host-html-google-drive/" target="_blank">Host HTML site on Google Drive tutorial</a></del></li>
	<li><a href="http://epress.trincoll.edu/dataviz/chapter/host-html-github/" target="_blank">Host HTML code and collaborate with GitHub Pages tutorial</a> *updating</li>
</ul>
<strong>DISCUSS </strong>how to interpret the meaning of data visualizations (and what they do not mean) with clear wording *to come

<strong>FIND </strong>data sources of interest to non-profit organizations, particularly in Connecticut
<ul>
	<li><a href="http://www.socialexplorer.com/" target="_blank">Social Explorer</a> to download tables and explore visualizations from US Census and other sources (*free data limited; full access requires institutional license; Trinity student <a href="http://www.trincoll.edu/LITC/Library/servicesinfo/spacestech/Pages/network.aspx" target="_blank">off-campus VPN access</a>)</li>
	<li><a href="http://magic.lib.uconn.edu/" target="_blank">MAGIC</a>: Map and Geographic Information Center at the University of Connecticut to download boundaries and data</li>
</ul>
<strong>CASE STUDIES</strong> *to come
