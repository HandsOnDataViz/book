OLD Google Sheets scatter and bubble tutorial

Create your own version using our [Scatter Chart with static data labels in Google Sheets template](https://docs.google.com/spreadsheets/d/1LJCj3RaVgaQsAZriV_JDQhBrIBSvnH_N1LBCkZK1bqs/). Go to *File > Make a Copy* to create a version in your Google Drive that you can edit. Select *only the two* columns that contain your numeric data, not all three columns, and go to *Insert > Chart*. If Google Sheets does not automatically guess the type of chart you wish to create, go to the *Chart type* dropdown and select *Scatter chart*. Make sure your x-axis is set to *Life Expectancy*, and your Series shows *Fertility*. Note that both columns display `123` icons, meaning they are numeric.

You will see a lot of scatter charts out there that do not label data points, and that's okay.
Some scatter plots are designed to show whether or not there is a correlation, and knowing
which points are which is not important. But sometimes labels are important for your storytelling.

In Chart editor, open the kebab menu (3 dots) of your Series dataset (Fertility), and then *Add labels*
(see Figure \@ref(fig:scatter-labels)).
The labels added by default will be the x-values of points. To make Google Sheets read
labels from the third column (*Country*), click the name of your label dataset (Life Expectancy),
then *Select a data range* button in the upper-right corner of the dropdown,
and choose cells in the relevant columns. Make sure to include the header (first row) if
all other data ranges include it.

(ref:scatter-labels) In the chart's Setup window, choose *Add labels* to the Series.

```{r scatter-labels, out.width="350px", fig.cap="(ref:scatter-labels)"}
knitr::include_graphics("images/06-chart/scatter-labels-annotated.png")
```

Tip: You may notice that some data points are too close to edges, and their labels are cut off.
To fix this, go to Customize tab of the Chart editor. There, you can set minimum and maximum values
for both horizontal and vertical axes. Unlike in bar charts, axes in scatter plots do not have to start at zero.
You can set your minimum and maximum values to be a few units below and above the extreme points of your
data range.

### Bubble Charts with 3 columns {-}
In this tutorial, we will show you a little trick that you can use if you want a scatter chart
with both data values displayed in a tooltip. We will use the same
World Bank dataset as we did for the scatter plot.

The bubble chart (more about the *proper* use of bubble charts in the next section)
in Figure \@ref(fig:bubble-3) shows the same data as our scatterplot on life expectancy vs fertility.

In the interactive version of the chart, hover your cursor over each bubble (dot) to reveal a tooltip
with the country name and the two data points.

(ref:bubble-3) This bubble chart is essentially a scatter chart, because no other dimensions (colors, sizes) are used. [See data](https://docs.google.com/spreadsheets/d/1CL7joH_3wvMYo9HIiSuFP0Ykv_Nl5DK6DYYcd3_gFnU/edit?usp=sharing) by World Bank. Explore the [full-screen interactive version](https://docs.google.com/spreadsheets/u/3/d/e/2PACX-1vQtMosshgyX6YoPpHo9QhSPk-ckOw1_yRryTF_vYJooBeWF13RaPv2IrGffcpaiqHPwfKFJAWY0HwA3/pubchart?oid=2105121864&format=interactive).

```{r bubble-3, fig.cap="(ref:bubble-3)"}
if(knitr::is_html_output(excludes="markdown")) knitr::include_url("https://docs.google.com/spreadsheets/d/1CL7joH_3wvMYo9HIiSuFP0Ykv_Nl5DK6DYYcd3_gFnU/pubchart?oid=2105121864&amp;format=interactive") else knitr::include_graphics("images/06-chart/bubble-3.png")
```

The data for this example is available in [Google Sheets Bubble chart with 3 columns template](https://docs.google.com/spreadsheets/d/1CL7joH_3wvMYo9HIiSuFP0Ykv_Nl5DK6DYYcd3_gFnU/).

Notice that we moved the labels column (*Country*) to be the first one in the dataset,
but the order shouldn't matter in this case. So our first column is the label for each bubble,
the second column is the data to be plotted on horizontal x-axis, and the third column (fertility)
will be placed on the y-axis.

Select all three columns, and go to *Insert > Chart*. Google Sheets will likely create a stacked
column chart by default, so choose *Bubble* from the Chart type dropdown window.

If you want to remove labels from the bubbles, remove the *ID* series (click on the kebab menu > Remove).

Unfortunately, there is no easy way to reduce all bubbles to a uniformly smaller size.
In the following section, we will introduce you to the proper way of using bubble charts.

### Bubble Charts with 5 columns {-}
Bubble charts are a good alternative to scatter charts if you need to include
one or two extra series in addition to your x- and y-coordinates. One of those
can be expressed through bubble size (bigger bubbles represent larger values).
Another one can make use of color (best for categorical data).

The bubble chart in Figure \@ref(fig:bubble-5) shows fertility and life expectancy for a subset of the nations,
with population (shown by bubble size) and region (shown by bubble color).
Float your cursor over bubbles to view data details in the interactive version of the chart.

(ref:bubble-5) This bubble chart shows fertility and life expectancy for several countries, including their population (shown by bubble size) and region (shown by bubble color). [See data](https://docs.google.com/spreadsheets/d/1YgBWYm9nTGlCuyqSwU3SDb7xk-SMSPgjfYq5iLqL0nQ/) by World Bank. Explore the [full-screen interactive version](https://docs.google.com/spreadsheets/d/e/2PACX-1vQV0lrK1Lomxg-2IJJAYrB8Dvb9uc9mu5bKM2S8sWHzY9-E6ajoZwU4fRSghe2kXIHcmK4SfZO2NG4B/pubchart?oid=200651442&format=interactive).

```{r bubble-5, fig.cap="(ref:bubble-5)"}
if(knitr::is_html_output(excludes="markdown")) knitr::include_url("https://docs.google.com/spreadsheets/d/e/2PACX-1vQV0lrK1Lomxg-2IJJAYrB8Dvb9uc9mu5bKM2S8sWHzY9-E6ajoZwU4fRSghe2kXIHcmK4SfZO2NG4B/pubchart?oid=200651442&amp;format=interactive") else knitr::include_graphics("images/06-chart/bubble-5.png")
```

The five-column dataset is available in this [Google Sheets Bubble chart with 5 columns template](https://docs.google.com/spreadsheets/d/1YgBWYm9nTGlCuyqSwU3SDb7xk-SMSPgjfYq5iLqL0nQ/).
The columns are arranged in the following order: country label, x-axis value,
y-axis value, color, and bubble size.

(ref:bubble-5-data) Bubble chart data. Bubble size represents population, color – region.

```{r bubble-5-data, out.width="400px", fig.cap="(ref:bubble-5-data)"}
knitr::include_graphics("images/06-chart/bubble-5-data.png")
```

Select all data and go to *Insert > Chart*, and choose Bubble as the Chart type.
Make sure your *ID*, *X-axis*, *Y-axis*, *Series*, and *Size* fields
contain the series you want to display, and make sure to have *Use row 1 as headers* option checked.

To change labels color, go to Customize tab of the Chart editor, and set Text color under the Bubble menu.
Make it gray or black, so that it won't interfere with the bubble colors themselves.

Tip: If some of your bubbles are too close to the borders, set Min and Max values for the axis manually
under Horizontal axis and Vertical axis menus.
