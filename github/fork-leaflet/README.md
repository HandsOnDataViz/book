# Fork, Host, and Edit a Simple Leaflet Point Map Template with GitHub
*By [Jack Dougherty](../../introduction/who.md), last updated March 5, 2017*

This tutorial shows how to fork (copy), host, and edit a very simple point map, created with the open-source Leaflet code library (http://leafletjs.com), using GitHub (http://github.com) in your browser.

This basic tutorial teaches only the first steps of hosting and editing code templates. The goal is to help you move beyond the limitations of drag-and-drop web mapping services (such as BatchGeo and Google MyMaps), to create more customized maps on a web server that you control. To learn more, see additional [Leaflet Map Templates](../leaflet) in this book.

## Tool Review
Leaflet (http://leafletjs.com) is an open-source code library for users to create interactive maps. See tool review in the [Leaflet chapter](../leaflet) in this book.

GitHub (http://github.com) is a versatile tool to share, edit, and host simple code templates on the public web. Requires a free account. See also in this book the [introductory GitHub chapter](../github) and the earlier book chapter on [Creating Simple Web Pages with GitHub Pages](../embed/github-pages).
- Pros:
  - Free and easy-to-learn tool to share, edit, and host simple code templates.
  - All steps below can be completed in your web browser.
  - Easy to download and migrate open-source code to a different web server.
- Cons:
  - All work on GitHub is public by default. Private repositories (folders) require payment.
  - New users sometimes confuse the links for code repositories versus published web pages.

## Try it
You will copy and edit a very simple interactive point map like the one below:
<iframe src="https://jackdougherty.github.io/leaflet-map-simple/" width="90%" height=400></iframe>

## Video with step-by-step tutorial
{%youtube%}LT3wU4XAzWI{%endyoutube%}

1) Right-click to open this GitHub code template in a new tab: https://github.com/JackDougherty/leaflet-map-simple

2) Sign in to your free GitHub account

3) In the upper-right corner, click Fork to copy the template (also called a code repository, or repo) into your own account. Important: You can only fork a GitHub repo **one time**. To make a second copy, see chapter **TO DO**

4) In your new copy of the code repo, click on Settings, scroll down to the GitHub Pages area, select Master, and Save. This publishes the code to a public website that you control.

5) Scroll down to GitHub Pages section again, to select and copy the link to your published web site.

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
- See more [advanced Leaflet Map Templates](../leaflet) in this book.
- GitHub Pages features and tutorial, https://pages.github.com

{% footer %}
{% endfooter %}
