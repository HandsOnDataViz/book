# Prepare Data with Spreadsheet Formats and Formulas

Prepare your data in a spreadsheet (or a database) to make it easier to visualize. If your data does not already exist in a spreadsheet (or table format),

Some people prefer to pay for the Microsoft Excel spreadsheet application due to its familiarity or advanced features. But everything in this tutorial can be achieved with other spreadsheet applications such as LibreOffice (free open-source, donation requested) or Google Sheets (requires a free Google Drive account). All steps below are nearly the same across these common spreadsheet applications.

Across the top row, insert short meaningful headers for each column. Avoid unusual or special characters that not be recognized properly by other applications.

ADD screenshot raw vs clean header

Make the data in the column consistent within itself and the header.

ADD screenshot raw vs clean data column

If you have doubts when cleaning up columns, click (or right-click) on the spreadsheet tab to copy the sheet to another tab as a backup, to avoid destroying any data.

ADD GIF copy sheet to new tab

Add a *source* tab, after the data, with notes to remind you and others about its origins and when it was last updated.

Add screenshot of source tab

## Format data columns as needed

If your data needs to be formatted, select a spreadsheet column by clicking at the top. Or select the entire spreadsheet by clicking the top-left corner icon. Right-click your selection to reformat data (or use menu commands). For example, reformat the data to change the number of decimal points displayed. Or reformat a zip code from a number (because 06106 will not display the first zero) into a text or zip code field.

Add GIF to select column and reformat decimals

Add screenshot of zip code format?

## Sort or Filter data columns as needed

To sort a data column from its lowest to highest values, select the entire spreadsheet (top-left corner icon), then right-click or look for the sort menu. It's important to select the entire sheet to avoid accidentally sorting one column without the adjacent columns.

Add GIF sort data

The Filter command allows users to sort data, and also to display only rows with selected data.

Add GIF filter data

## Write simple formulas to calculate

In most spreadsheets, begin writing a simple calculation with an equal sign, and refer to specific cells and functions, such as:

- = A2 + B2 + C2
- = Sum(A2:C2)
- = Average(A2:C2)

Add GIF write simple average formula

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
