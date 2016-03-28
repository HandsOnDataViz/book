# Leaflet Point Storymap with Scrolling Narrative

*By [Jack Dougherty](../../introduction/who.md), last updated March 28, 2016*

## Try this demo

<iframe src="http://jackdougherty.github.io/leaflet-storymap/" width="100%" height=550></iframe>

## View demo in new page
- http://jackdougherty.github.io/leaflet-storymap/

## Create Your Own Storymap

Before you begin, review previous tutorials in this book:
- [Edit and Host Code Templates with GitHub](../../edit/github/)
- [Create and Convert Map Data with GeoJson.io](../../shape/geojsonio)


1. Go to the GitHub repository template (http://github.com/jackdougherty/leaflet-storymap) and fork a copy of this repo to your own GitHub account. Requires signup for a [free GitHub account](http://github.com). Reminder: if you have already forked one copy, go to your GitHub repository Settings to rename or delete the first copy, so that you may create a second copy.
2. Go to your copy on GitHub and click the "download" button to create a zipped (compressed) copy on your local computer. On most computers, double-click to unzip the folder.
3. The map.csv file contains the map data in an easy-to-edit format. Open map.csv with any spreadsheet tool and replace the existing data with your own.
  - id -- Assign numbers 1, 2, 3. . to each point, in desired order of appearance.
  - chapter --  Add title for each section of the narrative.
  - zoom -- Insert a zoom level for each chapter, usually between 11 (zoomed out) and 18 (zoomed in).
  - image -- If storing images in local "img" folder, follow this format: `img/photo1.jpg`. Or if loading images from an external site, insert the full URL. Currently, images must be about 300px wide and roughly similar height.
  - source-credit -- Add caption to credit the origin of the image. Write in this format: `Source: ABC` or leave blank if none.
  - source-link -- Add a URL to make the source-credit appear as a hyperlink, or leave blank if none.
  - description -- Add text to display in the narrative. Currently, the length is not adjustable.
  - lon and lat -- Insert the longitude and latitude coordinates of each point. To find coordinates in [Google Maps](http://www.google.com/maps), right-click any point and select What's Here. **Reminder:** Google Maps stores points in lat-lon format, but GeoJSON stores them in the reverse order (lon-lat, the same as X-Y coordinates in mathematics), so enter carefully into the map.csv spreadsheet.

4. Save the spreadsheet in CSV format. If this format is unfamiliar, learn more about [saving in CSV format](../../transform/csv/) in this book.
5. Open http://geojson.io in a browser. Drag in the map.csv file to inspect your point data. To export, save in GeoJSON format, and the browser will download a file named: `map.geojson`.
6. Go to your forked repository of leaflet-storymap in your GitHub.com account. Click on 'branches' and keep the master branch, but delete any others (such as gh-pages and/or dev).
7. In the master branch of your repo, click on Upload Files button, upload the two new files you created on your local computer, and replace the existing files with those names.
  - map.csv
  - map.geojson
8. In your master branch, click on the index.html file, click on the pencil icon to turn on the editor, and edit lines 7 and 22 to change the titles that will be displayed. When done, scroll down and click the clean Commit Changes button to save your edits to the master branch.
9. Host your storymap code on the live web with GitHub Pages. At the top level of your repo on GitHub.com, select the master branch drop-down menu, and type in this new branch name: `gh-pages`. When you first create this branch, it contents may take several minutes to appear the first time on the public web, but updates will take only seconds to appear. Your public URL follows this format: `http://USERNAME.github.io/REPO_NAME`.
10. Learn more about how to edit your GitHub branches and make 'pull requests' to save changes from one branch to the other in the [GitHub section in this book](../../edit/github/).


---



[Improve this book:](../../gitbook/improve.md) Select text to insert comments, or suggest edits on GitHub.

[Data Visualization for All](http://datavizforall.org)
is copyrighted by [Jack Dougherty and contributors](../../introduction/who.md)
and distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0). You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizForAll.org.

![Creative Commons by-nc image](../../cc-by-nc.png)
