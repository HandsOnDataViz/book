# Create an XY Scatter Chart with Tableau Public
*by [Jack Dougherty](../../introduction/who.md), last updated March 15, 2017*

An interactive scatter chart shows the relationship between two variables by displaying a series of XY coordinates. Readers can float their cursor over points to view specific details. The chart below, which illustrates the strong relationship between Connecticut school district income and test scores, was created with the free downloadable tool for Mac and Windows, Tableau Public http://public.tableau.com

## Try it

<iframe src="https://public.tableau.com/views/CTSchoolDistrictsbyIncomeandGradeLevels2009-13/Sheet1?:showVizHome=no&:embed=true" width="90%" height="500"></iframe>

## Video with step-by-step tutorial

{%youtube%}70RKjT91cjs{%endyoutube%}

1) Read the [Tableau Public tool review](../tableau-public) in this book, then download and install the free application on a Mac or Windows computer from http://public.tableau.com. Requires a free account.

2a) Right-click this link to Save this Excel file to your computer: [ct-districts-income-grades-2009-13](ct-districts-income-grades-2009-13.xlsx).

2b) Or, if you do not have Excel, Right-click this link to Save this CSV file to your computer: [ct-districts-income-grades-2009-13](ct-districts-income-grades-2009-13.csv), which contains the data sheet, but not the source notes sheet.

3) Open the file with any spreadsheet tool to view three columns: district, median household income, and grade levels (above/below national average for 6th grade Math and English test scores). In the Excel version, see the source notes tab, which explains how this data is based on the work of Sean Reardon et al. at the [Stanford Education Data Archive](http://purl.stanford.edu/db586ns4974), Motoko Rich et al. at [The New York Times](http://www.nytimes.com/interactive/2016/04/29/upshot/money-race-and-success-how-your-school-district-compares.html), Andrew Ba Tran at [TrendCT](http://trendct.org/2016/05/06/wealth-and-grades-compare-connecticuts-school-districts/), and the American Community Survey 2009-13 via [Social Explorer](http://socialexplorer.com).

Hint: To prepare your own scatter chart data from different sources, see the [Match Spreadsheet Columns with VLookup Function](../../spreadsheet/vlookup) chapter in this book.

4) Connect to your data file. If you downloaded the Excel file, Connect to Excel. Or if you downloaded the CSV file, Connect to Text.

5) Drag the Data sheet into the Data Source field.

6) In bottom-left corner, click Sheet 1 (you may see a Go To Worksheet reminder). Although the Tableau Public worksheet may feel overwhelming at first, the key is learning where to drag items from the data tab into the main worksheet.

7) Drag the Grade Levels measure into the Rows field.

8) Drag the Median Household Income measure into the Columns field. The initial chart will appear as one point, but that's because all of the data is aggregated together. We're not done yet.

9) Drag the District dimension into the lower portion of the Marks area. Now your scatter chart will appear, and float your cursor over each point to view details.

10) Click Sheet 1 to rename the title of your chart.

11) Click the Worksheet menu to Show Caption and type in data sources.

12) Recommended: Click the Standard menu (above Columns) to change view to Fit Width.

![](tableau-standard-fit-width.png)

13) To share your chart to the web, select File > Save to Tableau Public As. Requires signup for a free Tableau account.  

14) Click Edit Details. Give your workbook a meaningful title, since this name will appear in the URL for your published work on the Tableau Public server.

15) In the toolbar settings, see the checkbox to Allow workbook and its data to be downloaded by others.

![Screenshot: Toolbar settings in Tableau Public](tableau-toolbar-settings-allow.png)

Checking this box enables the Download button at the bottom of your published work, which allows users to access your data and workbook, to see how you constructed the visualization.

![Screenshot: Download button in Tableau Public](tableau-download.png)

16) Click the Save button to publish your work on the public web (and that's why they call it Tableau Public).

17) After saving your chart to the web, Tableau Public will automatically open the link in your default web browser. Or, see your public works in your Tableau Public online profile, which follows this format:
```
https://public.tableau.com/profile/USERNAME
```

## Learn more
- Insert your interactive chart in your own website in the [Embed On Your Web](../../embed/) chapter of this book, and in particular, [Embed Tableau Public on your Website](../../embed/tableau).
- Combine multiple visualizations and tell stories with Tableau Public dashboard and story point features
- See Tableau Public Resources, with how-to videos and sample data, https://public.tableau.com/en-us/s/resources

{% footer %}
{% endfooter %}
