# About This GitBook

This free open-access book is created with [GitBook](http://gitbook.com) an open-source publishing tool that creates multiple editions (Web, PDF, EPUB, Mobi/Kindle), using GitHub shareable repositories and the easy-to-read Markdown syntax. See GitBook Documentation (https://help.gitbook.com).

The contents of the book are freely accessible on this GitHub code repository: https://github.com/jackdougherty/datavizbook

Since this open-access book is shared under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0), anyone may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.

##Submit additional chapters to the book
- Recommended: [Contact the lead author](introduction/contributors.md) with a summary of your proposed chapter.
- On the [book GitHub repository](https://github.com/JackDougherty/datavizbook), fork a copy, and create your proposed chapter.
- Follow the existing folder/file structure - see below
- Compose the chapter in GitHub-flavored Markdown - see below
- See more details below about embedding video, iframes, etc.

## Folder/file structure for this GitBook:
- Part folder (example: map)
- Chapter subfolder (example: map/point-gft)
- Chapter text (example: map/point-gft/README.md)
- Chapter images (example: map/point-gft/visual.png)

## Table of Contents
View the SUMMARY.md file for this GitBook at: https://github.com/JackDougherty/datavizbook/blob/master/SUMMARY.md

## Compose in Markdown for GitHub/GitBook
Markdown is an easy-to-read syntax that is simpler than HMTL and growing in popularity across many digital platforms. GitBook follows most of GitHub Flavored Markdown syntax: https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/

See also GitBook Markdown guide: https://help.gitbook.com/format/markdown.html

## GitBook Plugins
Plugins extend the features of basic GitBook, and can be configured in the book.json file. View the entire repository of GitBook plugins: https://plugins.gitbook.com/

View the specific plugins and configurations for this book at: https://github.com/JackDougherty/datavizbook/blob/master/book.json

## Embed YouTube Video with GitBook Plugin
Since the youtube plugin is installed in this Gitbook, embed videos in the text like this:

```



## HTML elements supported by GitBook Markdown
- Insert HTML comments for notes that are not visible to GitBook readers (but are visible on the GitHub public repo)

```html
     <!-- TO DO: Revise this page -->
```
- Insert HTML iframe for interactive elements (which are visible on GitBook web edition, but not in ebook editions; perhaps in future)

```html
<iframe src="https://assets-cdn.github.com/images/modules/contact/heartocat.png">
```

## Markdown code-fencing to display non-executed code:
To display non-executed code within Markdown, insert three backticks (`) followed by the language (typically html or javascript), the code, and three closing backticks. Example:

```
```html
<iframe src="https://assets-cdn.github.com/images/modules/contact/heartocat.png">
```                         (end of example)
```

## My GitBook Workflow

- The public book is generated from the MASTER branch of this online repo: https://github.com/JackDougherty/datavizbook


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

####Avoid GitBook Editor App
At present, I avoid using the GitBook Editor App since this tool supports only one-way import, and does not play nicely with edits made using the other methods above. Maybe this will change in the future.


<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a>

[Data Visualization for All](http://datavizbook.org)
by [Jack Dougherty and contributors](introduction/contributors.md)
is published under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0).
You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.
