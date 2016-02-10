# Filtered Point Map with Socrata Open Data

*By [Veronica Armendariz](introduction/contact.md) and [Jack Dougherty](introduction/contact.md), last updated February 10, 2016*

Open data repositories recently launched by the State of Connecticut (http://data.ct.gov) and the City of Hartford (http://data.hartford.gov) both use the Socrata platform (http://www.socrata.com), which offer user-friendly ways to view, filter, and export data. Also, the Socrata platform includes built-in support to create interactive charts and maps, and to embed them on your own websites. This tutorial demonstrates these features by creating an interactive point map of selected schools from the Connecticut Education Directory in the state data portal. The final product looks like this:

<div><iframe width="500px" title="CT Schools Map" height="425px" src="https://data.ct.gov/w/shww-dhc6/wqz6-rhce?cur=wg0AOYsW1XR&from=root" frameborder="0"scrolling="no"><a href="https://data.ct.gov/Education/CT-Schools-Map/shww-dhc6" title="CT Schools Map" target="_blank">CT Schools Map</a></iframe><p><a href="http://www.socrata.com/" target="_blank">Powered by Socrata</a></p></div>

One advantage of creating data visualizations on the Socrata platform is that the chart or map is linked to the data repository. If the Socrata platform administrator updates the data table, then a Socrata dataviz based on that data will be automatically updated, too. This may be especially useful for "live" data that is continuously updated by the Socrata administrator, such as fire, crime, and property data repositories. 

But there are limitations to creating your chart or map on an open data repository platform. First, if the agency stops using the platform, or changes the structure of the underlying data, your online chart or map may stop functioning. Second, you are usually limited to using data tables and geographic boundaries that already exist on that platform, since importing your own may not be an option. 

If these limitations concern you, a simple alternative is to export data from the open repository (which means that any "live" data would become "static" data), and import it into your preferred dataviz tool, such as those described in other chapters of this book. A second, more advanced alternative, is to learn how to pull live data from the repository directly into your dataviz, using an Application Programming Interface (API), which requires coding skills that are beyond the scope of this tutorial. (To learn more about the Socrata API: https://dev.socrata.com/.) 


If these limitations concern you, a simple alternative is to export data from the open repository (which turns any "live" data into "static" data), and import it into your preferred dataviz tool, such as those described in other chapters of this book. A second, more advanced alternative is to learn how to pull live data out of the platform using an Application Programming Interface (API), which requires coding skills that are beyond the scope of this tutorial. (Learn more about the Socrata API:  
## Steps to create a Socrata filtered point map
Create a free account on any Socrata platform. One account will work on all Socrata sites.

![](SocrataMap1.png)

Select your desired dataset in Socrata. In this tutorial, we will use CT Open Data &gt; Education &gt; CT Education Directory (<a href="https://data.ct.gov/Education/Education-Directory/9k2y-kqxn" target="_blank">https://data.ct.gov/Education/Education-Directory/9k2y-kqxn</a>). The data table must include a location column that includes geocoordinates. If there is address data but no geocoordinates, then post a suggestion to the Socrata site administrator to add a geocoded column.

[](SocrataMap2.png)

Filter the data to display only the desired rows. The CT Education Directory lists both district offices and school addresses, but for this map we only wish to display the latter. On the top-right corner of the table, click the Filter tab.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap3.png"><img class="aligncenter size-full wp-image-304" alt="SocrataMap3" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap3.png" width="563" height="609" /></a>

Add a New Filter Condition, which displays only the rows you select. In this tutorial, select “Organization Type” and “is”, then type the exact name from the table, such as “Public Schools.” Be sure to type it correctly or the filter may not work. If you wish to select multiple types, add a new filter condition for each. In this tutorial, we also will filter for other types: Public Charter Schools, CT Technical High Schools, Regional Schools, State Agency Facilities, Endowed and Incorporated Academies Schools, and Regional Education Service Center Schools.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap4.png"><img class="aligncenter size-full wp-image-305" alt="SocrataMap4" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap4.png" width="604" height="526" /></a>

Select the Visualize tab and choose Map, which will display several options. First, under Config for Education Direction, select Point Map as the Plot Style, and choose the Location column to identify the geocoordinates.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap5.png"><img class="aligncenter size-full wp-image-314" alt="SocrataMap5" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap5.png" width="552" height="598" /></a>

Further below in the Visualize &gt; Map options, select the checkbox for Advanced Config for the Education Directory to edit the Flyout Details (similar to a pop-up information window) that displays details when users click on a map point. Select data items you wish to display, such as Title: Name, and additional Flyout Details: Organization Type, Location I, and Website. Further down, select the “w/o labels” checkbox to avoid displaying the column headers in your flyout details.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap6.png"><img class="aligncenter size-full wp-image-306" alt="SocrataMap6" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap6.png" width="489" height="630" /></a>

In Visualize &gt; Map &gt; Base Maps, select your desired background map, such as Google Roadmap.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap7.png"><img class="aligncenter size-full wp-image-307" alt="SocrataMap7" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap7.png" width="474" height="534" /></a>

Add a legend to display once you build the map. In the Advanced Configuration area, select the Legend Configuration checkbox and mark its position. After selecting all of these map options, click Apply. Socrata will generate your map with default point colors. Double-check to make sure your data appear, and that your Visualize settings are correct, before moving to the next step.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap8.png"><img class="aligncenter size-full wp-image-308" alt="SocrataMap8" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap8.png" width="433" height="519" /></a>

Assign point colors and legend labels by returning to the Filter tab, and select Conditional Formatting. Understand the difference between these two features. Previously, we used Filter to display only selected types of data (in this case, school buildings, rather than district administrative offices). Now, we will use Conditional Formatting to assign color codes and labels to our filtered data.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap9.png"><img class="aligncenter size-full wp-image-309" alt="SocrataMap9" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap9.png" width="557" height="576" /></a>

In the Conditional Formatting section, type a name into the Description that you wish to display in the legend. You may type a shorter name than the longer name that appears in the data table, such as “Charter Schools” instead of the longer “Public Charter Schools.” Also, select a color for each Description.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap10.png"><img class="aligncenter size-full wp-image-310" alt="SocrataMap10" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap10.png" width="561" height="537" /></a>

Continue to add Conditional Formatting by defining the data columns. In this example, select “All Conditions Apply,” choose “Organization Type” and “Is”, then type the category exactly as it appears in the data table (such as Public Charter Schools). For this map of schools in the CT Education Directory data table, we added several more types (Regional Schools, CT Technical High Schools, etc.) and also added a second rule to identify Magnet Schools (where Organization Type is Public Schools, and Interdistrict Schools is Yes).
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap11.png"><img class="aligncenter size-full wp-image-311" alt="SocrataMap11" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap11.png" width="423" height="503" /></a>

After setting all of your Conditional Formatting, press Apply at the bottom of the tab. Double-check that your visualization appears exactly as you wish, then Save As under an appropriate name. Note that your visualization will become <strong>publicly visible</strong> to other users on the Socrata open data platform, though you have the option to remove it via your individual profile view.
<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap12.png"><img class="aligncenter size-full wp-image-312" alt="SocrataMap12" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMap12.png" width="663" height="407" /></a>

Visualizations created in the Socrata platform may be embedded on your own website, depending on your platform. Select the Embed tab to view HTML code, which can be resized. You may be able to copy and paste the HTML code directly into your website. If you use a self-hosted WordPress.org site that "strips out" HTML code, then see tutorials in this book on <a href="http://epress.trincoll.edu/dataviz/chapter/host-html-github/">how to host code on a live site (such as GitHub Pages)</a> and <a href="http://epress.trincoll.edu/dataviz/chapter/embed-iframe/">how to embed an iframe into a WordPress.org site</a>.
<p dir="ltr"><a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMapEmbed.jpg"><img class="aligncenter size-full wp-image-318" alt="SocrataMapEmbed" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/07/SocrataMapEmbed.jpg" width="505" height="487" /></a></p>
