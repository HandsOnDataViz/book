# My GitBook Workflow

## My Settings
- TO DO: explain GitBook-GitHub link; custom domain

## Simple edits with GitBook BROWSER Editor:
The GitHub Browser editor provides WYSIWYG preview, with works with most edits.
- check book repo for any pull requests from contributors: https://github.com/JackDougherty/datavizbook
- start up online GitBook browser editor https://www.gitbook.com/book/jackdougherty/datavizbook/details
- in online browser editor, create a new branch (dev) for edits
- when done, merge branches (push dev branch into master branch)
- delete the dev branch to avoid confusion

## Structural changes with GitHub Desktop and Atom Editor
When making major changes to the book, especially folder/file structure, copy a branch to a local computer with GitHub Desktop, and modify with Atom Editor (or your preferred text editor).
- check book repo for any pull requests from contributors: https://github.com/JackDougherty/datavizbook
- create dev branch
- use GitHub Desktop to sync repo to my local computer, where dev branch is default view
- use Atom editor to edit/upload/restructure files
- use GitHub Desktop to commit changes to online repo dev branch, send pull request to master branch, and confirm it online

##Why not the GitBook Editor Desktop App?
At present, I avoid using the GitBook Editor App since this tool supports only one-way import, and in my persona experience, does not play nicely with edits made using the other methods above. Maybe this will change in the future.


<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a>

[Data Visualization for All](http://datavizbook.org)
by [Jack Dougherty and contributors](introduction/contributors.md)
is published under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0).
You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.
