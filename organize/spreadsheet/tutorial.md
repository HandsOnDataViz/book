# Formatting Spreadsheets

Organize your data into a spreadsheet table with columns and rows (or for more complex projects, a database tool). Three common spreadsheet tools are:

- Microsoft Excel: many people are familiar with this tool, which also has advanced features, but it is not free
- [LibreOffice](http://www.libreoffice.org/): a powerful open-source alternative to Microsoft Office, which anyone can [freely download](http://www.libreoffice.org/download) for Mac/Windows/Linux, with donation requested
- [Google Sheets](https://www.google.com/sheets/about/): free spreadsheet tool on the Google Drive platform, works in modern browsers, requires free account

All steps illustrated below are nearly the same across these three spreadsheet tools.


## Make clean column headers and sheets

Across the top row, insert short meaningful headers for each column. Avoid special characters that may not be recognized properly by other applications. Make the data in the column consistent within itself.

![](SpreadsheetBetterColumnHeaders.png)

## Save source data in separate sheet

If you have doubts when cleaning up columns, click (or right-click) on the spreadsheet tab to copy the sheet to another tab as a backup, to avoid destroying any data.

![](SpreadsheetCopySheet640w.gif)

Add a *source* tab, after the data, with notes to remind you and others about its origins and when it was last updated.

![](SpreadsheetSourceTab.png)

## Format data columns as needed

If your data needs to be formatted, select a spreadsheet column by clicking at the top. Or select the entire spreadsheet by clicking the top-left corner icon. Right-click your selection to reformat data (or use menu commands). For example, reformat the data to change the number of decimal points displayed. Or reformat a zip code from a number (because 06106 will not display the first zero) into a text or zip code field.

![](SpreadsheetFormatZipAsText.png)

## Sort data rows

To sort data rows by a column, select the entire spreadsheet (top-left corner icon), then right-click or look for the sort menu. Be sure to select the entire sheet to avoid accidentally sorting one column without the adjacent ones.

![](SpreadsheetSort640w.gif]

**TO DO: Fix sort graphic above; add filter

## Write calculation formulas

In most spreadsheets, begin writing a simple formula with an equal sign, and refer to specific cells and functions, such as:

- = A2 + B2 + C2
- = Sum(A2:C2)
- = Average(A2:C2)

## Copy and Paste or Drag formulas to calculate automatically

Spreadsheets can magically automate calculations across rows or columns. In most cases, you can copy and paste a formula into new cells. Sometimes you can click-and-drag the lower-right corner of a formula cell (which may appear as a cross-hair) to automate calculations.

![](SpreadsheetFormula640w.gif)

## Combine address terms to geocode in Google Maps

When preparing address data for a map, some geocoding tools prefer to separate columns (address, city, state, zip) while other tools (such as Google Maps) needs these terms combined into one location column.

To combine (or concatenate) terms, write a simple formula using ampersands (&) as connectors, and quotation marks around blank spaces as separators. No commas are necessary. For example, if a spreadsheet contained four columns, *Address, City, State, Zip* (A-D), then in column E insert a new header named *Location* and a formula in this format:

- =A2 &" " & B2 &" " &C2 &" " &D2

![](SpreadsheetCombineTerms.png)

## Copy and Paste > Special > Values to replace formulas with data

After inserting calculations in a spreadsheet, sometimes dynamic formulas must be replaced with static data before the results can be visualized. One solution is to select and copy a column (or the entire sheet), then paste > special > values to replace the formula with numerical results.

![](SpreadsheetPasteSpecialValues640w.gif)

Remember that if you need to check or run the calculations again at a later point, click (or right-click) the tab to save a copy to the spreadsheet as a backup.
