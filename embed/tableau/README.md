# Embed a Tableau Public visualization

A Tableau Public visualization can be embedded in your own website as an iframe, like the interactive example below. Try it by floating your cursor over the data points.

<iframe src="https://public.tableau.com/views/DataVizForAll-scatter-chart/Sheet1?:showVizHome=no&:embed=true" width="500" height="500"></iframe>

1) In the Tableau Public server page, click the Share button and copy the source link (not the embed code).

![](TableauPublic-edit-embed.png)

2) For this example, the source link for the embedded visualization above is:

```html
https://public.tableau.com/views/DataVizForAll-scatter-chart/Sheet1?:embed=y&:display_count=yes&:showTabs=y
```

3) Delete the code after the question mark, to make it look like this:

```html
https://public.tableau.com/views/DataVizForAll-scatter-chart/Sheet1?
```

4) Add this code to the end, to replace what you deleted above:

```html
:showVizHome=no&:embed=true
```

5) The modified source link should appear like this:

```html
https://public.tableau.com/views/DataVizForAll-scatter-chart/Sheet1?:showVizHome=no&:embed=true
```

6) To embed inside WordPress.org, the iframe plugin must be installed, as described in the chapter. . .  Insert the modified source link inside the iframe shortcode, like this:
```html
[iframe src="https://public.tableau.com/views/DataVizForAll-scatter-chart/Sheet1?:showVizHome=no&:embed=true"]
```

To learn more about embedding Tableau Public visualizations with iframe, see: http://kb.tableau.com/articles/howto/embedding-tableau-public-views-in-iframes

{% footer %}
{% endfooter %}
