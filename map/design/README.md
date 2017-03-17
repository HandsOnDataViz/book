# Map Design Principles
*by [Jack Dougherty](../../introduction/who.md), last updated March 17, 2017*

** TO DO **
- rewrite questions to match script, and insert visual examples
- after questions, expand map principles and refer to related chart principles
- refer also to the Detect Bias chapters

** TO DO**
- explain the problem: which colors make sense in a polygon (aka choropleth) map?
- a very useful tool is ColorBrewer,  http://colorbrewer2.org, created by Cynthia Brewer, Mark Harrower and the Pennsylvania State University
- explain and give examples of these concepts
  - sequential data: best to show steps from low values (light color) to high values (dark color), such as a scale that increases from 1 to 100
  - diverging data: best to show extremes (dark colors) around a neutral middle (light color), such as a scale from -100 to 0 to 100
  - qualitative: best to show different categories, with their own color, such as a legend for most important product: apples, oranges, bananas

- choose number of data classes, nature of data, color scheme, color-blind and other options
- click Export tab to view all options; hex codes are typically used in Leaflet map code templates

![Screenshot: ColorBrewer web interface](colorbrewer.png)


{% footer %}
{% endfooter %}
