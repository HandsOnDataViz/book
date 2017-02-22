# Embed a Data Visualization iframe in GitHub Pages
*by [Jack Dougherty](../introduction/who.md), last updated February 22, 2017*

Question: After you create an interactive chart or map, how do you embed the live version in a website that you control?

Here's the full three-step answer that combines lessons from the [Embed on the Web chapter introduction](../embed) and the two previous tutorials:

1) First, create a web page that supports iFrame embed codes. If you don't know what that means or don't yet have a personal website, go back to the previous tutorial, [Create a Simple Web Page with GitHub Pages](../github-pages), or see the video and step-by-step instructions below.

2) Second, copy the iframe code from your data visualization. Go back to the previous tutorial, [Copy an iframe code from a Google Sheets interactive chart](../iframe-google-sheets), or see the video and step-by-step instructions below.

3) Third, embed (or paste) the iframe code into your website. The video and instructions below show how to paste an iframe from a Google Sheets interactive chart into a simple web page with GitHub Pages.

## Try it

The goal is to embed the iframe code from a Google Sheets interactive chart, which resides on a Google web server, into your GitHub Pages web site. The result will be similar to the one below:

<iframe width="644" height="398" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/1YgBWYm9nTGlCuyqSwU3SDb7xk-SMSPgjfYq5iLqL0nQ/pubchart?oid=200651442&amp;format=interactive"></iframe>

## Video tutorial and step-by-step instructions

{%youtube%}enjhlnqaXOE{%endyoutube%}

1) Sign up for free GitHub account, then sign in, at http://github.com.
2) Create a new repository (also called a "project" or similar to a "folder").
3) Name your repository (or "repo"), and select Initialize with a README file. Optional steps: add a description and select a license.
4) Scroll down and click the green button to Create your repo, which will appear in a new browser tab, with this URL format:
```
https://github.com/YOUR-USERNAME/YOUR-REPO-NAME
```
5) In your GitHub repo, click on Settings, scroll down to GitHub Pages, select Master branch as your source, then Save. This publishes the code from your repo to the public web.
6) When the Settings page refreshes, scroll back down to GitHub Pages to see the new link to your published website, which will appear in this format:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME
```
7) Right-click and Copy this link to your published web site.
8) At the top of the page, click on the repo name to return to the main level.
9) Click the README.md file to open it in your browser, and click the pencil symbol to edit it.
10) Inside your README.md file, paste the link to your published web site, and type any text you wish to appear. The .md extension refers to Markdown, an easy-to-read computer language that GitHub Pages can process.
11) Go to a data visualization you have created, such as a Google Sheets chart, select Publish > Embed, and copy the iframe code. This line of HTML code displays the interactive visualization website inside your personal website.  
12) Scroll down and click Commit to save your edits.
13) When your GitHub repo page refreshes, click on the new link to go to your published web site.
**BE PATIENT!** Your new site may not appear instantly. Refresh the browser every 10 seconds. You may need to wait up to 1 minute for a new site to appear the first time, but later changes will be much faster.

Important:
- A published README.md file will display an HTML iframe code, unless you add other HTML files (such as index.html) to your repository.

Remember that GitHub Pages is designed to create simple web pages and sites. See other web publishing tools mentioned in this chapter to create more sophisticated web sites.

{% footer %}
{% endfooter %}
