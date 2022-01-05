## Concepts
- Tables
	- Deals with the data more sanely, is limited to a tabular block of data
	- Toggle via `format as table`
- Pivot Tables
	- Allow aggregation of information for quick summary stats
	- Custom Field: `PivotTable Analyze > Fields, Items & Sets > Calculated Field`
	- Slicer: Extra element to filter data with pretty buttons
	- Timeline: Nice, date related filters

## Shortkeys
- F4: Toggle between relative / absolute references I.e. $ signs
- CTRL + Shift + Arrow: Select until last value in that direction
- 

## Functions
- LEFT / RIGHT: Get a substring from that direction 
- SEARCH: Get position of search string in another string
- Lookup functions: These will **always** search the first row or column, so data firmst is crucial
  - VLOOKUP: Looks for data in rows, searches the first *column* for the provided value
  - HLOOKUP:  Looks for data in columns, searches the first *row* for the provided value
  - XLOOKUP: Newer and better alternative!
-   

## Tips
- Get rid of empty rows
  1. Select all data
  2. Add filters
  3. Select all blank (at bottom of filter)
  4. Delete rows
- identify duplicate rows
  - Use a row with unique values e.g. id 
  - Conditional Formatting > Duplicates
- Expand formula to selection: Select area of interest, press F2 to edit first cell, press CTRL + Enter to fill
- FlashFill: Can detect simple operations for you, e.g. write a combined name and it can fill the whole column with names

