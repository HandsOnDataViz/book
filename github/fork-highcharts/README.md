# Fork and Edit a Highcharts Scatter Chart with GitHub
*By [Jack Dougherty](../../introduction/who.md), last updated March 25, 2017*

This tutorial introduces the **basic steps** of working with code templates, using a simple Highcharts scatter chart code (http://highcharts.com) and GitHub in your browser (http://github.com). You will learn how to:
- A) Fork (copy) the Highcharts template to your GitHub account
- B) Publish your live chart to the public web with GitHub Pages
- C) Modify the chart title, subtitle, and axis labels
- D) Upload new data points from a comma-separated values (.csv) spreadsheet

Code templates help us to move beyond the limits of drag-and-drop web tools (such as Google Sheets and Tableau Public) and to create more customized visualizations on a web server that you control. Before you begin, learn the broad concepts in the chapter introduction [Modify and Host Code Templates with GitHub](../github). For more advanced examples, see the [Highcharts Templates](../highcharts) chapter in this book. If you have problems with this tutorial, go to the [Fix Common GitHub and Code Errors](../fix) chapter in this book.

## Try it
You will begin this tutorial with a basic chart template that includes only 7 points. Right-click to open [full-size chart in new tab](https://jackdougherty.github.io/highcharts-scatter-csv/).

<iframe src="https://jackdougherty.github.io/highcharts-scatter-csv/" width="90%" height=425></iframe>

By the end of this tutorial, you will learn how to modify the chart and add a new CSV spreadsheet with over 160 points. Right-click to open [full-size chart in new tab](https://jackdougherty.github.io/highcharts-scatter-csv-instructor-sample).
<iframe src="https://jackdougherty.github.io/highcharts-scatter-csv-instructor-sample/" width="90%" height=425></iframe>

## Video with step-by-step tutorial

{%youtube%}72pgCZqWg7Q{%endyoutube%}

#### A) Fork (copy) the Highcharts template to your GitHub account

Before you begin, sign up for a free GitHub account: http://github.com

1) Right-click to open this GitHub code template in a new tab: https://github.com/JackDougherty/highcharts-scatter-csv

2) In the upper-right corner of the code template, sign in to your free GitHub account

3) In the upper-right corner, click Fork to copy the template (also called a code repository, or repo) into your GitHub account. The web address (URL) of the new copy in your account will follow this format:
```
https://github.com/USERNAME/REPOSITORY
```

Reminder: You can only fork a GitHub repo **one time**. If needed, see how to [Make a Second Copy of a GitHub Repo](../second-copy) in this book.

#### B) Publish your live chart to the web with GitHub Pages
4) In your new copy of the code repo, click on Settings, scroll down to the GitHub Pages area, select Master, and Save. This publishes your code template to a live map on a public website that you control.

5) Scroll down to GitHub Pages section again, to select and copy the link to your published web site, which will follow this format:
```
https://USERNAME.github.io/REPOSITORY
```

6) Scroll up to the top, and click on your repo name to go back to its main page.

7) At the top level of your repo main page, click on README.md, and click the pencil icon to edit this file, written in easy-to-read Markdown code.

8) Delete the existing link to the live site, and paste in the link to your site. Scroll down and Commit to save your edits.

9) On your repo main page, right-click on the link to your published site to open in a new tab. **Be patient** during busy periods, when your website may take up to 1 minute to appear the first time.

#### C) Modify the chart title, subtitle, and axis labels
10) Go back to your browser tab for your code repo. Click on the index.html file (which contains the chart code), and click the pencil icon to edit it.

11) Explore the chart code, which contains HTML, CSS, and JavaScript. Look for code comments that begin with "EDIT" for sections that you can easily change, such as title, subtitle, x-axis and y-axis labels, and tooltip data labels. Scroll down to Commit your changes.

12) Go to your live website browser tab and refresh the page to view your edits. **Be patient** during busy periods, when some edits may take up to 1 minute to appear.

#### D) Upload new data points from a .CSV spreadsheet

13) Go to your GitHub code repository tab and click to view the file named: data-scatter.csv

14) GitHub automatically opens CSV files. Although it's possible to edit the file inside GitHub, let's upload a larger data file with the same name. Click this link and Save to download to your computer: [data-scatter in CSV format](https://www.datavizforall.org/github/fork-highcharts/data-scatter.csv).

15) In your GitHub code repo, click Upload Files, and drag the new data-scatter.csv into the folder, and Commit changes to replace the existing file with the same name.

16) In your GitHub repo, click the new data-scatter.csv file to inspect the changes. Then go to your live website tab and refresh to see the updated scatter chart. ** Be patient** during busy periods, when changes make take up to 1 minute to appear.

## Learn more
- To solve problems, see the [Fix Common GitHub and Code Errors](../fix) chapter in this book.
- See more [Highcharts Templates](../highcharts) in this book
- Highcharts Demos http://highcharts.com/demo and Highcharts Docs http://www.highcharts.com/docs
- GitHub Pages features and tutorial, https://pages.github.com

{% footer %}
{% endfooter %}
