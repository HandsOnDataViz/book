#### Copy and Paste > Special > Values to replace formulas with data {-}


I removed this section from spreadsheet skills because I believe it's a leftover method I used when copying and pasting data into GIS, which is now done by exporting CSV to keep data and remove formulas.


After inserting calculations in a spreadsheet, sometimes dynamic formulas must be replaced with static data before the results can be visualized. One solution is to select and copy a column (or the entire sheet), then paste > special > values to replace the formula with numerical results.

```{r spreadsheet-paste-special}
if(knitr::is_html_output(excludes="markdown")) knitr::include_url("images/03-spreadsheet/SpreadsheetPasteSpecialValues640w.gif") else knitr::include_graphics("images/placeholder.jpg")
```

Remember that if you need to check or run the calculations again at a later point, click (or right-click) the tab to save a copy to the spreadsheet as a backup.
