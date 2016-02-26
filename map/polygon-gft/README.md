# Thematic polygon map with Google Fusion Tables

A thematic polygon map (also called a choropleth map) displays a colored pattern on each region to express its numerical value. In the interactive version embedded below, click on any region to view its info window with additional data.

<iframe width="600" height="400" scrolling="no" frameborder="no" src="https://www.google.com/fusiontables/embedviz?q=select+col2%3E%3E1+from+1MeyX2ICg1uIiAQUOChkUtbnZqfFE-3Kke3SkXnur&amp;viz=MAP&amp;h=false&amp;lat=41.51442003948278&amp;lng=-72.62841864453128&amp;t=1&amp;z=9&amp;l=col2%3E%3E1&amp;y=2&amp;tmplt=2&amp;hml=KML"></iframe>

*Median Household Income in Connecticut Towns, 2009-14, American Community Survey 5-Year Estimates, US Census/Social Explorer.*

To create a thematic polygon map, we need to merge two types of files:
- data table: the numerical values for each polygon
- geographic borders: a series of points that draws each polygon

To merge the data table and geographic borders, the two files must share a common column of information, usually the name or ID of each polygon.





One of the easiest ways to create thematic data maps (geographic areas shaded by data values) is to use Google Fusion Tables (GFT), a freely accessible tool for managing, merging, and visualizing data on the web. GFT requires a [free Google Drive account](http://drive.google.com) (use a regular Google username; avoid limited-access Google Apps for Education accounts). For general information, see Google documentation "<a href="https://support.google.com/fusiontables/answer/2571232" target="_blank">About Fusion Tables</a>" and also the <a href="http://www.google.com/support/fusiontables/" target="_blank">GFT Help Page</a>. This tutorial was updated in Fall 2013 to incorporate <a href="https://support.google.com/fusiontables/answer/1656859" target="_blank">new GFT features</a>, such as automatic map legends. See also <a href="http://youtu.be/ReUAlZsJxP4" target="_blank">video tutorial</a> at the bottom of the page.

view this video screencast</a>:

https://www.youtube.com/watch?v=ReUAlZsJxP4

http://youtu.be/ReUAlZsJxP4

<span><strong>To Do **:</strong> If you need to display textual data in your legend, rather than numerical data, see this solution: </span><span></span><a href="https://github.com/JackDougherty/FusionTable-Map-custom-legend" target="_blank">https://github.com/JackDougherty/FusionTable-Map-custom-legend</a>

<strong>Acknowledgement:</strong> Tutorial adapted from <a href="http://kh-samples.googlecode.com/svn/trunk/talks/hackhackers/workshop.html" target="_blank">Create A Map, kh-samples, Google Code</a>.

<strong>Download and understand your data</strong>
Before starting to map, closely examine your data files to understand their meaning, sources of origin, and limitations.

1) Click on the sample spreadsheet data to download to your desktop, open the file, and examine it.
<p style="padding-left: 30px;"><a title="dropbox" href="https://dl.dropbox.com/u/14023305/CT_SchoolDist_HartfordArea_Race_2009_10.xls" target="_blank">spreadsheet data</a> (in Excel .xls format) Racial composition of Hartford-area school districts, 2009-10, from the <a title="CEDAR" href="http://sdeportal.ct.gov/Cedar/WEB/ct_report/CedarHome.aspx" target="_blank">Connecticut Department of Education, CEDaR data site</a></p>
2) Click on the sample map boundary data to download to your desktop, open the file (using the free <a href="http://www.google.com/earth" target="_blank">Google Earth</a> application), and examine it.
<p style="padding-left: 30px;"><a title="dropbox" href="https://dl.dropbox.com/u/14023305/CT_TownBoundaries_Census2010.kml" target="_blank">boundary data</a> (.kml format) Connecticut town boundaries, Census 2010, from <a title="MAGIC" href="http://magic.lib.uconn.edu/connecticut_data.html#boundaries" target="_blank">MAGIC UConn Libraries, boundary data page</a></p>
<p style="padding-left: 30px;"><em>Additional resource:</em> For related data projects, you may download this <a href="https://dl.dropboxusercontent.com/u/14023305/CT_CensusTractBoundaries2010_UConnMAGIC_wgs84.kml" target="_blank">CT Census Tracts 2010 boundary file</a> (.kml format), from <a title="MAGIC" href="http://magic.lib.uconn.edu/connecticut_data.html#boundaries" target="_blank">MAGIC UConn Libraries, boundary data page</a>. Also, you can download census tract spreadsheet data to merge with it from <a href="http://www.census.gov" target="_blank">Census.gov</a> or <a href="http://www.socialexplorer.com" target="_blank">SocialExplorer.com</a> (export in CSV format, and multiply 6-digit tract number by 0.01 to add decimals to match).</p>
<p style="padding-left: 30px;"><em>Advanced tip:</em> These sample boundary files in KML (Keyhole Markup Language) format initially were downloaded from MAGIC in compressed KMZ format, which is not compatible with Google Fusion Tables. To learn how to modify files with free tools, see this <a href="http://epress.trincoll.edu/dataviz/chapter/convert-kml-filter" target="_blank">tutorial to convert from KMZ to KML in Google Earth and filter results in Google Fusion Tables</a>.</p>
<strong>Upload spreadsheet and boundary data to Google Fusion Tables (GFT)</strong>
1) Sign in to your <a title="gdrive" href="http://drive.google.com" target="_blank">Google Drive account</a> and go to Create &gt; Fusion Table (experimental).

