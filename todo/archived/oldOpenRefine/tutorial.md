Users can upload addresses to be geocoded as points on a map with several free tools, such as BatchGeo and <a href="http://epress.trincoll.edu/dataviz/chapter/create-point-map-gft/" target="_blank">Google Fusion Tables</a>. But sometimes you need to extract the latitude/longitude coordinates of points (e.g., 41,769, -72.672) for other purposes, such as identifying their location in census geography, or measuring distances between two points for a batch of addresses. Consider the range of solutions below:

To extract <strong>ONE</strong> lat/long coordinate at a time, enter it into Google Maps, right-click on the marker, and select "What's here?" to display and copy the result.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GoogleMapsExtractLatLong.png"><img class="aligncenter size-full wp-image-171" alt="GoogleMapsExtractLatLong" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GoogleMapsExtractLatLong.png" width="452" height="270" /></a>

To extract <strong>MULTIPLE</strong> lat/long coordinates for a batch of addresses, consider the pros and cons of using a Geographic Information System (GIS) tool versus the Open Refine tool.

GIS tools are more powerful, but come at a price. Some GIS applications are free and open-source (such as <a href="http://www.qgis.org/" target="_blank">QGIS</a>), while others are expensive and proprietary (such as ESRI's <a href="http://www.arcgis.com/" target="_blank">ArcGIS</a>, which offers a 30-day free trial, then requires licensing between $100 to $1500 per year). But all GIS tools come with a learning curve that requires a significant time investment. For example, with ArcGIS 10.1, extracting lat/long coordinates involves several steps: preparing and adding a spreadsheet of addresses to a basemap, creating and running the address locator, manually inspecting and rematching some results, exporting the table into a DBF or text file, then importing the results into a spreadsheet program.

[caption id="attachment_206" align="aligncenter" width="597"]<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/ArcGISGeocodeSteps.png"><img class="size-full wp-image-206" alt="Geocoding and extracting XY coordinates with ArcGIS 10.1 requires several steps (not all are shown here)" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/ArcGISGeocodeSteps.png" width="597" height="623" /></a> Geocoding and extracting XY coordinates with ArcGIS 10.1 requires several steps (not all are shown here)[/caption]

One advantage is that knowledgeable GIS users can quickly run large batches of address and manually correct problematic ones to improve precision. In the ArcGIS 10.1 sample above, it took the computer less than a minute to process over 2,400 addresses. But then it took me more than an hour to correct unmatched addresses (the address locator packaged with ArcGIS could not find 100 North Quaker Lane, until I changed it to 100 Quaker Ln N) and locate poorly-written ones (such as 50C Main Street, which should be 50 Main St, Apartment C). Still, ArcGIS gave a reliability score to each address it automatically matched, and allowed me to manually inspect and modify results.

If you do not have access or knowledge of GIS tools, then use the free tool <a href="http://openrefine.org/" target="_blank">Open Refine</a> tool (formerly known as Google Refine, now open source). By following the steps below, new users can geocode multiple addresses using the Google Maps web service and extract coordinates, but with some limitations:
<ul>
	<li>you must clean up addresses before geocoding, since there is no easy way to manually inspect or rematch</li>
	<li>you must display your results on a Google Map, in accordance with the <a href="https://developers.google.com/maps/documentation/geocoding/#Limits" target="_blank">Google Geocoding API usage limits</a></li>
	<li>only 2,500 addresses may be geocoded per day, and a batch this size may require one hour of server time</li>
</ul>
First, clean up your address file. If needed, <a href="http://epress.trincoll.edu/dataviz/chapter/format-combine-addresses" target="_blank">format and combine address terms into one column</a> prior to uploading your spreadsheet.

Download and start up <a href="http://openrefine.org/" target="_blank">Open Refine</a>, which runs in your default browser, to choose and upload data.
<p style="text-align: center;"><a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeoCodeOpenRefineCreate.png"><img class="aligncenter  wp-image-181" alt="GeoCodeOpenRefineCreate" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeoCodeOpenRefineCreate.png" width="503" height="231" /></a></p>
Create and name a new project.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineCreateProject2blurred.png"><img class="aligncenter size-full wp-image-209" alt="GeocodeOpenRefineCreateProject2blurred" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineCreateProject2blurred.png" width="600" height="453" /></a>

To obtain the lat/lon coordinates of a column of addresses, use drop-down menu to edit column, then add column by fetching URLs.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineAddColumn.png"><img class="aligncenter size-full wp-image-183" alt="GeocodeOpenRefineAddColumn" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineAddColumn.png" width="468" height="429" /></a>

Inside Open Refine, write a coded expression to fetch the URL of an address from the free Google Geocoding web service, using the code below:
<code>'http://maps.googleapis.com/maps/api/geocode/json?' + 'sensor=false&amp;' + 'address=' + escape(value, 'url')</code>

Name the new column and set the throttle delay to at least 1000 milliseconds to avoid heavy use of the geocoding service. Click OK.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineAddExpression.png"><img class="aligncenter size-full wp-image-211" alt="GeocodeOpenRefineAddExpression" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineAddExpression.png" width="600" height="397" /></a>

Be patient and respect limits when using free geocoding services. This sample of 2,4000 addresses required over one hour. If you need faster solutions, use more complex GIS tools as described above.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineProcessing.png"><img class="aligncenter size-full wp-image-212" alt="GeocodeOpenRefineProcessing" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineProcessing.png" width="487" height="172" /></a>

After the long geocoded results appear, we need to extract only the coordinates. Select the drop-down menu to Edit column &gt;  Add column based on this column.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineOutputAddColumn.png"><img class="aligncenter size-full wp-image-216" alt="GeocodeOpenRefineOutputAddColumn" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineOutputAddColumn.png" width="600" height="321" /></a>

Name the new column (LatGoogle) and add this expression to extract the latitude coordinate:

<code>value.parseJson().results[0].geometry.location.lat</code>

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineLatGoogle.png"><img class="aligncenter size-full wp-image-219" alt="GeocodeOpenRefineLatGoogle" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineLatGoogle.png" width="600" height="308" /></a>

Add another column based on the results column, name it (LngGoogle), and add this expression to extract the longitude coordinate:

<code>value.parseJson().results[0].geometry.location.lng</code>

Export the project table into your preferred format.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineExport.png"><img class="aligncenter size-full wp-image-220" alt="GeocodeOpenRefineExport" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/03/GeocodeOpenRefineExport.png" width="272" height="331" /></a>

Hint: In some cases, you may wish to write one expression that extracts the lat and long coordinates into one column:

<code>value.parseJson().results[0].geometry.location.lat + ',' + value.parseJson().results[0].geometry.location.lng</code>

How did the lat/lng results from ArcGIS (using StreetMap address locator) compare with Open Refine (using Google Geocoding service)? Both made some errors, though different types. On one hand, ArcGIS + StreetMap had difficulty with address term placement and abbreviations (100 North Quaker Lane had to be changed to 100 Quaker Ln N). On the other hand, Open Refine + Google Geocoding got confused by some addresses that included apartment floors (100 Fairview St FL 3, West Hartford CT 06119 was mistakenly coded as "Florida"). Both struggled with misspelled street names, and when Open Refine + Google Geocoding was uncertain about the front of the address, it relied on the back end and placed the point in the middle of the zip code region. Overall, ArcGIS included reliability scores and allowed me to manually inspect and rematch addresses, while Open Refine + Google Geocode did not offer any clues on where errors might exist, until I placed them on a map and spotted about a dozen Connecticut addresses in Florida. Bottom line: if precision and speed matter, use a GIS application.

But the Open Refine tool has many valuable uses beyond those described here. See Open Refine <a href="http://openrefine.org/" target="_blank">general documentation</a>, and specifics about
<a href="https://github.com/OpenRefine/OpenRefine/wiki/Geocoding" target="_blank">geocoding</a>, and the <a href="http://opensas.wordpress.com/2013/06/30/using-openrefine-to-geocode-your-data-using-google-and-openstreetmap-api/" target="_blank">Opensas blog post</a> on how to manually refine and hand-pick unmatched addresses to edit. Also, view the Open Refine geocoding screencast below:

http://youtu.be/5tsyz3ibYzk
