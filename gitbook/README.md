# About This GitBook

***Data Visualization for All*** is created with [GitBook](http://gitbook.com), an open-source publishing platform that creates multiple editions (Web, PDF, ePUB, Mobi/Kindle), written in the easy-to-read Markdown format. See GitBook documentation (which is still a work-in-progress) in two places:
- https://github.com/GitbookIO/gitbook#gitbook
- https://help.gitbook.com

This book is hosted on the free GitBook.com platform. Updates are automatically generated when the author makes changes to the master branch of its linked GitHub repository: https://github.com/JackDougherty/datavizbook

Since this open-access book is shared under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0), anyone may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.

##Comment on any paragraph
- Select text and click the plus symbol (+) in margin.
- Requires a free GitHub or GitBook account.
- View other comments in margin, or all in [Discussions](https://www.gitbook.com/book/jackdougherty/datavizbook/discussions).
- Constructive criticism and suggestions are welcome.

![](GitBook-comments-2016-02.gif)

##Suggest revisions on any page
- Click "Edit in GitHub" at top of any page, which opens new tab.
    ![](GitBook-edit-on-github.png)
- To view the code behind the page, click Raw button.
- To suggest revisions, click Editor button (the pencil symbol), which requires a [free GitHub account](http://github.com).
    ![](GitHub-edit-file.png)
- After entering revisions, scroll down to click Propose File Change.
- On next screen, click Create Pull Request to send changes to the book master branch.
- On next screen, click Create Pull Request again to confirm.
- The book owner will review your suggested revisions, and you will receive automatic notification on any changes.

##Submit additional chapters to the book
- Recommended: [Contact the lead author](introduction/contributors.md) with a summary of your proposed chapter.
- On the [book GitHub repository](https://github.com/JackDougherty/datavizbook), fork a copy to your own GitHub account (requires free signup).
- Create your proposed chapter following the book's existing folder/file structure, in GitHub/GitBook Markdown format, as explained below.
- 

## Folder/file structure for this GitBook:
- Part folder (example: map)
- Chapter subfolder (example: map/point-gft)
- Chapter text (example: map/point-gft/README.md)
- Chapter images (example: map/point-gft/visual.png)

## Table of Contents
GitBook requires a SUMMARY.md file, which organizes the table of contents. View the SUMMARY.md file for this GitBook at: https://github.com/JackDougherty/datavizbook/blob/master/SUMMARY.md

## Compose in Markdown for GitHub/GitBook
Markdown is an easy-to-read syntax that is simpler than HMTL and growing in popularity across many digital platforms. GitBook follows most of GitHub Flavored Markdown syntax: https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/

See also GitBook Markdown guide: https://help.gitbook.com/format/markdown.html

Inside each chapter folder, the main text is stored in the README.md file, to simplify the GitBook web addresses. Example:
- A chapter in the GitHub repository: https://github.com/JackDougherty/datavizbook/blob/master/map/point-gft/README.md
- The same chapter on GitBook (which converts README.md to index.html): http://www.datavizbook.org/content/map/point-gft/index.html
- Abbreviated web address to same chapter (since "index.html" is not required): 
- http://www.datavizbook.org/content/map/point-gft


### Embed links in GitBook Markdown
Insert brackets around the words to be underlined, followed by parentheses for the embedded link, like this:

```
Regular text [with underlined hotlink](http://anywhere.com)
```
### Embed images in GitBook Markdown
Upload images into the chapter folder. In the 


## GitBook Plugins
Plugins extend the features of basic GitBook, and are configured in the book.json file. View the entire repository of GitBook plugins: https://plugins.gitbook.com/

View the plugins and configurations used in this book at: https://github.com/JackDougherty/datavizbook/blob/master/book.json

### Embed YouTube Video with GitBook Plugin
Since the [youtube plugin](https://plugins.gitbook.com/plugin/youtube) is installed in this Gitbook, embed videos in the text this way:

```
{% youtube %}https://youtu.be/b73LBXYrbng{% endyoutube %}
```
The YouTube video will appear as an embedded iframe in the online web version of the GitBook, and as a link in the ebook versions. 


## Insert HTML comments in GitBook Markdown
- Insert HTML comments for notes that are not visible to GitBook readers (but are visible on the GitHub public repo)

```html
     <!-- TO DO: Revise this page -->
```
- Insert HTML iframe for interactive elements (which are visible on GitBook web edition, but not in ebook editions; perhaps in future)

```html
<iframe src="https://assets-cdn.github.com/images/modules/contact/heartocat.png">
```

## Use Code-Fencing in Markdown
To display non-executed code within Markdown for GitHub/GitBook, follow this code-fencing format:
- insert three backticks (`) followed by the language (typically html or javascript)
- insert the non-executed code to display
- insert three closing backticks. 

Example:

```
```html
<iframe src="https://assets-cdn.github.com/images/modules/contact/heartocat.png">
```                         (end of example)
```

## My GitBook Workflow

#### My Settings
- TO DO: explain GitBook-GitHub link; custom domain

####For simple edits by owner to GitBook using BROWSER Editor (with preview screen):
- check book repo for any pull requests from contributors: https://github.com/JackDougherty/datavizbook
- start up online GitBook browser editor https://www.gitbook.com/book/jackdougherty/datavizbook/details
- in online browser editor, create a new branch (dev) for edits
- when done, merge branches (push dev branch into master branch)
- delete the dev branch to avoid confusion 

####For major revisions and structural file/folder changes by owner with Atom Editor (no preview):
- check book repo for any pull requests from contributors: https://github.com/JackDougherty/datavizbook
- create dev branch
- use GitHub Desktop to sync repo to my local computer, where dev branch is default view
- use Atom editor to edit/upload/restructure files
- use GitHub Desktop to commit changes to online repo dev branch, send pull request to master branch, and confirm it online

####Why not the GitBook Editor Desktop App?
At present, I avoid using the GitBook Editor App since this tool supports only one-way import, and in my persona experience, does not play nicely with edits made using the other methods above. Maybe this will change in the future.


<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a>

[Data Visualization for All](http://datavizbook.org)
by [Jack Dougherty and contributors](introduction/contributors.md)
is published under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0).
You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.
