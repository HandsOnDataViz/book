# Clean Up Dirty and Disorganized Data

Sometimes we receive a spreadsheet with problem entries that need to be cleaned up before we can successfully upload it into a visualization tool.

## Split one column into two with Excel

One common problem is when multiple pieces of data appear in one column, and your goal is to split them into separate columns. If those data pieces are separated by commas (or similar punctuation), you might be able to fix this with a simple spreadsheet command: split text into columns.

To follow this example, [download this sample spreadsheet](split-coordinate-pairs.csv), and open with Excel. (**TO DO** test with other spreadsheet tools)

1. Select the data column you wish to split.

2. Select Data > Split Text to Column

3. In the wizard screen, select Delimited data and click next.

4. In step 2 of the wizard screen, check the "comma" box, since this symbol divides the data column. Click next.

5. In step 3 of the wizard screen, accept the default General format, and Finish.

The coordinate pairs column is now split into two separate columns. Relabel the headers: longitude and latitude.

**TO DO** insert GIF animation above?

## Combine separate data columns into one

Another common data cleaning problem is when you receive address data in separate columns, like this:

| Street      | City        | State      | Zip        |
| :---------- | :---------- | :--------- | :--------- |
| 100 Main St | Hartford    | CT         | 06106      |

But your data visualization tool requires you to combine all of this terms into one location column, like this:

| Location                          |
| :-------------------------------- |
| 100 Main St, Hartford, CT 06106   |

One easy solution is to write a simple spreadsheet formula to combine (or concatenate) terms, using ampersands (&) as connectors, and quotation marks around blank spaces as separators. For example, if a spreadsheet contained four columns, *Address, City, State Zip* (A-D), then in column E insert a new header named *Location* and a formula in this format:

- =A2 &" " & B2 &" " &C2 &" " &D2

![](SpreadsheetCombineTerms.png)

**TO DO**
- Confirm that Google Fusion Tables geocoder does not require commas between terms
- Clarify what happens with zip code in the example above

## Clean up Connecticut city/town names with VLOOKUP

In Connecticut, residents often write their local village, post office station, or borough name into the city field of an address. But these local names do not necessarily match up with the official list of 169 Connecticut town municipality names.

The Connecticut Mirror/TrendCT staff have openly shared a wonderful spreadsheet, ctnamecleaner, to help unify these mismatched names.

Click to view [ctnamecleaner in a public Google sheet](https://docs.google.com/spreadsheets/d/1WqZIGk2AkHXKYvd4uXy5a2nwyg529e7mMU5610Ale0g/edit#gid=0). For advanced users, see also https://github.com/trendct/ctnamecleaner

Use the VLOOKUP tool, described in this book, to match up official town names in your data.

**TO DO** illustrate the concept and steps above


## Advanced data cleaning

For more advanced data cleaning, see Alvin Chang's excellent tutorial to Open Refine in TrendCT/CT Mirror:
http://trendct.org/2015/04/24/john-jonathan-and-johnny-how-to-merge-them-in-open-refine/
