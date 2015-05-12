# Expandable geocoded point map with Google Fusion Tables

Google Fusion Tables (GFT) is a free tool that allows users to upload and geocode a spreadsheet of location data, create an interactive point map with a numerical legend, and embed the product in a web page, like this:

<iframe width="100%" height="400" src="https://www.google.com/fusiontables/embedviz?q=select+col2+from+1OenqPrEAJVZDQrUe5fSeElMMVjrUbHTN9JoN0KU&viz=MAP&h=false&lat=44.517390498730755&lng=-89.70086420624999&t=1&z=6&l=col2&y=2&tmplt=2&hml=GEOCODABLE"></iframe>

*Click markers to explore Wisconsin Education Association Council affiliates, by origin, 1921-73*

GFT requires a free [Google Drive account](http://drive.google.com/) (use a regular Google username; avoid limited-access Google Apps for Education accounts). For general information, see Google documentation "[About Fusion Tables](https://support.google.com/fusiontables/answer/2571232)" and "[Create a Map](https://support.google.com/fusiontables/answer/2527132)" and also the [GFT Help Page](http://www.google.com/support/fusiontables/).

## Download and understand your data
Before starting to map, closely examine your data table to understand its meaning, sources of origin, and limitations.

1) Click to open the sample spreadsheet data, examine the source information, and determine what it does -- and does not tell us. For example, who added the present-day zip codes to this historical data? Why do they appear for some affiliates but not others?

- [sample spreadsheet location data of WEAC affiliates](https://docs.google.com/spreadsheet/ccc?key=0AtmGKybdRLlZdGlUM3hhUWhUZ1BibXdFbFFqLWVYbnc&usp=sharing), by year of origin, 1921-73 in Google Spreadsheet format, which you may File > Make a copy (to save to your Google Drive), or File > Download (to save in Excel .xlsx format on your hard drive)

Upload spreadsheet data to Google Fusion Tables (GFT)

Sign in to your Google Drive account and go to Create > Fusion Table (experimental).

If Fusion Tables is not listed, go to Create > Connect More Apps, search for "Fusion" and Connect the Fusion Tables app to your Google Drive account, as shown below:





TO DO: To display textual data, rather than numerical, in a GFT legend, see this solution: https://github.com/JackDougherty/FusionTable-Map-custom-legend