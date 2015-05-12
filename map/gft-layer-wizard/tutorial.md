# Overlay Maps with Fusion Tables Layer Wizard

One reason to create maps with Google Fusion Tables is the ability to overlay them on top of one another to view patterns in your data. A simple tool to overlay maps is the [Fusion Tables Layer] Wizard(http://fusion-tables-api-samples.googlecode.com/svn/trunk/FusionTablesLayerWizard/src/index.html).

![]FusionTablesLayerWizard.png
*Static screenshot of the tool*

Follow these instructions:

- For each Google Fusion Table, change the sharing settings to "public" or "anyone with the link" can view.
- Add map layers one at a time, beginning with the bottom layer (in this example, a colored polygon map).
- For each map, copy and paste the link found at Tools > Publish > Send a link.
- Click the *Add Layer* button to insert another. Optional: add a search feature.
- Center and zoom into the preview map as you desire it to be displayed.
- Adjust map dimensions and stylize base map as desired.

Copy and paste the automated HTML code into a web page to display your interactive multi-layered map. (If you need a web publishing solution, see the GitHub Pages tutorial in this book.) Any changes you make to the underlying Google Fusion Tables will appear in the multi-layered map.

<style>
    #map-canvas { width:600px; height:400px; }
    .layer-wizard-search-label { font-family: sans-serif };
  </style>
  <script type="text/javascript"
    src="http://maps.google.com/maps/api/js?sensor=false">
  </script>
  <script type="text/javascript">
    var map;
    var layer_0;
    var layer_1;
    function initialize() {
      map = new google.maps.Map(document.getElementById('map-canvas'), {
        center: new google.maps.LatLng(41.63778483593867, -72.52362170468746),
        zoom: 9,
        mapTypeId: google.maps.MapTypeId.ROADMAP
      });
      layer_0 = new google.maps.FusionTablesLayer({
        query: {
          select: "col2>>1",
          from: "10Lf_WvY-PiojybhpPGw8DcxkNa9UeAMN0-go4CTx"
        },
        map: map,
        styleId: 2,
        templateId: 2
      });
      layer_1 = new google.maps.FusionTablesLayer({
        query: {
          select: "col9",
          from: "19dKubosLdlkch9vXK-i7bNp3OxdwImTolwnwdZ9d"
        },
        map: map,
        styleId: 3,
        templateId: 5
      });
    }
    google.maps.event.addDomListener(window, 'load', initialize);
  </script>
  <div id="map-canvas"></div>
*Sample interactive multi-layered map from [Fusion Tables Layer Wizard] tool(http://fusion-tables-api-samples.googlecode.com/svn/trunk/FusionTablesLayerWizard/src/index.html)
