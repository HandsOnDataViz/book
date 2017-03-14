# Fork and Edit a Simple Leaflet Map with GitHub
*By [Jack Dougherty](../../introduction/who.md), last updated March 14, 2017*

This tutorial introduces the **basic steps** of working with code templates, using a simple Leaflet map code (http://leafletjs.com) and GitHub in your browser (http://github.com). You will learn how to:
- A) Fork (copy) the Leaflet map code template to your GitHub account
- B) Publish your live map to the public web with the GitHub Pages
- C) Modify the map title and add controls to change map layers
- D) Upload more geocoded map points from a comma-separated-values (.CSV) sheet

Code templates help us to move beyond the limits of drag-and-drop web mapping services (such as BatchGeo and Google MyMaps) and to create more customized visualizations on a web server that you control. Before you begin, learn the broad concepts in the chapter introduction [Modify and Host Code Templates with GitHub](../github). For more advanced examples, see the [Leaflet Map Templates](../leaflet) chapter in this book.

## Try it
You will begin this tutorial with a simple interactive map that includes one pop-up point:
<iframe src="https://jackdougherty.github.io/leaflet-map-simple/" width="90%" height=350></iframe>

By the end of this tutorial, you will learn how to modify the map and add a new CSV spreadsheet of pop-up points:
<iframe src="https://jackdougherty.github.io/leaflet-map-simple-instructor-sample/" width="90%" height=350></iframe>

## Video with step-by-step tutorial

** TO DO - update video and expand tutorial steps **

{%youtube%}LT3wU4XAzWI{%endyoutube%}

Before you begin, sign up for a free GitHub account: http://github.com

1) Right-click to open this GitHub code template in a new tab: https://github.com/JackDougherty/leaflet-map-simple

2) In the upper-right corner of the code template, sign in to your free GitHub account

3) In the upper-right corner, click Fork to copy the template (also called a code repository, or repo) into your GitHub account. The web address (URL) of the new copy in your account will follow this format:
```
https://github.com/USERNAME/REPOSITORY
```

Reminder: You can only fork a GitHub repo **one time**. If needed, see how to [Make a Second Copy of a GitHub Repo](../second-copy) in this book.

4) In your new copy of the code repo, click on Settings, scroll down to the GitHub Pages area, select Master, and Save. This publishes your code template to a live map on a public website that you control.

5) Scroll down to GitHub Pages section again, to select and copy the link to your published web site, which will follow this format:
```
https://USERNAME.github.io/REPOSITORY
```

6) Scroll up to the top, and click on your repo name to go back to its main page.

7) At the top level of your repo main page, click on README.md, and click the pencil icon to edit this file, written in easy-to-read Markdown code.

8) Delete the existing link to my live site, and paste in the link to your site. Scroll down and Commit to save your edits.

9) On your repo main page, right-click on the link to your published site to open in a new tab. **Be patient ** because during busy periods, your website may take up to 1 minute to appear the first time.

10) Go back to your browser tab for your code repo. Click on the index.html file (which contains the map code), and click the pencil icon to edit it.

11) Explore the map code, which contains HTML, CSS, and JavaScript. Look for code comments that begin with "EDIT" for ideas about what you can easily change. Scroll down to Commit your changes.

12) Go to your live website browser tab and refresh the page to view your edits. **Be patient* during busy periods, when some edits may take up to 1 minute to appear.

## Try These Simple Map Edits

Although this book does not attempt to teach you how to code, it encourages you to be code-curious! Try making these edits to your index.html file in one browser tab, and then refresh the published website (and be patient) in another tab.

A) Edit the initial map zoom level (12) to any number between 1 (max zoom out) and 18 (max zoom in)

```JavaScript
// Set up initial map center and zoom level
var map = L.map('map', {
  center: [41.77, -72.69], // EDIT latitude, longitude to re-center map
  zoom: 12,  // EDIT from 1 to 18 -- decrease to zoom out, increase to zoom in
  scrollWheelZoom: false
});
```

B) Change the basemap layer by removing “.addTo(map)” from the Carto light layer, and adding it to the Stamen colored terrain layer

Your original code looks like this:
```JavaScript
// display Carto basemap tiles with light features and labels
L.tileLayer('https://cartodb-basemaps-{s}.global.ssl.fastly.net/light_all/{z}/{x}/{y}.png', {
  attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>, &copy; <a href="https://carto.com/attribution">CARTO</a>'
}).addTo(map); // EDIT - insert or remove ".addTo(map)" before last semicolon to display by default

// display Stamen basemap tiles with colored terrain and labels
L.tileLayer('https://stamen-tiles.a.ssl.fastly.net/terrain/{z}/{x}/{y}.png', {
  attribution: 'Map tiles by <a href="http://stamen.com">Stamen Design</a>, under <a href="http://creativecommons.org/licenses/by/3.0">CC BY 3.0</a>. Data by <a href="http://openstreetmap.org">OpenStreetMap</a>, under <a href="http://www.openstreetmap.org/copyright">ODbL</a>.'
}); // EDIT - insert or remove ".addTo(map)" before last semicolon to display by default
```

Your modified code should look something like this:
```JavaScript
// display Carto basemap tiles with light features and labels
L.tileLayer('https://cartodb-basemaps-{s}.global.ssl.fastly.net/light_all/{z}/{x}/{y}.png', {
  attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>, &copy; <a href="https://carto.com/attribution">CARTO</a>'
}); // EDIT - insert or remove ".addTo(map)" before last semicolon to display by default

// display Stamen basemap tiles with colored terrain and labels
L.tileLayer('https://stamen-tiles.a.ssl.fastly.net/terrain/{z}/{x}/{y}.png', {
  attribution: 'Map tiles by <a href="http://stamen.com">Stamen Design</a>, under <a href="http://creativecommons.org/licenses/by/3.0">CC BY 3.0</a>. Data by <a href="http://openstreetmap.org">OpenStreetMap</a>, under <a href="http://www.openstreetmap.org/copyright">ODbL</a>.'
}).addTo(map); // EDIT - insert or remove ".addTo(map)" before last semicolon to display by default
```

C) Edit the latitude and longitude coordinates of the default blue point marker to show a new location. To find coordinates for any location and to learn more, go to http://www.latlong.net

```JavaScript
// display a default blue point marker with pop-up text
L.marker([41.77, -72.69]).addTo(map) // EDIT latitude, longitude to re-position marker
.bindPopup("Insert pop-up text"); // EDIT pop-up text message
```

D) Edit the marker pop-up text. See the last line of the code snippet above.

E) Copy and paste the two lines that contain the L.marker code, and change coordinates in the second instance, to add new markers to the map. Your modified code might look like this:

```JavaScript
// display a default blue point marker with pop-up text
L.marker([41.77, -72.69]).addTo(map) // EDIT latitude, longitude to re-position marker
.bindPopup("Insert pop-up text"); // EDIT pop-up text message

L.marker([41.55, -72.55]).addTo(map) // EDIT latitude, longitude to re-position marker
.bindPopup("Insert pop-up text"); // EDIT pop-up text message
```

## Learn more
- See more [advanced Leaflet Map Templates](../leaflet) in this book
- About Leaflet https://leafletjs.com
- GitHub Pages features and tutorial, https://pages.github.com

{% footer %}
{% endfooter %}
