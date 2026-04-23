Works with **.xls** and **.xlsx** files. You can do everything you would be able to do in Excel but in **R**!


### `loadWorkbook()`:
* loads in the Excel workbook into R, after loading it you get **workbook** object
### `getSheets():`
* returns the sheets that are in the workbook.
### `readWorksheet():`
* reads the worksheet
* (workbook, sheet, startRow, endRow, startCol, endCol, header)
### `createSheet():`
* creates a new sheet in workbook
* (workbook, name)
### `writeWorksheet():`
* adds data to a specific sheet
* (workbook, data_to_add, sheet)
### `saveWorkbook():`
* saves workbook to a file
* (workbook, file)
### `renameSheet():`
* renames a sheet in a workbook, remember to save the workbook after changing names.
* (workbook, old_sheet_name, new_sheet_name)
### `removeSheet():`
* removes sheet from workbook
* (workbook, sheet_to_remove)
