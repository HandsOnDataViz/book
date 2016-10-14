# Leaflet Maps with Google Sheets template

*By [Jack Dougherty](../../introduction/who.md), last updated October 14, 2016*

## Explore this demo

<iframe src="http://jackdougherty.github.io/leaflet-maps-with-google-sheets/" width="100%" height=550></iframe>

## View demo in new page
- http://jackdougherty.github.io/leaflet-maps-with-google-sheets/

## Features
Create Leaflet maps with a linked Google Sheets template.
- friendly and easy-to-learn searchable map tool with flexibility for advanced users
- clickable point data layers with custom marker icons and pop-up images
- color-coded polygon data layers with numeric or text legends
- upload and geocode addresses, and set map options, in the Google Sheet template
- host your live web map and polygon data with GitHub Pages
- responsive web design for both small and large devices
- built entirely with open-source code, and no usage limits

## Create Your Own: Fork a copy of the code template on GitHub
- http://github.com/jackdougherty/leaflet-map-simple/
- Remember, if you have already forked one copy, go to your GitHub repository Settings to rename it, or create a new GitHub repo and use GitHub Desktop to upload template Files

## To Do
- explain all steps
- Insert internal references to prior steps in this book. See the Edit and Host Code Templates section in this book. Requires a free GitHub account to host your own version on the web.

Design and host your own map on the public web, add your point and/or polygon data, and customize its appearance. *Quick directions for now -- with illustrations to come soon*

These steps require that you sign up and log into a:
- free GitHub account (https://github.com/) to edit two lines of open-source code
- free Google Drive account (https://drive.google.com) to copy and edit the Google Sheets template

#### A) Fork/copy this code repository and publish with GitHub Pages
- Click the Fork button, in the upper-right corner of this code repository, to create a copy of the code in your account.
- Reminder to fix later: if you have already created a fork of this repo, for your second version you will need to (rename original? clone or download?)
- Your new repository will have a web address in this format:
```
https://github.com/USERNAME/leaflet-maps-with-google-sheets
```
- Click the Settings button, in the upper-right section of your new repository.
- On the Settings page, scroll down to the GitHub Pages section, select Source > master branch, and click Save.
- GitHub Pages has published the *default* map from your code repository as a live public web page, which you can view by clicking on the link displayed after "Your site is published at...". It will appear in this format:
```
https://USERNAME.github.io/leaflet-maps-with-google-sheets/
```
- Copy the link to your live web page above.
- Go back to your GitHub code repository home page.
- Click on the README.md file. To edit this file, click the pencil symbol in the upper-right.
- In the Demo section, paste the link to your live web page from above.
- Scroll down and click the green Commit Changes button, which saves your edits to your GitHub repo.
- Go back to your GitHub repo home page. The new link you pasted to your default map should appear in the lower half of this page. Test it.
- Reminder to fix later: need to remove the dev branch from this public repo to avoid confusing newcomers.

#### B) File > Make a Copy and Publish your Google Sheets template
- Your live web map currently displays data from the *default* Google Sheet template. To insert your own data, you will need to make a copy and edit one line of code in your GitHub repository.
- In your GitHub repo home page, click on the [Google Sheet template link]( https://docs.google.com/spreadsheets/d/1ZxvU8eGyuN9M8GxTU9acKVJv70iC3px_m3EVFsOHN9g/edit#gid=0).
- Make sure that you are logged into your Google Drive account, and select File > Make a Copy. Insert a new name to associate it with your new map data, and save it in a folder where you can find it again later, then click OK.
- In your new Google Sheet, click File > Publish to the Web. (Leave the drop-downs as "Entire Document" and "Web page"). Click Publish. All data that you enter below will be *public*.

#### C) Paste your Google Sheets ID into the GoogleDocID.js file
- In your browser address bar, copy the long ID for your new Google Sheet, appears between "/d/" and "/edit...". It will look similar this:
![](google-sheet-id.jpg)

- In your GitHub repo home page, click on the file named GoogleDocID.js, and click the pencil symbol to edit it.
- Replace the default Google Sheet ID by pasting your own from above. Do not erase the quote marks.
- Scroll down and click the green Commit Changes button to save your edits.

#### D) Customize your map settings in the Options tab

#### E) Geocode address data and customize markers in the Points tab

#### F) Upload/link polygon data and set legend colors in Options tab

- Go back to your live web map, which now displays data from your new Google Sheet. Keep both open in separate browser tabs or windows. When you make changes to your Google Sheet, click the refresh button in the live map to update the display.
- The Google Sheet contains three tabs (labeled at the bottom): Options, Points, Polygons.
- In the Options tab, type in your map title, use drop-downs to select map background, and so forth.
- In the Points tab, each row represents a point on your map. Type or paste in data, image links, addresses, and so forth.
  - To geocode addresses inside this Google Sheet, select the Address-Latitude-Longtiude columns, and click the Geocode > Selected Cells (Address to Lat Long) menu. (Geocoding is an add-on feature that does not appear in default Google Sheets.)
  - Group related points into Categories that you can define, which will appear as layers on the map.
- In the Polygons tab... TO DO: explain how polygon data must be prepared in GeoJSON format and uploaded into your GitHub repo (see example: ct-towns-density.geojson); refer to http://DataVizForAll.org tutorials on how to prepare your polygon data
  - find polygon data
  - refer to tutorial on how GeoJSON data is organized by "properties" -- refer to book and include this exercise: Open your GeoJSON polygon map file with http://geojson.io or http://mapshaper.org to view property categories (such as "name") and values for each item
  - if needed, convert polygon data from shapefile or KML format into GeoJSON format with http://geojson.io
  - if needed, edit polygon data and join/merge tables of new data with http://mapshaper.org



---



[Improve this book:](../../gitbook/improve.md) Select text to insert comments, or suggest edits on GitHub.

[Data Visualization for All](http://datavizforall.org)
is copyrighted by [Jack Dougherty and contributors](../../introduction/who.md)
and distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0). You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizForAll.org.

![Creative Commons by-nc image](../../cc-by-nc.png)
