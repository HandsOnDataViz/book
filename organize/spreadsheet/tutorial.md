# Prepare Data with Spreadsheet Formats and Formulas

Prepare your data in a spreadsheet (or a database) to make it easier to visualize. If your data does not already exist in a spreadsheet (or table format),

Some people prefer to pay for the Microsoft Excel spreadsheet application due to its familiarity or advanced features. But everything in this tutorial can be achieved with other spreadsheet applications such as LibreOffice (free open-source, donation requested) or Google Sheets (requires a free Google Drive account). All steps below are nearly the same across these common spreadsheet applications.

Across the top row, insert short meaningful headers for each column. Avoid special characters that may not be recognized properly by other applications. Make the data in the column consistent within itself.

![](SpreadsheetBetterColumnHeaders.png)

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

## Write calculation formulas

In most spreadsheets, begin writing a simple formula with an equal sign, and refer to specific cells and functions, such as:

- = A2 + B2 + C2
- = Sum(A2:C2)
- = Average(A2:C2)

![](SpreadsheetFormula640w.gif)

## Combine address terms to geocode in Google Maps

When preparing address data for a map, some geocoding tools prefer to separate columns (address, city, state, zip) while other tools (such as Google Maps) needs these terms combined into one location column.

To combine (or concatenate) terms, write a simple formula using ampersands as connectors, and quotation marks around any spaces. No commas are necessary. For example, if the spreadsheet appears as follows:

INSERT TABLE with A, B, C, D as Address, City, State, Zip

In Column E, create a new column header named *Location* and insert this formula:



## Copy and Paste or Drag formulas to calculate automatically

The magic of spreadsheets is automate calculations across all rows or columns. In most cases, you can copy and paste a formula into new cells. Sometimes you can click-and-drag the lower-right corner of a formula cell (which may appear as a cross-hair) to automate calculations.

ADD GIF drag formula calculations

## Copy and Paste > Special > Values to replace formulas with data

After inserting calculations in a spreadsheet, sometimes dynamic formulas must be replaced with static data before the results can be visualized. One solution is to select and copy a column (or the entire sheet), then paste > special > values to replace the formula with numerical results.

ADD GIF paste special values

Remember that if you need to check or run the calculations again at a later point, click (or right-click) the tab to save a copy to the spreadsheet as a backup.
