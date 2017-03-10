# Filtered line chart with Tableau Public
*by [Veronica X. Armendariz and Jack Dougherty](../../introduction/who.md), last updated March 10, 2017*

We created this interactive filtered line chart for a non-profit education advocacy group, which wanted web visitors to compare student achievement levels over time across forty schools. Since displaying all of the line charts at once is overwhelming, the filtered line chart provides checkboxes to turn on/off selected data lines to make specific comparisons. Readers can float their cursor over each line to identify the school name and data details. The tutorial below illustrates how to create your own version with a free downloadable tool for Mac and Windows computers, Tableau Public, https://public.tableau.com

## Try it
<iframe src='https://public.tableau.com/views/LineChartSample/Sheet1?:showVizHome=no&:embed=true' width="90%" height="530"></iframe>

** TO DO **
- update steps from Tableau Public v9 to v10.2
- insert video tutorial
- insert direct link https://public.tableau.com/profile/jackdougherty#!/vizhome/LineChartSample/Sheet1

Before you begin: Read the [Tableau Public tool review](../tableau-public) in this book, then download and install the free application on a Mac or Windows computer from http://public.tableau.com. Requires a free account.

Step 1: Organize your data in a format that Tableau Public can read. Before importing, examine your data in a spreadsheet tool (such as Microsoft Excel) and format the Year column as a Date. To avoid displaying “2007” as “1/1/2007,” create a custom date format as “yyyy,” which displays it as 2007. Also, leave all blank spaces in the spreadsheet as-is so that Tableau automatically converts them to “null” values during the data import.

Sample data files:
- [LineChartData.xlsx - long version](LineChartData.xlsx)
- [LineChartDataAY.xlsx - with academic years](LineChartDataAY.xlsx)
- [SchoolSnapshotSampleData.xlsx - sample school for Achieve Hartford](SchoolSnapshotSampleData.xlsx)

![](TPublicLineChart1.png)

Step 2: Download a free copy of [Tableau Public](https://public.tableau.com), open the application, and click the Open Data button. (Note that users may pay to upgrade to Tableau Professional to access live server data across a wide range of business platforms.)

![](TPublicLineChart2.png)

Step 3: Connect your spreadsheet data file to Tableau Public, search through your drive, and select it.

![](TPublicLineChart3.png)

Step 4: The sheets of your data file will automatically appear in Tableau Public and allow you to rename them if you wish. Any blanks will automatically convert to “null.” Click the Go to Worksheet button.

![](TPublicLineChart4.png)

Step 5: Tableau Public encourages users to select dimensions and measures, then drag-and-drop them into a grid of rows and columns, which serves as a framework for the interactive chart you wish to build. Dimensions are any information that is qualitative or categorical, while measures are quantitative information about the dimensions ([learn more from Tableau documentation](http://onlinehelp.tableau.com/v6.1/public/online/en-us/Id112A8A00YEX.html)).  In this example, we are creating a line chart with two dimensions (year and school) and one measure (test scores). Drag and drop Year into the Column area of the grid, which places our unit of time across the horizontal axis.

![](TPublicLineChart5.png)

Step 6: Drag and drop School Cohorts dimension into the Row area of the grid, which will display this dimension in the vertical axis.

![](TPublicLineChart6.png)

Step 7: Since Scores is a numerical measure, drag and drop this value into the middle of the grid, which will display all of the scores for each school and year.

![](TPublicLineChart7.png)

Step 8: We need to reformat the Score measure so that the numbers are displayed individually, and not aggregated by default. Select Score (but not its drop-down menu), then go to the Analysis menu and turn off Aggregated Measures. All of the data measures will be visible.

![](TPublicLineChart8.png)

Step 9: To visualize your data table as a line chart, go to the Show Me window and select Lines (continuous).

![](TPublicLineChart9.png)

Step 10: Initially, each School row appears at its own chart. To blend all of them together into one master chart, drag the School Cohort dimension to the Marks window and drop it on the Color button. All of the School lines will appear in one chart, with identifying colors.

![](TPublicLineChart10.png)

Step 11: To filter the line chart to display only selected items, go to the Marks window, select the School Cohort drop-down menu, and choose Show Quick Filter.

![](TPublicLineChart11.png)

Step 12: In the Quick Filter window, select only a few Schools to display.

![](TPublicLineChart12.png)

Step 13: Since the Quick Filter window shows users the schools they want to see, we don't necessarily need the legend that matches each school with a color. Optional: in the School Cohort window, select the drop-down menu and choose Hide Card to the color legend from your visualization.

![](TPublicLineChart13.png)

Step 14: Make sure that all of the wording on the axes appears exactly as desired, and double-click any element to edit. For example, double-click the horizontal x-axis to change text from “Year to Year” to simply “Year.”

![](TPublicLineChart14.png)

Step 15: Before saving your workbook, create a free Tableau Public account in your web browser. Once you have a valid login, in the Tableau Public app, go to File menu and select Save to Web As to save your work and make it publicly accessible. (If you wish to make your work private, upgrade to Tableau Professional.)

![](TPublicLineChart15.png)

Step 16: After saving your workbook, Tableau will generate a general view of how your visualization appears on the web, with an option to email the link. To embed the visualization in your website, copy the HTML embed code and paste it into a web page that can host this code.

## Learn more
- Insert your interactive chart in your own website in the [Embed On Your Web](../../embed/) chapter of this book, and in particular, [Embed Tableau Public on your Website](../../embed/tableau).
- Combine multiple visualizations and tell stories with Tableau Public dashboard and story point features
- See Tableau Public Resources, with how-to videos and sample data, https://public.tableau.com/en-us/s/resources

{% footer %}
{% endfooter %}
