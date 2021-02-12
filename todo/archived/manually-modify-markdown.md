## Manually Modify Markdown Output {- #modify-markdown}
The O'Reilly production team has agreed to accept our full-book Markdown file into their workflow, which is easier for them to work with than the full-book MSWord file. Note that our Bookdown index.Rmd file includes code to generate a full-book Markdown:

```
bookdown::markdown_document2:
  default
```

See this not-fully-documented Bookdown solution about generating Markdown output: https://stackoverflow.com/questions/58164239/compile-bookdown-to-markdown. We experimented to see if "strict" Markdown would produce cleaner output, following this RMarkdown guide https://bookdown.org/yihui/rmarkdown/markdown-document.html, but saw no difference when compared to the default settings.

We need to do a bit of manual cleanup before ORM production team can convert the full-book Markdown file into [AsciiDoc format for their Atlas platform](https://docs.atlas.oreilly.com/writing_in_asciidoc.html), unless we find a way to automate these steps. See workaround notes in the Images and Tables sections above. Remember to avoid mischievous characters in R code-chunk image captions (such as `<` or `>` or `"`) that will throw HTML errors into the Markdown output images.

- Build the book with Bookdown, including one full-length Markdown file (docs folder, suffix .md)
- Manually rename it as HandsOnDataViz-modified.md
- Manually paste in these Markdown tables to replace HTML tables (unless ORM can handle this part)
  - from index.Rmd, table of authors
  - from 07-chart.Rmd, Table 1: Chart types covered in this book
- Manually delete any remaining `<iframe...` elements (unless they are non-executable code snippets)
- Manually mark up "Variable List:" for production team in two places in Chapter 5 (and chapter 2?)
- Save and push the modified Markdown file up to GitHub repo

TODO: Check to see if triple back tics render correctly in the Markdown full-book output.

NOTE: Tried to insert unicode character `&emsp;` for four-whitespace characters appended to level 3 subheads in chap 5, but PDF engine Latex could not process. Then tried to switch to `latex_engine: xelatex` to deal with unicode characters, but received different error. Replaced unicode symbol with hyphen-space, which is good enough.

Note: Previously, we tried to use [Pandoc](http://pandoc.org) to convert the modified.md file to asciidoc, but encountered many errors.

OLD Pandoc conversion steps (for reference only):

- Use command line to navigate to subfolder with `pwd` and `cd`.
- Convert with: `pandoc handsondataviz-modified.md --from markdown --to asciidoc --standalone --output handsondataviz-modified.asciidoc`
