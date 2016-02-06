# Calculate Formulas in Spreadsheets

Simple formulas can save you lots of time. The big advantage of spreadsheet tools is the ability to insert simple formulas to calculate numbers, or combine columns of text, for entire rows and columns.

## Write a simple formula

In most spreadsheets, begin writing a simple formula with an equal sign, and refer to specific cells and functions, such as:

- = A2 + B2 + C2
- = Sum(A2:C2)
- = Average(A2:C2)

## Copy or Drag formulas

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
