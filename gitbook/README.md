# About This GitBook

This free open-access book is created with [GitBook](http://gitbook.com) an open-source publishing tool that creates multiple editions (Web, PDF, EPUB, Mobi/Kindle), using GitHub shareable repositories and the easy-to-read Markdown syntax. See GitBook Documentation (https://help.gitbook.com).

The contents of the book are freely accessible on this GitHub code repository: https://github.com/jackdougherty/datavizbook

Since this open-access book is shared under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0), anyone may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.

## Improve the book with comments, revisions, additions
To share a public comment on any paragraph inside this book, select the text and click the plus symbol (+) in the margin. Constructive criticism is welcome, but inappropriate comments will be removed. <!-- TO DO: insert commenting GIF -->

To suggest revisions for the book, click the "Edit in GitHub" link at the top of any page, which opens the relevant page in the development branch (dev) on the GitHub repository. You will need a free GitHub account to proceed further. Click the editing button (looks like a pencil), enter your suggested revisions, and commit the change (similar to save). <!--TO DO: Test this with Veronica's account -->

To submit an additional chapter for potential inclusion in the book, follow the Markdown format, the existing file/image/folder structure (explanation to come) and submit the change to the dev branch of the repository. Email any questions to the lead author: jack.dougherty@trincoll.edu.

## GitBook structure for files/folders/images
To come: explain and illustrate how my system works. . .

## GitBook Plugins
View the GitBook repository of plugins to extend features at: https://plugins.gitbook.com/

To view the plugins for this book on its GitHub repository:  https://github.com/JackDougherty/datavizbook/blog/dev/book.json

## Writing with Markdown for GitHub/GitBook
Markdown is an easy-to-read syntax that is simpler than HMTL, and becoming popular across a number of digital platforms. GitBook follows most of GitHub Flavored Markdown syntax: https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/

Also see the GitBook Markdown guide (https://help.gitbook.com/format/markdown.html) for some specific differences: TO COME: LIST; but check if all are supported in book exports

GitHub Markdown also supports HTML syntax for specific items, such as:

Commented-out code that is not viewed by readers:
```html
     <!-- TO DO: Revise this page -->
```

Code-fencing to display non-executed code:
TO DO: Describe and illustrate three backticks (`), followed by the language (typically html, javascript), and closing backticks.

Embed iframe:
TO DO: Explain how to do in HTML in markdown

Embed YouTube video for multiple book formats:
Since the GitBook YouTube plugin is installed in this book. . . TO DO: show steps

## My GitBook Workflow (rough notes)

- The public book is generated from the MASTER branch of this online repo: https://github.com/JackDougherty/datavizbook

- Make all edits to a duplicate DEV branch, then merge into the master branch
- Keep a current duplicate DEV branch available and encourage others to submit pull requests to that branch, not master

- To compose/edit GitBook, by owner, using BROWSER Editor:
  - check online repo to make sure that dev branch is current with master branch (if not, pull request)
  - use online GitBook browser editor https://www.gitbook.com/book/jackdougherty/datavizbook/details
  - set online browser editor to edit the dev branch, NOT the master branch
  - when done, merge branches (which means merge dev into master branch)

- For editing or major file/folder restructuring by owner with Atom Editor (no preview):
  - check online repo to make sure that dev branch is current with master branch (if not, pull request)
     use GitHub Desktop to sync repo to my local computer, where dev branch is default view
     use Atom editor to edit/upload/restructure files (no GitBook preview available)
     use GitHub Desktop to commit changes to online repo dev branch, send pull request to master branch, and confirm it online
