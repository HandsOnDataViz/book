# Host with GitHub Pages and embed an iFrame
*by [Jack Dougherty](../introduction/who.md), last updated February 17, 2017*

Question: After you create an interactive chart or map, how do you embed the live version in a website that you control?

Answer: If you don't already have your own website, then create a simple web page with GitHub (http://github.com), and copy-and-paste the iframe code from your data visualization to make it fully interactive on the web. GitHub includes a free and friendly web interface, and also free web hosting through its built-in GitHub Pages.

## Tool Review
- Pros:
  - Free and easy-to-learn tool to edit and host simple pages on the public web.
  - All steps below are completed entirely in your web browser.
- Cons:
  - All work on GitHub is public by default. Private repositories require payment.
  - New users sometimes confuse links for code repositories versus the hosted sites.

## Video tutorial and step-by-step instructions

{%youtube%}enjhlnqaXOE{%endyoutube%}

- Sign up for free GitHub account, then sign in, at http://github.com.
- Create a new repository (similar to a new "project" or "folder").
- Name your repository (or "repo"), and select Initialize with a README file. Optional: select a license. Click the green button to Create your repo, which will appear in a new browser tab, with this URL format:
```
https://github.com/YOUR-USERNAME/YOUR-REPO-NAME
```
- In your GitHub repo, click on Settings, scroll down to GitHub Pages, select Master branch as your source, then Save. This hosts the code from your repo on the public web.
- When the Settings page refreshes, scroll back down to GitHub Pages to see the new link to your hosted website, which will appear in this format:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME
```
- Right-click and Copy this link to your new hosted site.
- At the top of the page, click on the repo name to return to the main level.
- Click the README.md file to open it in your browser, and click the pencil symbol to edit it.
- Type any text into your README.md file, which is written in easy-to-read Markdown code.
- Paste the link to your new hosted site in your README.md file.
- Go to a data visualization you have created, such as a Google Sheets chart, select Publish > Embed, and copy of the iframe code. These are instructions to display the interactive visualization inside your web page, written in HTML code, which GitHub Markdown can process.
- Scroll down and click Commit to save your edits.
- When your GitHub repo page refreshes, click on the new link to go to your hosted site.
- BE PATIENT! Your new site may not appear instantly. Refresh the browser every 10 seconds. You may need to wait up to 1 minute for a new site to appear the first time, but later changes will be faster.

{% footer %}
{% endfooter %}
