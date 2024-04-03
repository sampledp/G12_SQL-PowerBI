# GOOGLE SHEET THEORY

## Section One - Spreadsheet Basics, Variables, and Shortcuts!

### Basic Operations:
- **Entering Data**: To enter data into a cell, simply click on the cell and start typing.
- **Editing Data**: Double-click on a cell to edit its contents directly.
- **Formatting Cells**: Select the cells that want to format, then use the formatting options in the toolbar to change text formatting, number formatting, or cell alignment.

### Working with Variables:
- **Defining Variables**: Can define variables using the `=` sign followed by the variable name and its value. For example: `sales_tax_rate = 0.08`.
- **Using Variables in Formulas**: Once defined, We can use variables in formulas. For example, if a variable named `sales_tax_rate`, we can use it in a formula like `=B2 * sales_tax_rate` to calculate sales tax.

### Useful Keyboard Shortcuts:
- **Ctrl+C**: Copy selected cells.
- **Ctrl+V** : Paste copied cells.
- **Ctrl+Z**: Undo last action.
- **Ctrl+Shift+Arrow keys**: Select cells quickly.
- **Ctrl+Enter**: Fill selected cells with data.

## Section Two - Introduction to Your First Functions!

### Basic Functions:
- **SUM**: Adds up a range of cells. Example: `=SUM(A1:A10)`.
- **AVERAGE**: Calculates the average of a range of cells. Example: `=AVERAGE(B1:B5)`.
- **MAX**: Returns the highest value in a range of cells. Example: `=MAX(C1:C10)`.
- **MIN**: Returns the lowest value in a range of cells. Example: `=MIN(D1:D10)`.
- **COUNT**: Counts the number of cells in a range that contain numbers. Example: `=COUNT(E1:E10)`.

### Applying Functions Effectively:
- **Syntax and Arguments**: Each function has its own syntax and arguments. 
- **Nested Functions**: We can nest functions within each other to perform more complex calculations. Example: `=IF(SUM(A1:A10) > 100, "High", "Low")`.

## Section Three - Introduction to Conditional Functions

### IF Statements:
- **Syntax**: The syntax for an IF statement is `=IF(condition, value_if_true, value_if_false)`.
- **Example**: `=IF(B2 > 100, "High", "Low")` will return "High" if the value in cell B2 is greater than 100, otherwise it will return "Low".

### Other Logical Functions:
- **AND**: Returns TRUE if all conditions are true. Example: `=AND(B2 > 100, C2 < 50)`.
- **OR**: Returns TRUE if any of the conditions are true. Example: `=OR(B2 > 100, C2 < 50)`.
- **NOT**: Returns TRUE if the condition is false, and vice versa. Example: `=NOT(B2 > 100)`.

## Section Four - Sorting, Filtering & Pivot Tables Crash Course

### Sorting Data:
- **Alphabetical Sorting**: Select the range we want to sort, then go to Data > Sort range.
- **Numerical Sorting**: Same as alphabetical sorting but ensure the data is in number format.
- **Custom Sorting**: Use the custom sort option to sort by multiple columns.

### Filtering Data:
- **Basic Filtering**: Go to Data > Create a filter to enable filtering for the selected range.
- **Filter Views**: Create different filter views to quickly switch between different filters.

### Pivot Tables:
- **Creating a Pivot Table**: Select the data range, then go to Data > Pivot table.
- **Adding Rows and Columns**: Drag fields into the rows or columns section to organize your data.
- **Calculating Values**: Use the values section to perform calculations like sum, average, count, etc.

## Section Five - Lookups

### VLOOKUP Function:
- **Syntax**: `=VLOOKUP(search_key, range, index, [is_sorted])`.
- **Example**: `=VLOOKUP(A2, B:C, 2, FALSE)` will search for the value in cell A2 in the first column of the range B:C and return the value from the second column.

### HLOOKUP Function:
- **Syntax**: Similar to VLOOKUP but for horizontal lookup.
- **Example**: `=HLOOKUP(A2, B1:D2, 2, FALSE)` will search for the value in cell A2 in the first row of the range B1:D2 and return the value from the second row.

## Section Six - GOOGLE Functions

### Advanced Functions:
- **GOOGLEFINANCE**: Get stock quotes, historical data, and currency conversion rates.
- **GOOGLETRANSLATE**: Translate text into different languages.
- **GOOGLEMAPS**: Embed Google Maps into our spreadsheet.

### Unique Features:
- **Collaboration Tools**: Real-time collaboration with multiple users.
- **Add-ons**: Extend the functionality of Google Sheets with add-ons like Google Analytics, Mail Merge, etc.

## Section Seven - Import Range Data create an Excel format

### Importing Data:
- **From CSV**: Go to File > Import > Upload, then select the CSV file.
- **From Excel**: Go to File > Import > Upload, then select the Excel file.
- **From Web Queries**: Use the IMPORTHTML, IMPORTXML, IMPORTDATA functions to import data from websites.

### Formatting Data for Excel:
- **Number Formatting**: Ensure numbers are formatted correctly for Excel compatibility.
- **Date Formatting**: Excel recognizes dates in various formats, but it's best to use the standard date format (e.g., yyyy-mm-dd).
- **Text Formatting**: Use plain text format to avoid issues with special characters or formatting.

### Exporting Data:
- **To Excel**: Go to File > Download > Microsoft Excel (.xlsx) to export the spreadsheet in Excel format.
- **Checking Compatibility**: Open the exported Excel file to ensure formatting and data integrity.
