# About This GitBook

This free open-access book is created with [GitBook](http://gitbook.com) an open-source publishing tool that creates multiple editions (Web, PDF, EPUB, Mobi/Kindle), using GitHub shareable repositories and the easy-to-read Markdown syntax. See GitBook Documentation (https://help.gitbook.com).

The contents of the book are freely accessible on this GitHub code repository: https://github.com/jackdougherty/datavizbook

Since this open-access book is shared under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0), anyone may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.

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

```
```javascript
here's some javascript
```                         (example)
```

Embed iframe:
TO DO: Explain how to do in HTML in markdown

Embed YouTube video for multiple book formats:
Since the GitBook YouTube plugin is installed in this book. . . TO DO: show steps

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
