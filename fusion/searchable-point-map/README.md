# Searchable Point Map Template with Google Fusion Tables and GitHub Pages

*By [Derek Eder and Jack Dougherty](../../introduction/who.md), last updated March 26, 2016*

Explore this live demo (http://jackdougherty.github.io/fusion-map-point) of a searchable point map with checkboxes.

![](searchable-map-screenshot.png)

This tutorial demonstrates how to create your own Searchable Map, using [Derek Eder's Template for Google Fusion Tables](http://derekeder.com/searchable_map_template/), and freely host it on the web with GitHub Pages. All of the basic steps can be done inside your browser.

Before you begin, review other tutorials in this book:
- [Point map with Google Fusion Tables](../../map/point-gft/)
- [Edit and Host Code with GitHub Pages](../../edit/github)

Overview of key steps:

- [A. Create a point map in Google Fusion Tables](#A)
- [B. Fork a copy of the template to your GitHub account](#B)
- [C. Create a new GitHub Pages branch to publish to the web](#C)
- [D. Edit map options in index.html of your gh-pages branch](#D)
- [E. Insert your own Google Developers API key](#E)
- [F. Add filter to show legend and selected map points](#F)
- [G. Save code edits from gh-pages to your master branch](#G)

See also the [YouTube video tutorial](#video), a more advanced [GitHub Desktop workflow](#workflow), and additional [MapsLib Options](#options) below.

## A. Create a point map in Google Fusion Tables <a id="A"></a>

1. Upload a spreadsheet with address data into Google Fusion Tables and create a point map. See the [tutorial in this book](../../map/point-gft).
1. Make sure at least one column is set to a type of Location and that Fusion Tables has geocoded it
1. Your Fusion Table may include at least one column of data about the points on your map, such as numbers (1, 2, 3, etc.) to represent different types. In the Map tab, select Change Feature Styles to group marker icons into color-coded categories.
1. Set the Fusion Table to be publicly visible (via the Share button in the upper right) and make sure 'Allow Download' is enabled.

## B. Fork a copy of the template to your GitHub account <a id="B"></a>

The Searchable Map Template code is a free repository on the GitHub platform. Users may "fork" one copy to their own GitHub account to edit, and then host a live web version on GitHub Pages.

1. Create a free account on [GitHub](http://github.com)
2. Go to the Searchable Map Template repository on Derek's GitHub account (https://github.com/derekeder/FusionTable-Map-Template) and click the Fork button to copy it to your own GitHub account.
3. OR, fork a similar template on Jack's GitHub account (https://github.com/jackdougherty/fusion-map-point) that already includes the checkbox code describe in step F.

Reminder: GitHub allows users to create **one fork** of a repo to your account. To create a second copy, go to the repo of your first copy, click Settings, and rename it. But if you rename your repo, you also will need to change any links you created to its live version in the next section. 

![](github-settings-rename.png)


## C. Create a new GitHub Pages branch to publish to the web <a id="C"></a>
When you forked the template into your GitHub account, it created two branches: master and gh-pages (abbreviation for GitHub Pages). Keep the master branch, but delete the old gh-pages branch, because it will not work with your account. When you create a new gh-pages branch, it will publish a working demo of the template code to the public web.

1. To delete the old gh-pages branch, select the "branches" tab in your GitHub repo, and click the trash can icon to remove it.
2. Click the repo title to go to the top level.
3. Select the *branch:master* drop-down menu, type the *exact* phrase "gh-pages" into the textbox, and press enter to create and publish your own GitHub Pages branch to the web.
4. In this new "gh-pages" branch, click on the README.md file, and click the pencil icon to edit it inside your browser.
5. Near the top of the README.md, type the link to view it on the live web, in this format: `http://USERNAME.github.io/REPO_NAME`. For example, Derek's GitHub Pages branch is visible on the web at: http://derekeder.github.io/FusionTable-Map-Template
6. When you finish editing the README.md file, scroll down to the bottom and click the green Commit Changes button to save your changes to the gh-pages branch.
7. Try clicking the new link you just added to your README file, which should open your live site in a new tab. When GitHub is busy, *it may take several minutes for your live site to appear the first time*, but later edits will be visible in seconds.

When your live map becomes visible, it will look identical to the template version, until you edit the code. Even if you are waiting for the live version to appear, you can continue to the next section and edit map options in your gh-pages branch.

## D. Edit map options in index.html of your gh-pages branch <a id="D"></a>
The Searchable Map Template contains several files, but the most essential is index.html, since web browsers will open it by default when they view your GitHub Pages branch. Edit the file to show your map data, rather than data that came with the template, and to modify your map options. All of these steps may be done in your browser.

1. Make sure that you are still editing the gh-pages branch of your GitHub repo, rather than the master branch. To switch branches, use the drop-down menu.
2. To edit the index.html file, select its name, then click the pencil icon to enter editing mode.
3. Select the "soft-wrap" drop-down menu option for a better view of long lines of code.
4. Scroll down to around line 120 of index.html to edit these essential map options.
```javascript
$(function() {
  var myMap = new MapsLib({
  fusionTableId:"1m4Ez9xyTGfY2CU6O-UgEcPzlS0rnzLU93e4Faa0",
  googleApiKey: "AIzaSyA3FQFrNr5W2OEVmuENqhb2MBB2JabdaOY",
  locationColumn: "geometry",
  map_center: [41.8781136, -87.66677856445312],
  locationScope: "chicago"
});
```
5. Learn about each one:
  - fusionTableId - The ID of your Google Fusion Table point map that you created above, located in *File => About this table*. Select your long TableId and use keyboard commands to copy and paste into the code.)
   - googleApiKey - Get your own [Google Developers Application Programming Interface (API) key](https://developers.google.com/maps/documentation/javascript/get-api-key#get-an-api-key), as shown in the next section, then copy and paste it in place of the default key in the template
   - locationColumn - The name of your location column in your Fusion Table, such as "geometry" or "address" or other.
   - map_center - The lat/long coordinate where you want to center your map. ([Find yours here](http://www.itouchmap.com/latlong.html)).
   - locationScope - The area where you want to limit searches (set to 'chicago' by default).

6. After making these edits, scroll down to the bottom of the page and click Commit Changes to save to your gh-pages branch. 
7. On the README.md page, click the link you inserted to your live site to view the most recent changes. Click the browser refresh button to update the display, or [bypass the cache](http://en.wikipedia.org/wiki/Wikipedia:Bypass_your_cache#Bypassing_cache).

See more details in the [MapsLib options](#options) section.

## E. Insert your own Google Developers API key <a id="E"></a>
Create your own Google Maps JavaScript API key to replace the default in the Map Options section of the index.html file above. By inserting your own key, Google will allow 25,000 requests per day to your Searchable Map.

1. Go to the [Google Developers Maps JavaScript API page](https://developers.google.com/maps/documentation/javascript/get-api-key#get-an-api-key) and click the Get a Key button
2. On the [Google Developers Console page](https://console.developers.google.com/projectselector/apis/credentials), select Create a New Project and press Continue
3. On the Credentials page, create a key, which should look something like `AIzaSyBNVkiNzErPTEGpxWp0cvdqDMd2BxD-S50`.
4. Copy and paste your key into the Map Options section of the index.html file as described above.
5. To find or edit your key in the future, go back to the [Google Developers Console page](https://console.developers.google.com/projectselector/apis/credentials) 

## F. Add filter to show legend and selected points <a id="F"></a>
The Searchable Map Template code can be customized to include a filter, which displays a color-coded interactive legend that allows users to display selected points on the Google Fusion Table map. See Derek's [Searchable map template project wiki](https://github.com/derekeder/FusionTable-Map-Template/wiki) to learn about several [filter examples](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples).

Adding a basic filter requires three steps:
- Set up Fusion Table data column and map point colors
- Insert filter display code into index.html
- Insert filter logic code into maps_lib.js file

This tutorial demonstrates how to insert a basic checkbox filter, using the [sample Google Fusion Table data from Derek's template](https://www.google.com/fusiontables/DataSource?docid=1m4Ez9xyTGfY2CU6O-UgEcPzlS0rnzLU93e4Faa0#rows:id=1). This filter refers to numerical values (1, 2, 3) in the "type" data column of the Fusion Table, which match three color codes (blue, green, and red) in the Fusion Table Map, which correspond to three labels (City, Private, Hazardous) for types of Chicago recycling stations. Of course, your data will be different, but create a table like the one below to organize your design.

| type | colors | labels     |
|------|--------|------------|
| 1    | blue   | City       |
| 2    | green  | Private    |
| 3    | red    | Hazardous  |

Hint: In Part B above, if you forked [Jack's version of the searchable map template](https://github.com/jackdougherty/fusion-map-point), it already includes the basic checkbox code.

####Set up Fusion Table data column and map point colors
1. Confirm the values in the "type" column of your Google Fusion Table.
2. Confirm the matching color values in your Fusion Table Map.

####Insert filter display code into index.html
1. Edit the index.html file in your gh-pages branch. In Derek's template, delete his description about filters (rows 59-78). In its place, copy and paste the checkbox filter display code shown below. Note that "cbType1" means "check box type 1." Customize your titles, labels, and colors to match your own data. Scroll to the bottom of the page to "commit changes" to your gh-pages branch.

```html
<h4>
  Recycling services
</h4>
<ul class='inputs-list unstyled'>
  <li>
    <label class='checkbox inline'>
      <input type='checkbox' id='cbType1' />
      <span class='filter-box filter-blue'></span>
      City drop-off location
    </label>
  </li>
  <li>
    <label class='checkbox inline'>
      <input type='checkbox' id='cbType2' />
      <span class='filter-box filter-green'></span>
      Private business
    </label>
  </li>
  <li>
    <label class='checkbox inline'>
      <input type='checkbox' id='cbType3' />
      <span class='filter-box filter-red'></span>
      Hazardous materials
    </label>
  </li>
</ul>
```
####Insert filter logic code into maps_lib.js file
The maps_lib.js file (which appears in the js, or JavaScript folder) contains the core code that operates the Searchable Map template. Adding a filter with logical statements (matching those in the index.html and the Fusion Table) allows users to turn on/off selected point maps. Numerical filters work best, but see Derek's [project wiki filter page](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples) for examples with text strings.

1. In your gh-pages branch, edit the maps_lib.js file, located in the js folder.
2. Copy and paste the filter logic shown below into the "custom filters" section of the code, usually between lines 165-166 of the template. Note that "cbType1" and its numerical value (1) should match your index.html file and Fusion Table. Scroll down to commit changes to your gh-pages branch.

```javascript
var type_column = "'type'";
var searchType = type_column + " IN (-1,";
if ( $("#cbType1").is(':checked')) searchType += "1,";
if ( $("#cbType2").is(':checked')) searchType += "2,";
if ( $("#cbType3").is(':checked')) searchType += "3,";
self.whereClause += " AND " + searchType.slice(0, searchType.length - 1) + ")";
```
Hints:
- The data column in the template is named "type." But if your Fusion Table column name has spaces in it, make sure to surround it with single quotes as shown.
- The number of filter colors/labels/types can be expanded beyond the 3 shown above by adding lines of code. Fusion Tables and the Searchable Map Template support 5 large markers (blue, red, green, yellow, purple), and Fusion Tables supports 5 additional small markers with the same colors.
- In the index.html file, edit the titles, text, and source info to tell the story of your map and credit others. 

## G. Save code edits from gh-pages to master branch<a id="G"></a>

After you complete these edits to your gh-pages branch and view the live web version, save a copy of your work with a "pull request" to your master branch. Use the gh-pages branch for testing new features on your live web demo site, and use the master branch to preserve a safe copy of your working code. (More advanced users can use the [GitHub Desktop workflow](#workflow).)

1. In the right-hand column of the top-level of your GitHub repository, click "Pull Request"
2. Click the green "New Pull Request" button.
3. In the drop-down menus, select YOUR base and YOUR branches (**not** Derek's or Jack's base). In this example, the goal is to send a pull request TO your master branch FROM your gh-pages branch. ![](GitHub-Create-Pull-Request.png)
4. Click the green Create Pull Request button. Give your pull request a name, such as: *Updated index file*.
5. Click the next green Create Pull Request Button.
6. If GitHub decides it can automatically merge the gh-pages branch edits into the master branch, a green Merge Pull Request button will appear. Click it.
7. Click the green Confirm Merge button.
8. Your Pull Request should be successfully completed. Do NOT delete the gh-pages branch unless you really wish to do so.

## GitHub Desktop workflow <a id="workflow"></a>



## Video tutorial <a id="#video"></a>

{% youtube %}https://youtu.be/b73LBXYrbng{% endyoutube %}

**TO DO** Update video to reflect edits above, such as inserting URL in the README.MD, or Get an API key

## Additional MapsLib options <a id="#options"></a>

You can configure your map by passing in a dictionary of options when you create a new `MapsLib` instance in `index.html` or `index_iframe.html`. Here's an example:

```javascript
var myMap = new MapsLib({
  fusionTableId:      "1m4Ez9xyTGfY2CU6O-UgEcPzlS0rnzLU93e4Faa0",
  googleApiKey:       "AIzaSyA3FQFrNr5W2OEVmuENqhb2MBB2JabdaOY",
  locationColumn:     "geometry",
  map_center:         [41.8781136, -87.66677856445312],
  locationScope:      "chicago"
});
```

| Option           | Default value           | Notes                                                                                                                                                         |
|------------------|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fusionTableId    |                         | **Required**. Table ID of your Fusion Table (found under File => About).                                                                                      |
| googleApiKey     |                         | **Required**. Found at https://console.developers.google.com/ The key provided in this template is for demonstration purposes only. Please register your own. |
| map_centroid     |                         | **Required**. Center [latitude, longitude] that your map defaults to.                                                                                         |
| recordName       | record                  | Used for showing the count of results.                                                                                                                        |
| recordNamePlural | records                 |                                                                                                                                                               |
| searchRadius     | 805                     | Default search radius. Defined in meters. Default is 1/2 mile.                                                                                                |
| locationColumn   | geometry                | Name of the location column in your Fusion Table. If your location column name has spaces in it, surround it with single quotes like this "'my location'".    |
| locationScope    |                  | Appended to all address searches to keep results within a geographic area.                                                                                    |
| defaultZoom      | 11                      | Default zoom level when map is loaded (bigger is more zoomed in).                                                                                             |
| addrMarkerImage  | images/blue-pushpin.png | Image used to identify your address search on the map. Setting it to blank (`""`) will hide the marker.                                                              |



---



[Improve this book:](../../gitbook/improve.md) Select text to insert comments, or suggest edits on GitHub.

[Data Visualization for All](http://datavizforall.org)
is copyrighted by [Jack Dougherty and contributors](../../introduction/who.md)
and distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0). You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizForAll.org.

![Creative Commons by-nc image](../../cc-by-nc.png)
