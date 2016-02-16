# Embed a Tableau Public visualization

To embed a Tableau Public data visualization as an iframe, like this:

<iframe src="https://public.tableau.com/views/DataVizBook-simple-scatterchart/Sheet1?:showVizHome=no&amp;:embed=true"></iframe>

1) In the Tableau Public server page, click the Share button and copy the source link (not the embed code).

![](TableauPublic-edit-embed.png)

2) For this example, the source link for the embedded visualization above is:

```html
https://public.tableau.com/views/DataVizBook-simple-scatterchart/Sheet1?:embed=y&amp;:display_count=yes&amp;:showTabs=y
```

3) Delete the code after the question mark, to make it look like this:

```html
https://public.tableau.com/views/DataVizBook-simple-scatterchart/Sheet1?
```

4) Add this code to the end, to replace what you deleted above:

```html
:showVizHome=no&:embed=true
```

5) The modified source link should appear like this:

```html
https://public.tableau.com/views/DataVizBook-simple-scatterchart/Sheet1?:showVizHome=no&:embed=true
```

6) To embed inside WordPress.org, the iframe plugin must be installed, as described in the chapter. . .  Insert the modified source link inside the iframe shortcode, like this:
```html
[iframe src="https://public.tableau.com/views/DataVizBook-simple-scatterchart/Sheet1?:showVizHome=no&:embed=true"]
```

To learn more about embedding Tableau Public visualizations with iframe, see: http://kb.tableau.com/articles/howto/embedding-tableau-public-views-in-iframes
