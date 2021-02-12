## Point Map with BatchGeo {- #batchgeo}
Although BatchGeo is not the most powerful mapping tool available, its easy-to-learn interface stands out as one of the fastest ways to create an interactive point map. With the free version, organize up to 250 rows of data in a spreadsheet template, copy and paste them into the platform. BatchGeo will geocode your data and display map markers with colored categories on a Google Map base layer, which can be clicked to show linked titles, text, and small photos (which must be hosted online elsewhere) categories, descriptions, and links (including images hosted elsewhere online). Since the free version does *not* include an account login, enter your email to receive a link to the finished map, like the sample shown in Figure \@ref(fig:batchgeo-map).

(ref:batchgeo-map) Point map of museums and parks with BatchGeo: Explore the [interactive version](https://batchgeo.com/map/a36a85afb293fd0a7160997f0ff83e0c).

```{r batchgeo-map, fig.cap="(ref:batchgeo-map)"}
if(knitr::is_html_output(excludes="markdown")) knitr::include_url("https://batchgeo.com/map/a36a85afb293fd0a7160997f0ff83e0c", height="550px") else knitr::include_graphics("images/08-map/batchgeo-map.png")
```

To create your own point map with BatchGeo, follow this quick tutorial.

1. Open this [BatchGeo data template in Google Sheets](https://docs.google.com/spreadsheets/d/1IA0J4Z9C0_zsvgcunD2kHtR__sdQqUPzNHNjqCLYBRQ/edit#gid=312385679), log into your Google account, and go to *File > Make a Copy* to create a version you can edit in your Google Drive.

2. You can delete and enter your own data into the template, as shown in Figure \@ref(fig:batchgeo-template). Not every address field is required, but adding more will improve the accuracy of the geocoder. Several columns are optional and can be deleted (such as URL, Image URL, Image Source). If you enter a URL, its active link will appear in the Name field. Also, you can enter an Image URL if a photo is hosted elsewhere online, with an ideal size of 200x200 pixels.

(ref:batchgeo-template) Enter your data into the template, then select all and copy it.

```{r batchgeo-template, fig.cap="(ref:batchgeo-template)"}
knitr::include_graphics("images/08-map/batchgeo-template.png")
```

3. Select and copy your data from the template, open the [BatchGeo](https://batchgeo.com) site, click the large field, and paste in your data, as shown in Figure \@ref(fig:batchgeo-paste).

(ref:batchgeo-paste) Click the large field and paste in your data from the template.

```{r batchgeo-paste, fig.cap="(ref:batchgeo-paste)"}
knitr::include_graphics("images/08-map/batchgeo-paste.png")
```

4. Click the *Validate and Set Options* button to inspect or adjust how BatchGeo will upload your data fields and preview a pop-up window, as shown in Figure \@ref(fig:batchgeo-validate). Here you can change the default *Region* from *United States* to other areas of the world. Also, click the *Advanced* button to see more options to change the basemap layer or point symbols. Then click the *Make Map* button.

(ref:batchgeo-validate) Click the *Validate* button to inspect and preview your data and advanced options.

```{r batchgeo-validate, out.width=500, fig.cap="(ref:batchgeo-validate)"}
knitr::include_graphics("images/08-map/batchgeo-validate.png")
```

5. In the *Map* window, click the *Save and Continue* button to enter a title and set other options, such making your map *public* or *unlisted*, as well as customizing the layout, as shown in Figure \@ref(fig:batchgeo-save). Insert your email address to receive a link to your online map. Click *Save Map*.

(ref:batchgeo-save) Be sure to enter your email address to receive a link to your online map.

```{r batchgeo-save, out.width=500, fig.cap="(ref:batchgeo-save)"}
knitr::include_graphics("images/08-map/batchgeo-save.png")
```

6. Check your email for a message from BatchGeo with a link to your live map, and another link to make edits, as shown in Figure \@ref(fig:batchgeo-email). The email also will include a code to [embed your live map on the web, which you'll learn about in Chapter 10](embed.html).

(ref:batchgeo-email) Save the BatchGeo email with links and an embed code for your map.

```{r batchgeo-email, out.width=500, fig.cap="(ref:batchgeo-email)"}
knitr::include_graphics("images/08-map/batchgeo-email-annotated.png")
```

Overall, BatchGeo is a free and easy-to-learn point map tool, but one with several limitations. You can only create maps with 250 points or less, and only a few options to customize their appearance, unless you upgrade to the paid version. Also, while the tool geocodes your location data, it does not show you the latitude and longitude coordinates, but see the [Geocode section of Chapter 3 for a Google Sheets add-on](geocode.html) that will show you the geocoordinates. See more info on the [BatchGeo support page](http://support.batchgeo.com) and also their [post about power-user tips](https://blog.batchgeo.com/5-steps-to-become-a-batchgeo-power-user/).

Now that you've learned about one tool to create point maps, let's compare it with a second tool, Google My Maps, which includes some additional features.
