# Create an XY Scatter Chart with Tableau Public

*by [Jack Dougherty](introduction/who.md), last updated February 16, 2016*

A scatter chart shows the relationship between two variables by displaying a series of XY coordinate points. For example, if you want to view the relationship between a school district's test scores and its student poverty levels, place both of these variables inside an XY scatter chart, as shown below. With an online interactive version, viewers can explore the data and float over or click any point to see its label. Try this sample:

<script type='text/javascript' src='https://public.tableau.com/javascripts/api/viz_v1.js'></script><div class='tableauPlaceholder' style='width: 750px; height: 600px;'><noscript><a href='http:&#47;&#47;www.datavizbook.org&#47;content&#47;chart&#47;scatter-chart-tableau&#47;index.html'><img alt='Sheet1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Da&#47;DataVizBook-simple-scatterchart&#47;Sheet1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz' width='981' height='741' style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='site_root' value='' /><param name='name' value='DataVizBook-simple-scatterchart&#47;Sheet1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Da&#47;DataVizBook-simple-scatterchart&#47;Sheet1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='showVizHome' value='no' /><param name='showTabs' value='y' /><param name='bootstrapWhenNotified' value='true' /></object></div>

## Prepare your XY data
For a simple XY scatter chart, create a spreadsheet that contains three columns: data labels, variable 1, and variable 2. For example, to compare how Connecticut school districts vary by student poverty and test scores, this 3-column spreadsheet was created from two different tables in the [Connecticut Open Data repository, Education section](https://data.ct.gov/Education). [Download the sample data](CT-Districts-StudentPoverty-TestScore-2012-13.csv) in CSV format, which opens in any spreadsheet tool.

![](TableauPublic-prepare-data.png)

Learn how to join two different tables that share a similar column, with the VLookup spreadsheet tutorial in this book, **to do**

## The Tableau Public tool
Several tools can create scatter charts, but Tableau Public offers a relatively quick way to produce a highly interactive version that can easily be embedded on your site, with links to the data source.

Download and install Tableau Public (https://public.tableau.com/), currently available for Mac or Windows. The free Tableau Public app requires your data to become public, as the name suggests, and is designed for academics, journalists, and non-profit organizations that wish to publish data visualizations on the open web. If you wish to keep your visualizations and the underlying data private, the company sells a similar app called Tableau Desktop. (This tutorial displays screens from version 9.2 for Mac.)

Start up Tableau Public. Click connect to link to the data you prepared above, in an Excel spreadsheet, a generic text file (CSV, comma separated values), or a statistical file (for applications such as SAS, SPSS, and R.)

![](TableauPublic-connect.png)

Tableau Public opens a new workbook and shows the data source tab, to confirm that your spreadsheet has been uploaded correctly. To create your visualization, go to the worksheet by clicking "Sheet 1" in the bottom-left corner.

![](TableauPublic-data-source-go-to-worksheet.png)

At first glance, the Tableau Public worksheet can feel overwhelming. Don't let it scare you. We're going to do an easy one, together. On the left side, see the three columns of data. Tableau Public has automatically identified our first column (CT School District) as a "Dimension," and our second and third columns (test score and student poverty data) as "Measures."

![](TableauPublic-worksheet.png)

The key to Tableau Public is learning where to drag items from the data tab into the main worksheet.

Drag one measure (such as student poverty) into the Columns field, where it will turn green. Drag the other measure (test scores) into the Rows field, where it also will turn green. The initial chart will appear as one dot, with all of your data clumped together, but don't worry. We're not done yet.

![](TableauPublic-drag-each-measure.png)

Drag the dimension (school districts) into the bottom of the Marks tab. Your scatter chart will appear. Float over each point to reveal its label and underlying data.

![](TableauPublic-drag-dimension.png)

To reinforce the concept, here's a short animated loop of the two dragging steps above.

![](TableauPublic-scatter-chart-640.gif)

## Sharing your Tableau Public on the web

Go to File > Save to Tableau Public As. The next step requires signing up for a free Tableau account and profile.

![](TableauPublic-save-as.png)

Save your Tableau Public workbook, and give it a meaningful name. Your interactive chart and underlying data will be published on the Tableau server and become publicly available.

After your workbook is saved on the server, Tableau Public should automatically open it in your default web browser. But if no workbook appears, look in your Tableau Public profile, which follows this format: https://public.tableau.com/profile/USERNAME

Click the Edit Details button to modify the title or add a brief description. Click the Share button to copy the embed code. Learn how to embed the interactive chart in your own website, in the [Publish section of this book](publish/README.md).

![](TableauPublic-edit-embed.png)

---
[Improve this book:](gitbook/improve.md) select text to insert comment, or suggest edits.

[Data Visualization for All](http://datavizbook.org)
copyrighted by [Jack Dougherty and contributors](introduction/who.md)
is distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0).
You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a>
