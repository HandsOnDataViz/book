# Leaflet Story Maps with Google Sheets and Scrolling Narrative

*By [Ilya Ilyankou and Jack Dougherty](../../introduction/who.md), last updated September 28, 2017*

## Try it
Explore the map or right-click to [view full-screen map in a new tab](https://datavizforall.github.io/leaflet-storymaps-with-google-sheets/)
<iframe src="https://datavizforall.github.io/leaflet-storymaps-with-google-sheets/" width="90%" height=500></iframe>

The map pulls the point data and settings from a linked Google Sheet, which you can explore below or right-click to [view full-screen Sheet in a new tab](https://docs.google.com/spreadsheets/d/1AO6XHL_0JafWZF4KEejkdDNqfuZWUk3SlNlQ6MjlRFM/)
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSqxGs67j80rAPDZdQaS5jI0avn1qs2y5N8fOaeHUGvyrnIwBmWomlfAuujtvPrxtF-5FBZxi_KdTUm/pubhtml?widget=true&amp;headers=false" width="90%" height=500></iframe>


## Create Your Own

## TO DO -- update all directions below to match new Google Sheet format

Before you begin, review previous tutorials in this book:
- [Share, Edit, and Host Code Templates with GitHub](../github/)
- [Create and Convert Map Data with GeoJson.io](../transform/geojsonio)

1. Go to the GitHub repository template (https://github.com/jackdougherty/leaflet-storymap) and fork a copy of this repo to your own GitHub account. Requires signup for a [free GitHub account](http://github.com). Reminder: if you have already forked one copy, go to your GitHub repository Settings to rename or delete the first copy, so that you may create a second copy.
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
10. Learn more about how to edit your GitHub branches and make 'pull requests' to save changes from one branch to the other in the [GitHub section in this book](../github/).

##Examples and Extended Features
See how other readers have used this template to tell their own map stories, and added more features with flexible Leaflet code.  
- Explore at http://pembrokesoundscapes.ca/map, view code at https://github.com/rblades/rblades.github.io -- Added audio playback in the narrative, historical map layers.

{% footer %}
{% endfooter %}
