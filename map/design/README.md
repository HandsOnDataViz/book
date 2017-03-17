# Map Design Principles
*by [Jack Dougherty](../../introduction/who.md), last updated March 17, 2017*

** TO DO **
- rewrite questions to match script, and insert visual examples
- after questions, expand map principles and refer to related chart principles
- refer also to the Detect Bias chapters

** TO DO**
## Design with ColorBrewer
- explain the problem: how do we choose colors when designing a polygon (aka choropleth) map?
- a very useful tool is ColorBrewer,  http://colorbrewer2.org, created by Cynthia Brewer, Mark Harrower and the Pennsylvania State University

![Screenshot: ColorBrewer web interface](colorbrewer.png)

1) Number of data classes (also known as "buckets"). More does not necessarily mean better. Try different numbers and color schemes, and decide if you (and your audience) can easily distinguish between them.
- a smaller number sorts your data into fewer buckets, and shows a more "coarse" map, but colors differences become more visible
- a larger number sorts your data into more buckets, and shows a more "granular" map, but color differences become harder to see
- insert visual legend of each

2) Nature of data:
- Sequential: best to show steps from lower values (light color) to higher values (dark color)
  - example: a scale that increases from 1 to 100
- Diverging: best to show extremes (dark colors) around a neutral middle (light color)
  - example: a scale that highlights extremes from -100 to 0 to 100
- Qualitative: best to show different categories, represented by their own color
  - example: a map legend of the dominant crop in each area: apples, oranges, bananas

3) Pick a color scheme, with options for colorblind-safe and print-friendly.
- Think about the ideal format for your audiences. Will they view your visualizations on a computer screen and/or paper?

4) Click the Export tab to view all options. Some Leaflet map templates in this book use specific color names (such as "red" or "darkgreen") and some use hexadecimal codes, abbreviated as "hex codes" (such as #ff0000 or #336600). To learn more, use a Color Picker tool, such as https://www.w3schools.com/colors/colors_picker.asp

## Learn more
- Lisa Charlotte Rost, “Your Friendly Guide to Colors in Data Visualisation,” Lisa Charlotte Rost, April 22, 2016, https://lisacharlotterost.github.io/2016/04/22/Colors-for-DataVis/.

{% footer %}
{% endfooter %}