If Fusion Tables is not listed, go to Create &gt; Connect More Apps, search for "Fusion" and Connect the Fusion Tables app to your Google Drive account, as shown below:

<a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_AddFusionAppMarked.png"><img class="aligncenter size-full wp-image-1687" alt="GFT_AddFusionAppMarked" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_AddFusionAppMarked.png" width="600" height="285" /></a>

2) In GFT, import the spreadsheet table you downloaded above. Select "From this computer" &gt; Browse and navigate to the file. Click Next to confirm data, click Next again to add any source info (such as "CT Dept of Ed" or "UConn MAGIC", then click Finish.

<a href="http://commons.trincoll.edu/jackdougherty/files/2012/11/ImportNewGFT.png"><img class="aligncenter size-full wp-image-876" alt="" src="http://commons.trincoll.edu/jackdougherty/files/2012/11/ImportNewGFT.png" width="510" height="124" /></a>

3) Repeat the steps above to upload the .kml boundary data. (The first town name may appear as "County subdivisions not defined," which you can ignore for this exercise.)
<p style="padding-left: 30px;">Advanced tip: Any columns highlighted in yellow means that GFT is attempting to <a href="https://support.google.com/fusiontables/answer/1012281" target="_blank">geocode location data</a> by placing a point on a map. For this exercise, geocoding is unnecessary because our KML boundary file already contains location data. To turn off the yellow highlighting, in the GFT column drop-down menu, select Change, and select "Text" instead of "Location" for the Description, as shown below:</p>
<p style="padding-left: 30px;"><a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_ChangeColumn.png"><img class="aligncenter size-full wp-image-1688" alt="GFT_ChangeColumn" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_ChangeColumn.png" width="339" height="306" /></a></p>
<strong>The "Fusion" part: Merge the spreadsheet table with the boundary table </strong>
4) In your web browser, go to the GFT spreadsheet tab (which should already be open; if not, click on it in your Google Drive tab). In the menu, select File &gt; Merge:

<a href="http://commons.trincoll.edu/jackdougherty/files/2012/11/GFTMergeMenu.png"><img class="aligncenter size-full wp-image-877" alt="" src="http://commons.trincoll.edu/jackdougherty/files/2012/11/GFTMergeMenu.png" width="230" height="240" /></a>

5) Select the table you wish to merge with your spreadsheet table. (In this example, choose the geographic bound

<a href="http://commons.trincoll.edu/jackdougherty/files/2012/11/SelectTableToMerge.png"><img class="aligncenter size-full wp-image-879" alt="" src="http://commons.trincoll.edu/jackdougherty/files/2012/11/SelectTableToMerge.png" width="468" height="175" /></a>6) Before you merge, confirm the source of the match, which means to select the correct data columns that are common to both tables. In this exercise, go to the right-hand CT Town Boundaries table and select "Name" to match it up with the "District" column of the CT School District spreadsheet data, as shown below. (Match the TYPE of data, meaning Districts and Town names, even if they do not appear in the same order.)

<a href="http://commons.trincoll.edu/jackdougherty/files/2012/11/ConfirmMerge.png"><img class="aligncenter size-full wp-image-880" alt="" src="http://commons.trincoll.edu/jackdougherty/files/2012/11/ConfirmMerge.png" width="422" height="315" /></a>

7) Click Next, merge all columns, and View the newly merged table, as shown below:

<a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_MergedTableCreated.png"><img class="aligncenter size-full wp-image-1690" alt="GFT_MergedTableCreated" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_MergedTableCreated.png" width="417" height="202" /></a>

<strong>Create and Style a Thematic Map with Info Windows
</strong>8) In your new Merged table, see the Map tab and select Change feature styles.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2013/11/GFTpolygon-ChangeMapStyles.png"><img class="aligncenter size-full wp-image-98" alt="GFTpolygon-ChangeMapStyles" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2013/11/GFTpolygon-ChangeMapStyles.png" width="533" height="401" /></a>

9) To modify the thematic map, select Polygons &gt; Fill Color, and experiment with Buckets and Gradients to modify the thematic map shading. <em>Reminder: if you choose to map a percentage column (rather than raw numbers), adjust the range (from 0-100 to an appropriate range, such as 0 - 1.0).</em>

