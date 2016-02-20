# Structure, Plugins, and Syntax

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
---
[Improve this book:](gitbook/improve.md) select text to insert comment, or suggest edits.

[Data Visualization for All](http://datavizbook.org)
copyrighted by [Jack Dougherty and contributors](introduction/who.md)
is distributed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0).
You may freely share and modify this content for non-commercial purposes, with a source credit to http://DataVizBook.org.

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a>
