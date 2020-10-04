But what if you need to geocode dozens, hundreds, or even thousands of addresses?
In this section, we will look at two ways to geocode larger lists of addresses.
First, you'll learn how to use our custom-built
[Google Sheets Geocoder](https://github.com/HandsOnDataViz/google-sheets-geocoder),
which lets you convert addresses using Google Geocoder (available pretty much worldwide)
and the US Census Geocoder (for US addresses only).
Second, you'll learn how to use a stand-alone US Census Geocoder that allows you
to upload a file with up to 10,000 addresses within the US, and download geocoded results.

Note: Using Google Maps Geocoder within Google Sheets (App Script) does not require
an API key. In the past, free tier was restricted by 1,000 geocoding requests in 24 hours.
Since 2018, [use quotas are unclear](https://developers.google.com/apps-script/guides/services/quotas),
but we believe the new limit is [up to 50 requests per minute](https://developers.google.com/maps/documentation/geocoding/usage-and-billing#other-usage-limits).


#### Geocode addresses with Google Sheets Geocoder {-}

The Google Sheets Geocoder script lives inside [a special Google Sheet](https://docs.google.com/spreadsheets/d/1XvtkzuVyQ_7Ud47ypDJ4KOmz_5lOpC9sqeEDBbJ5Pbg/edit#gid=0)
that you should *copy* to your own Google Drive (you don't need editing access, just go to *File > Make a copy*).

The spreadsheet contains six columns. Populate the first column, *Location*, with your addresses.
The remaining five columns will be filled by the geocoding script. Select all six columns,
go to *Geocoder* in the menu, and choose which geocoding utility to use, like is shown in Figure \@ref(fig:sheets-geocoder).

(ref:sheets-geocoder) Put addresses in the first column, and use Geocoder to fill in the remaining five.

```{r sheets-geocoder, fig.cap="(ref:sheets-geocoder)"}
if(knitr::is_html_output(excludes="markdown")) knitr::include_url("images/14-transform/sheets-geocoder.gif", height="280px") else knitr::include_graphics("images/14-transform/sheets-geocoder.png")
```

Note: If your address data is split into multiple columns (such as *Street*, *City*, and *State*),
revisit [Clean Data with Spreadsheets](clean-spreadsheets.html) section to remind yourself
how to "glue" multiple cells into one.

The first time you run the Geocoder script, it will ask for your permission. TODO: since we still need Google to authorize our script, you will need to click *Advanced* and then *Go to Geocoder (unsafe)* near the bottom of the next screen. Trust us -- our script is safe to use! The code is open-source and is available [on GitHub](https://github.com/HandsOnDataViz/google-sheets-geocoder), so you or your programmer friend can make sure it doesn't steal your personal data. Sorry for the inconvenience.

Once the script finishes executing, you will get a pop-up notification that will tell you how many addresses
were successfully geocoded, and how many failed. Inspect *Found* and *Quality* columns to ensure the geocoder matched your addresses correctly.
Then look at the failed addresses and see if you can spot problems with them. For tips about
using Google geocoder, see [documentation](https://developers.google.com/maps/faq#geocoder_queryformat).

Note: The Geocoder plugin is a small Apps Script program that is connected to your Google sheet.
It sends your addresses to either [US Census Geocoder](https://geocoding.geo.census.gov/geocoder),
or [Google Geocoding API](https://developers.google.com/apps-script/reference/maps/geocoder),
and gets geocoded results as a response.

#### Geocode US addresses to census tracts with Google Sheets Geocoder {-}

You can use a modified version of the Google Sheets Geocoder, available in
[its own spreadsheet](https://docs.google.com/spreadsheets/d/1x_E9KwZ88c_kZvhZ13IF7BNwYKTJFxbfDu77sU1vn5w/edit#gid=0),
to assign census tracts and GeoIDs to addresses within the United States.

A GeoID is a unique identifier of a place according to the US Census. A sample 15-digit
GeoID, `090035245022001`, consists of a state (09), followed by county (003),
followed by census tract (524502, or more conventional 5245.02),
followed by a census block group (2), and finally a census block (001).

Make a copy of the [template spreadsheet](https://docs.google.com/spreadsheets/d/1x_E9KwZ88c_kZvhZ13IF7BNwYKTJFxbfDu77sU1vn5w/edit#gid=0)
into your own Google Drive by going to *File > Make a copy*.

You only need to populate the first column, *Location*. The rest seven columns
will be populated by the Geocoder. Similar to the previous template, select all eight columns,
and go to *Geocoder > US Census 2010 Geographies*, like is shown in Figure \@ref(fig:sheets-geocoder-censusgeo).

If you run this script for the first time, Google Sheets will ask you for permission to run,
and will possibly warn you that this script is unsafe. Once again, you shouldn't worry. The plugin
is open-source and you can inspect it to make sure it doesn't steal or retain your personal data.

(ref:sheets-geocoder-censusgeo) Put addresses in the first column, and use Geocoder to fill in the remaining seven.

```{r sheets-geocoder-censusgeo, fig.cap="(ref:sheets-geocoder-censusgeo)"}
if(knitr::is_html_output(excludes="markdown")) knitr::include_url("images/14-transform/sheets-geocoder-censusgeo.gif", height="330px") else knitr::include_graphics("images/14-transform/sheets-geocoder-censusgeo.png")
```

#### Insert Google Sheets Geocoder script into your own spreadsheet {-}

If you don't want to make a copy of the Google Sheet templates from the previous examples,
you can insert the open-source Geocoder scripts into your own Google sheet.

1. In your personal Google spreadsheet, go to *Tools > Script Editor*. This should open up a new tab.
1. Replace the empty `function myFunction()` with the contents of `geocoder-census-google.gs` from the plugin's [repo on GitHub](https://github.com/handsondataviz/google-sheets-geocoder).
1. In Script Editor, click *File > Save*. An *Edit Project Name* window will pop up, where you should give the script a meaningful name, such as "Geocoder".
1. Close the Script Editor, and go back to your spreadsheet. Refresh and wait for a couple of seconds. *Geocoder* should appear in the menu.