<a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFTChangeMapFeatureStyles2.png"><img class="aligncenter size-full wp-image-1693" alt="GFTChangeMapFeatureStyles2" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFTChangeMapFeatureStyles2.png" width="494" height="517" /></a>
<p style="padding-left: 30px;"><em>Advanced tip:</em> See Mark Monmonier, <em>How to Lie with Maps, Second Edition </em>(University of Chicago Press, 1996), <a title="excerpt" href="http://commons.trincoll.edu/cssp/files/2011/09/Monmonier1996excerpt.pdf" target="_blank">pp. 39-42 excerpt</a> on how same data can be spatially represented in very different ways, by modifying thematic map categories and cut-offs, in the Buckets or Gradients section of GFT. See also <a title="colorbrewer" href="http://colorbrewer2.org/" target="_blank">ColorBrewer</a> for advice on selecting appropriate map colors and categories. (*To do: look for ColorBrewer with HTML color output.)</p>
10) Select Automatic Legend. Check the box to show a legend, choose a title and position, and include a link to the source data.

<a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_AutomaticLegend.png"><img class="aligncenter size-full wp-image-1697" alt="GFT_AutomaticLegend" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_AutomaticLegend.png" width="544" height="520" /></a>

11) To modify how data appears in the map pop-up info windows, go to Map tab &gt; Feature Map &gt; Change info window. Select boxes in the Automatic tab and/or modify code in the Custom tab.

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2013/11/GFTpolygon-ChangeInfoLayout.png"><img class="aligncenter size-full wp-image-99" alt="GFTpolygon-ChangeInfoLayout" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2013/11/GFTpolygon-ChangeInfoLayout.png" width="353" height="429" /></a>
<p style="padding-left: 30px;">Advanced tip: To limit the data that appears in your map, go to the Merged Table and select Filter to exclude selected rows, as shown below:</p>
<p style="padding-left: 30px;"><a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFTFilter.png"><img class="aligncenter size-full wp-image-1695" alt="GFTFilter" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFTFilter.png" width="261" height="298" /></a></p>
<strong>Embed the interactive map in a WordPress.org post (or most web pages)</strong>
12) In the GFT Merged Table, click the Share button in upper-right corner to change the visibility settings of the default (Private) to Anyone with the Link, or Public:

<a href="http://commons.trincoll.edu/jackdougherty/files/2012/11/SharingSettings2012.png"><img class="aligncenter size-full wp-image-891" alt="" src="http://commons.trincoll.edu/jackdougherty/files/2012/11/SharingSettings2012.png" width="480" height="296" /></a>

13) Modify the map zoom level and position, then select Map of Geometry &gt; Publish.

<a href="http://commons.trincoll.edu/jackdougherty/files/2012/11/PublishMenu.png"><img class="aligncenter size-full wp-image-892" alt="" src="http://commons.trincoll.edu/jackdougherty/files/2012/11/PublishMenu.png" width="440" height="352" /></a>

14) Modify the map width and height to fit the space allowed by the WordPress theme. (For many WordPress pages, 600 x 400 pixels looks best.) Copy the long string of code code from the "Paste HTML to embed" field.

<a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_PublishHTML.png"><img class="aligncenter size-full wp-image-1696" alt="GFT_PublishHTML" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_PublishHTML.png" width="436" height="306" /></a>

15) In the Trinity Commons WordPress v3.5 site for my seminars, I have already activated <a href="http://wordpress.org/plugins/iframe/" target="_blank">a special plugin ("iframe")</a> to correctly process the HMTL embedded map code for students with regular authoring privileges. (If you have administrative privileges or your own self-hosted WordPress.org site, this step may not be necessary. Currently, iframes do NOT work in most WordPress.com sites.)

<a href="http://commons.trincoll.edu/jackdougherty/files/2012/11/PluginActiveIFrame.jpg"><img class="aligncenter size-full wp-image-896" alt="" src="http://commons.trincoll.edu/jackdougherty/files/2012/11/PluginActiveIFrame.jpg" width="360" height="86" /></a>

16) Go to WordPress and create a new post. In the editor, switch from the Visual to the Text tab, which allows users to insert and modify HMTL code. Paste the long string that you copied from the step above. Add square brackets at beginning and end, and edit a few characters to match this format (called a "shortcode"), then publish to view your post.

<a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_iFrameEmbedCode.png"><img class="aligncenter size-full wp-image-1700" alt="GFT_iFrameEmbedCode" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_iFrameEmbedCode.png" width="599" height="449" /></a>



---



[Improve this book:](../../gitbook/improve.md) Select text to insert comments, or suggest edits on GitHub.

[The DataViz Book](http://datavizbook.org)
is copyrighted by [Jack Dougherty and contributors](../../introduction/who.md)
and distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0). You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.

![Creative Commons by-nc image](../../cc-by-nc.png)
