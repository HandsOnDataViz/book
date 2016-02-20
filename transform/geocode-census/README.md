# Geocode address data with US Census Geocoder

**TO DO**: Write more detailed instructions for below

** TO DO** Create Hartford-area diagram of this relationship:
- State
- County
- County Subdivision
- Tract
- Block Group

Overview of key steps:
1) Organize address data with spreadsheet tool, such as Excel, and clean up unnecessary commas
2) Save data into 5 columns (id, address, city, state, zip) in .CSV format, without column headers
3) Upload data into US Census Geocoder: https://www.census.gov/geo/maps-data/data/geocoder.html, in batches of 1,000 addresses at a time
4) Sort geocoded results (match exact, match non-exact, tie, no-match), and clean and regeocode as needed
5) In spreadsheet, use the VLOOKUP function to join census block groups to demographic data

[Download 50 Sample Addresses in CSV format](sample-addresses-50.csv)

Detailed steps:

Explain census tracts and census-block groups, and ACS 5-year data.

1) In spreadsheet tool (such as MS Excel), copy data and organize into 5 columns, with NO column headings:
Unique ID number
Address (number and street, such as 100 Main Street)
City
State
Zipcode

Note: If the data does not include the state, then insert it as a new column

Note: If the Address column includes extra commas, like this:
100 Main St, Apt 2, Hartford, CT, 06112

Then create blank columns after the Address column; select Address column; Data > Text to Column
https://support.office.com/en-us/article/Split-text-into-different-cells-30b14928-5550-41f5-97ca-7a3e9c363ed7

2) When spreadsheet data is in 5 specific columns, save in .CSV format, which means comma-separated values. The output will appear as follows in a text editor:
1, 100 Main St, Hartford, CT, 06112

3) Upload in batches of 1,000 rows or less.

4) Geocoded results will be downloaded by the site in this format:
[insert]

Note: To re-run unmatched or tie data. . .

Note: If you wish to share de-identified data with others, remove the individual home addresses and share only the census block groups.

5) To census tracts or block groups with existing data, use VLookup function. . .

Read more about geocoding services
http://dlab.berkeley.edu/blog/address-geocoding-options-uc-berkeley-community

---
[Improve this book:](gitbook/improve.md) select text to insert comment, or suggest edits.

[Data Visualization for All](http://datavizbook.org)
copyrighted by [Jack Dougherty and contributors](introduction/who.md)
is distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0).
You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a>
