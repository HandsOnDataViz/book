# Leaflet Maps with Google Sheets
*by [Ilya Ilyankou and Jack Dougherty](../../introduction/who.md), last updated March 20, 2017*

## Try it

Explore the map or right-click [this link to open in a new tab](https://jackdougherty.github.io/leaflet-maps-with-google-sheets/)

<iframe src="https://jackdougherty.github.io/leaflet-maps-with-google-sheets/" width="90%" height=500></iframe>

The Leaflet map pulls data and options from an easy-to-modify Google Sheet. Right-click [this link to open in a new tab](https://docs.google.com/spreadsheets/d/1ZxvU8eGyuN9M8GxTU9acKVJv70iC3px_m3EVFsOHN9g)

<iframe src="https://docs.google.com/spreadsheets/d/1ZxvU8eGyuN9M8GxTU9acKVJv70iC3px_m3EVFsOHN9g/pubhtml?widget=true&amp;headers=false" width="90%" height=300></iframe>

## Tool Review
- [Leaflet Maps with Google Sheets](https://github.com/JackDougherty/leaflet-maps-with-google-sheets) allows you to create and customize point, polygon, or polyline maps with no coding skills. Copy and publish the Google Sheet template, copy and host the pre-made Leaflet code template with GitHub Pages, and easily link the two together.
- Requires a free Google account and a free GitHub account
- friendly and easy-to-learn searchable map tool with flexibility for advanced users
- clickable point data layers with custom marker icons and pop-up images
- color-coded polygon data layers with numeric or text legends
- upload and geocode addresses, and set map options, in the Google Sheet template
- host your live web map and polygon data with GitHub Pages
- responsive web design for both small and large devices
- built entirely with open-source code, and no usage limits

** TO DO -- rewrite into pros and cons **

## Video with step-by-step tutorial

In this tutorial, you will learn how to create your own copy of the Leaflet Maps with Google Sheets template, geocode and customize your own point markers, and either hide or upload your own polygon and/or polyline GeoJSON data. The video and instructions below breaks this down into these key steps:
- A) Fork (copy) the code template and publish your version with GitHub Pages
- B) File > Make a copy of the Google Sheet template and publish your version
- C) Paste your Google Sheet and map links into your GitHub
- D) Modify map title and other settings in the Options tab
- E) Geocode locations and customize new markers in the Points tab
- F) Hide the polygon and polyline legends and default GeoJSON data
- G) Upload and display your own polygon and polyline GeoJSON data
- H) Upload and display customized marker icons

Before you begin, this tutorial assumes that you:
- have a [free Google Drive account](http://drive.google.com), and learned the [File > Make a Copy in Google Sheets](https://www.datavizforall.org/spreadsheet/copy) tutorial in this book
- have a [free GitHub account](http://github.com), and learned the [Fork a Copy of a Simple Leaflet Map](https://www.datavizforall.org/github/fork-leaflet) tutorial in this book

** TO DO -- insert video  **

### A) Fork (copy) the code template and publish your version with GitHub Pages

1) Right-click to open the Leaflet Maps with Google Sheets code template in a new tab: https://github.com/JackDougherty/leaflet-maps-with-google-sheets

2) In the upper-right corner, sign in to your free GitHub account

3) In the upper-right corner, click Fork to copy the repository (repo) into your own account. Important: You can only fork a repository **one time**. To make a second copy, see instructions below **to come**.

4) Click on Settings, scroll down to the GitHub Pages area, select Master, and Save. This publishes the code to a public website you control.

5) Scroll down to GitHub Pages section again, and copy the link to your published web site.

![](lmwgs-1-fork-640.gif)

6) Click on the repo name to the go back to the top level.

7) At the top level of your repo, click on README.md, and click the pencil icon to edit this file, written in easy-to-read Markdown code.

8) Erase the link to previous live site, and paste in the link to your site. Scroll down and Commit (save) your edits.

9) Right-click on the link to your published site and open in a new tab. Your website may take up to 1 minute to appear the first time.

### B) File > Make a copy of the Google Sheet template and publish your version

1) Right-click to open this Google Sheets spreadsheet in a new tab: https://docs.google.com/spreadsheets/d/1ZxvU8eGyuN9M8GxTU9acKVJv70iC3px_m3EVFsOHN9g

2) Sign into your Google account

3) File > Make a Copy of the Google Sheet template to your Google Drive

4) File > Publish your Google Sheet to the public web

![](lmwgs-2-make-copy-640.gif)

### C) Paste your Google Sheet and map links into your GitHub

Here's the most important step: connect your Google Sheet directly to your GitHub code.

1) Copy your Google Sheet web address (or URL)

2) In your Github code repo, click to open this file: google-doc-url.js

3) Click the pencil symbol to edit the file

4) Paste your Google Sheet URL into the code to replace the current URL. Do not accidentally delete the existing quotation marks or punctuation.

5) Scroll to bottom of page and press Commit to save your changes

6) Go to the README.md file in your GitHub repo, click to open and edit, and paste your Google Sheet web address to replace the existing link near the top. Commit to save your changes.

7) In the top-level of your GitHub repo, test the new links to your map and your Google Sheet to make sure they work and point to your versions.

### D) Modify map title and other settings in the Options tab

** TO DO - redo GIF **

In your linked Google Sheet, go to the Options Tab and modify these items:

1) Map Title -- insert your own title

2) Map Subtitle -- insert your own version

3) Author Name -- insert your own name, or first name, or initials (will be public)

4) Author Email or Website -- insert your own (will be public), or delete the current name to make it blank

Open the link to your live map in a new browser tab and refresh to see your changes.

### E) Geocode locations and customize new markers in the Points tab

In your new map, our next goal is to add and modify the appearance of a new set of point markers, based on new addresses that you will enter and geocode.

In the Points tab of your Google Sheet:
1) Think of a simple data story that involves at least four geocodeable locations, divided into at least two groups. If you need an example, use this sample table of “Famous Places in New York City”:

| Group     | Name     | Location |
| :-------- | :------- | :------  |
| Landmark  | Empire State Building | 350 5th Ave, New York, NY 10118 |
| Landmark  | Metropolitan Museum of Art | 1000 5th Ave, New York, NY 10028 |
| Transit   | Grand Central Terminal | 89 E 42nd St, New York, NY 10017 |
| Transit   | Penn Station | 159 West 33rd Street, New York, NY 10120 |

2) Enter your Group, Name, and Location data into new rows below the current data.

3) Go to the Font Awesome Icons site, http://fontawesome.io/icons, scroll down to Search Icons, find your desired icon code name, and insert this into the Marker Icon (column B) of your Points sheet. For example, search for and insert the icon code "train" or "building" to display markers with either of these symbols in your map. (To upload your own customized marker, see section H further below.)

4) In Marker Color (column C), use the drop-down menu to select a marker color.

5) In Icon Color (column D), insert a color word (example: white) or hex code (example: #fff) to color the icon symbol inside your marker. Recommended: use white icon colors with dark marker colors.

6) Leave Custom Size (column E) blank.

7) Optional:
  - In Image (column G), insert the URL (preferably https://, not http://) of a small-to-medium sized image on the web
  - In Description (column G), insert text and/or a web link enclosed with an [HTML a href tag with target set to blank](https://www.w3schools.com/tags/tag_a.asp)

8) Do NOT delete or rename any column headers. However, you have the option to add new column headers to display in your map table.

9) Geocode your new data inside your Google Sheet by dragging your cursor to select 6 columns of data: Location - Latitude - Longitude - Found - Quality - Source

10) In the Geocoder menu that appears in this Google Sheet template, select one of the geocoding services. If one service cannot locate your data, try the other. Always inspect the accuracy of the Found column.

Open the link to your live map in a new browser tab and refresh to see your changes. If your new markers appear correctly, then delete the existing rows that came with this template.

### F) Hide the polygon and polyline legends and default GeoJSON data

To show a simple point map, learn how to turn off and hide the polygon and polyline legend and default data that came with this template. (See how to add your own GeoJSON data in section G below.)

In your linked Google Sheet:

1) In the Options tab, Polyline Legend Position (cell B 35) -- select Off to hide the legend

2) In the Polygons tab, Polygon Legend Position (cell B 4) -- select Off to hide the legend

3) In the Polygons tab, Polygon GeoJSON URL (cell B 6) -- delete contents to remove polygons

4) Go to the next tab, named Polygons1, in its drop-down menu, select Delete to remove sheet

5) In the Polylines tab, delete contents of the GeoJSON URL (cells A 2 and A 3) to remove lines

Go to the browser tab with your new map, and refresh the page to see your changes.

Optional:
- in the Options tab, Display Table (cell B 29), turn off to hide the table in your map
- or modify the list of item in Table Columns (cell B 30) to change the display in your table

### G) Upload and display your own polygon and polyline GeoJSON data

** TO COME **

### H) Upload and display customized marker icons

** TO COME **

{% footer %}
{% endfooter %}
