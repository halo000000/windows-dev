---
description: Top 116 Useful Excel Macro [VBA] Codes Examples
icon: file-xls
---

# 116 Useful Excel Macro \[VBA]

Macro codes can save you a ton of time. You can automate small as well as heavy tasks with VBA codes.

And do you know? With the help of macros, you can break all the limitations of Excel which you think Excel has.

And today, I have listed some of the **useful codes examples to help you become more productive** in your day to day work.

You can use these codes even if you haven’t used VBA before that. But here’s the first thing to know:

### What is a Macro Code? <a href="#id-0-what-is-a-macro-code" id="id-0-what-is-a-macro-code"></a>

In Excel, macro code is a programming code which is written in VBA (Visual Basic for Applications) language. The idea behind using a macro code is to automate an action which you perform manually in Excel, otherwise.

_For example, you can use a code to print only a particular range of cells just with a single click instead of selecting the range > File Tab > Print > Print Select > OK Button._

### How to use a Macro Code in Excel? <a href="#id-1-how-to-use-a-macro-code-in-excel" id="id-1-how-to-use-a-macro-code-in-excel"></a>

Before you use these codes, make sure you have your developer tab on your Excel ribbon to access VB editor. Once you activate developer tab you can use below steps to paste a VBA code into VB editor.

1. Go to your [developer tab](https://excelchamps.com/vba/add-developer-tab/) and **click on “Visual Basic”** to open the [Visual Basic Editor](https://excelchamps.com/vba/visual-basic-editor/).\
   ![click-on-visual-basic-editor-before-you-use-these-useful-macros-for-excel](https://cdn-ilacncj.nitrocdn.com/RtZAOJSIpUfqnjeuokJknkjieDmOhMZE/assets/images/optimized/rev-6f06a21/excelchamps.com/wp-content/uploads/2016/09/click-on-visual-basic-editor-before-you-use-these-useful-macros-for-excel.png)
2. On the left side in “Project Window”, right click on the name of your workbook and **insert a new module**.\
   ![add-module-to-paste-these-useful-macros-for-excel](https://cdn-ilacncj.nitrocdn.com/RtZAOJSIpUfqnjeuokJknkjieDmOhMZE/assets/images/optimized/rev-6f06a21/excelchamps.com/wp-content/uploads/2016/09/add-module-to-paste-these-useful-macros-for-excel.png)
3. Just **paste your code** into the module and close it.\
   ![use-useful-macro-codes-examples-by-pasting-them-into-vb-editor](https://cdn-ilacncj.nitrocdn.com/RtZAOJSIpUfqnjeuokJknkjieDmOhMZE/assets/images/optimized/rev-6f06a21/excelchamps.com/wp-content/uploads/2017/08/use-useful-macro-codes-examples-by-pasting-them-into-vb-editor.png)
4. Now, go to your developer tab and click on the **macro button**.\
   ![useful-macro-codes-examples-to-use-from-macro-options](https://cdn-ilacncj.nitrocdn.com/RtZAOJSIpUfqnjeuokJknkjieDmOhMZE/assets/images/optimized/rev-6f06a21/excelchamps.com/wp-content/uploads/2017/08/useful-macro-codes-examples-to-use-from-macro-options.png)
5. It will show you a window with a **list of the macros** you have in your file from where you can run a macro from that list.\
   ![useful-macro-codes-examples-list-from-macro-options](https://cdn-ilacncj.nitrocdn.com/RtZAOJSIpUfqnjeuokJknkjieDmOhMZE/assets/images/optimized/rev-6f06a21/excelchamps.com/wp-content/uploads/2017/08/useful-macro-codes-examples-list-from-macro-options.png)

**Learn VBA in 1 Hour**

### (List) Top 116 Macro Examples (CODES) for VBA Beginners <a href="#id-2-list-top-100-macro-examples-codes-for-vba-beginners" id="id-2-list-top-100-macro-examples-codes-for-vba-beginners"></a>

* This is my Ultimate VBA Library, which I update on a monthly basis with new codes. don’t forget to check the VBA Examples Sectionꜜ at the end of this list.
* VBA is one of the [Advanced Excel Skills](https://excelchamps.com/excel-skills/).
* To manage all of these codes, make sure to read about the [Personal Macro Workbook](https://excelchamps.com/vba/personal-macro-workbook/) so that you can use them in all the workbooks.
* I have tested all of these codes in different versions of Excel (2007, 2010, 2013, 2016, and 2019). If you find any errors in these codes, please share them[ with me](https://excelchamps.com/contact/).

### Download the PDF File

### Basic Codes

#### 1. Add Serial Numbers <a href="#id-4-1-add-serial-numbers" id="id-4-1-add-serial-numbers"></a>

This macro code will [automatically add serial numbers](https://excelchamps.com/blog/automatically-add-serial-numbers-in-excel/) to your Excel sheet, which can be helpful if you work with large amounts of data.

```
Sub AddSerialNumbers()
Dim i As Integer
On Error GoTo Last
i = InputBox("Enter Value", "Enter Serial Numbers")
For i = 1 To i
ActiveCell.Value = i
ActiveCell.Offset(1, 0).Activate
Next i
Last:Exit Sub
End Sub
```

To use this code, you need to select the cell from where you want to start the serial numbers and when you run this it shows you a [message box](https://excelchamps.com/vba/msgbox/) where you need to enter the highest number for the serial numbers and click OK.

And once you click OK, it simply runs a loop and add a list of serial numbers to the cells downward.

#### 2. Insert Multiple Columns <a href="#id-5-2-insert-multiple-columns" id="id-5-2-insert-multiple-columns"></a>

This code helps you to enter multiple columns in a single click.

```
Sub InsertMultipleColumns()
Dim i As Integer
Dim j As Integer
ActiveCell.EntireColumn.Select
On Error GoTo Last
i = InputBox("Enter number of columns to insert", "Insert Columns")
For j = 1 To i
Selection.Insert Shift:=xlToRight, CopyOrigin:=xlFormatFromRightorAbove
Next j
Last: Exit Sub
End Sub
```

When you run this code, it asks you the number columns you want to add and when you click OK, it adds entered number of columns after the selected cell. If you want to add columns before the selected cell, replace the xlToRight to xlToLeft in the code.

#### 3. Insert Multiple Rows <a href="#id-6-3-insert-multiple-rows" id="id-6-3-insert-multiple-rows"></a>

With this code, you can enter multiple rows in the worksheet. When you run this code, you can enter the number of rows to insert and make sure to select the cell from where you want to insert the new rows.

```
Sub InsertMultipleRows()
Dim i As Integer
Dim j As Integer
ActiveCell.EntireRow.Select
On Error GoTo Last
i = InputBox("Enter number of columns to insert", "Insert Columns")
For j = 1 To i
Selection.Insert Shift:=xlToDown, CopyOrigin:=xlFormatFromRightorAbove
Next j
Last: Exit Sub
End Sub
```

If you want to add rows before the selected cell, replace the xlToDown to xlToUp in the code.

#### 4. Auto Fit Columns <a href="#id-7-4-auto-fit-columns" id="id-7-4-auto-fit-columns"></a>

This code quickly auto fits all the columns in your worksheet.

```
Sub AutoFitColumns()
Cells.Select
Cells.EntireColumn.AutoFit
End Sub
```

When you run this code, it will select all the cells in your worksheet and instantly auto-fit all the columns.

#### 5. Auto Fit Rows <a href="#id-8-5-auto-fit-rows" id="id-8-5-auto-fit-rows"></a>

You can use this code to [auto fit](https://excelchamps.com/keyboard-shortcuts/auto-fit/) all the rows in a worksheet.

```
Sub AutoFitRows()
Cells.Select
Cells.EntireRow.AutoFit
End Sub
```

When you run this code, it will select all the cells in your worksheet and instantly auto fit all the rows.

#### 6. Remove Text Wrap <a href="#id-9-6-remove-text-wrap" id="id-9-6-remove-text-wrap"></a>

This code will help you to remove text wrap from the entire worksheet with a single click.

```
Sub RemoveTextWrap()
Range("A1").WrapText = False
End Sub
```

It will first select all the columns and then remove text wrap and auto fit all the rows and columns. There’s also a shortcut that you can use (Alt + H +‌W) for but if you add this code to [Quick Access Toolbar](https://excelchamps.com/excel-basics/quick-access-toolbar/) it’s convenient than a [keyboard shortcut](https://excelchamps.com/keyboard-shortcuts/).

#### 7. Unmerge Cells <a href="#id-10-7-unmerge-cells" id="id-10-7-unmerge-cells"></a>

This code simply uses the unmerge options which you have on the HOME‌ tab.

```
Sub UnmergeCells()
Selection.UnMerge
End Sub
```

The benefit of using this code is you can add it to the QAT and unmerge all the cell in the selection. And if you want to un-merge a specific range you can define that range in the code by replacing the word selection.

#### 8. Open Calculator <a href="#id-11-8-open-calculator" id="id-11-8-open-calculator"></a>

In Windows, there is a specific calculator and by using this macro code you can open that calculator directly from Excel.

```
Sub OpenCalculator()
Application.ActivateMicrosoftApp Index:=0
End Sub
```

As I mentioned that it’s for windows and if you run this code in the MAC version of VBA you’ll get an error.

This macro adds a date to the header when you run it. It simply uses the tag “\&D” for adding the date.

```
Sub DateInHeader()
With ActiveSheet.PageSetup
.LeftHeader = ""
.CenterHeader = "&D"
.RightHeader = ""
.LeftFooter = ""
.CenterFooter = ""
.RightFooter = ""
End With
End Sub
```

You can also change it to the footer or change the side by replacing the “” with the date tag. And if you want to add a specific date instead of the current date you can replace the “\&D” tag with that date from the code.

When you run this code, it shows an input box that asks you to enter the text which you want to add as a header, and once you enter it click OK.

```
Sub CustomHeader()
Dim myText As String
myText = InputBox("Enter your text here", "Enter Text")
With ActiveSheet.PageSetup
.LeftHeader = ""
.CenterHeader = myText
.RightHeader = ""
.LeftFooter = ""
.CenterFooter = ""
.RightFooter = ""
End With
End Sub
```

If you see this closely you have six different lines of code to choose the place for the header or footer. Let’s say if you want to add left-footer instead of center header simply replace the “myText” to that line of the code by replacing the “” from there.

### Formatting Codes

These VBA codes will help you to format cells and ranges using some specific criteria and conditions.

#### 11. Highlight Duplicates from Selection <a href="#id-15-11-highlight-duplicates-from-selection" id="id-15-11-highlight-duplicates-from-selection"></a>

This macro will check each cell of your selection and [highlight the duplicate values](https://excelchamps.com/vba/highlight-duplicate-values/).  You can also change the color from the code.

```
Sub HighlightDuplicateValues()
Dim myRange As Range
Dim myCell As Range
Set myRange = Selection
For Each myCell In myRange
If WorksheetFunction.CountIf(myRange, myCell.Value) &gt; 1 Then
myCell.Interior.ColorIndex = 36
End If
Next myCell
End Sub
```

#### 12. Highlight the Active Row and Column <a href="#id-16-12-highlight-the-active-row-and-column" id="id-16-12-highlight-the-active-row-and-column"></a>

I really love to use this macro code whenever I have to analyze a data table.

```
Private Sub Worksheet_BeforeDoubleClick(ByVal Target As Range, Cancel As Boolean)
Dim strRange As String
strRange = Target.Cells.Address & "," & _
Target.Cells.EntireColumn.Address & "," & _
Target.Cells.EntireRow.Address
Range(strRange).Select
End Sub
```

Here are the quick steps to apply this code.

1. Open VBE (ALT + F11).
2. Go to Project Explorer (Ctrl + R, If hidden).
3. Select your workbook & double click on the name of a particular worksheet in which you want to activate the macro.
4. Paste the code into it and select the “BeforeDoubleClick” from event drop down menu.
5. Close VBE and you are done.

Remember that, by applying this macro you will not able to edit the cell by double click.

#### 13. Highlight Top 10 Values <a href="#id-17-13-highlight-top-10-values" id="id-17-13-highlight-top-10-values"></a>

Just select a range and run this macro and it will highlight top 10 values with the green color.

```
Sub TopTen()
Selection.FormatConditions.AddTop10
Selection.FormatConditions(Selection.FormatConditions.Count).S
tFirstPriority
With Selection.FormatConditions(1)
.TopBottom = xlTop10Top
.Rank = 10
.Percent = False
End With
With Selection.FormatConditions(1).Font
.Color = -16752384
.TintAndShade = 0
End With
With Selection.FormatConditions(1).Interior
.PatternColorIndex = xlAutomatic
.Color = 13561798
.TintAndShade = 0
End With
Selection.FormatConditions(1).StopIfTrue = False
End Sub
```

#### 14. Highlight Named Ranges <a href="#id-18-14-highlight-named-ranges" id="id-18-14-highlight-named-ranges"></a>

If you are not sure about how many named ranges you have in your worksheet then you can use this code to highlight all of them.

```
Sub HighlightRanges()
Dim RangeName As Name
Dim HighlightRange As Range
On Error Resume Next
For Each RangeName In ActiveWorkbook.Names
Set HighlightRange = RangeName.RefersToRange
HighlightRange.Interior.ColorIndex = 36
Next RangeName
End Sub
```

#### 15. Highlight Greater than Values <a href="#id-19-15-highlight-greater-than-values" id="id-19-15-highlight-greater-than-values"></a>

Once you run this code it will ask you for the value from which you want to highlight all greater values.

```
Sub HighlightGreaterThanValues()
Dim i As Integer
i = InputBox("Enter Greater Than Value", "Enter Value")
Selection.FormatConditions.Delete
Selection.FormatConditions.Add Type:=xlCellValue, _
Operator:=xlGreater, Formula1:=i
Selection.FormatConditions(Selection.FormatConditions.Count).S
tFirstPriority
With Selection.FormatConditions(1)
.Font.Color = RGB(0, 0, 0)
.Interior.Color = RGB(31, 218, 154)
End With
End Sub
```

#### 16. Highlight Lower Than Values <a href="#id-20-16-highlight-lower-than-values" id="id-20-16-highlight-lower-than-values"></a>

Once you run this code it will ask you for the value from which you want to highlight all lower values.

```
Sub HighlightLowerThanValues()
Dim i As Integer
i = InputBox("Enter Lower Than Value", "Enter Value")
Selection.FormatConditions.Delete
Selection.FormatConditions.Add _
Type:=xlCellValue, _
Operator:=xlLower, _
Formula1:=i
Selection.FormatConditions(Selection.FormatConditions.Count).S
tFirstPriority
With Selection.FormatConditions(1)
.Font.Color = RGB(0, 0, 0)
.Interior.Color = RGB(217, 83, 79)
End With
End Sub
```

#### 17. Highlight Negative Numbers <a href="#id-21-17-highlight-negative-numbers" id="id-21-17-highlight-negative-numbers"></a>

Select a range of cells and run this code. It will check each cell from the range and highlight all cells where you have a negative number.

```
Sub highlightNegativeNumbers()
Dim Rng As Range
For Each Rng In Selection
If WorksheetFunction.IsNumber(Rng) Then
If Rng.Value &lt; 0 Then
Rng.Font.Color= -16776961
End If
End If
Next
End Sub
```

#### 18. Highlight Specific Text <a href="#id-22-18-highlight-specific-text" id="id-22-18-highlight-specific-text"></a>

Suppose you have a large data set, and you want to check for a particular value. For this, you can use this code. When you run it, you will get an input box to enter the value to search for.

```
Sub highlightValue()
Dim myStr As String
Dim myRg As range
Dim myTxt As String
Dim myCell As range
Dim myChar As String
Dim I As Long
Dim J As Long
On Error Resume Next
If ActiveWindow.RangeSelection.Count &gt; 1 Then
myTxt = ActiveWindow.RangeSelection.AddressLocal
Else
myTxt = ActiveSheet.UsedRange.AddressLocal
End If
LInput: Set myRg = _
Application.InputBox _
("please select the data range:", "Selection Required", myTxt, , , , , 8)
If myRg Is Nothing Then
Exit Sub
If myRg.Areas.Count &gt; 1 Then
MsgBox "not support multiple columns"
GoTo LInput
End If
If myRg.Columns.Count &lt;&gt; 2 Then
MsgBox "the selected range can only contain two columns "
GoTo LInput
End If
For I = 0 To myRg.Rows.Count - 1
myStr = myRg.range("B1").Offset(I, 0).Value
With myRg.range("A1").Offset(I, 0)
.Font.ColorIndex = 1
For J = 1 To Len(.Text)
Mid(.Text, J, Len(myStr)) = myStrThen
.Characters(J, Len(myStr)).Font.ColorIndex = 3
Next
End With
Next I
End Sub
```

To highlight all the cells with comments use this macro.

```
Sub highlightCommentCells()
Selection.SpecialCells(xlCellTypeComments).Select
Selection.Style= "Note"
End Sub
```

#### 20. Highlight Alternate Rows in the Selection <a href="#id-24-20-highlight-alternate-rows-in-the-selection" id="id-24-20-highlight-alternate-rows-in-the-selection"></a>

By highlighting alternate rows, you can make your data easily readable, and for this, you can use below VBA code. It will simply highlight every alternate row in selected range.

```
Sub highlightAlternateRows()
Dim rng As Range
For Each rng In Selection.Rows
If rng.Row Mod 2 = 1 Then
rng.Style = "20% -Accent1"
rng.Value = rng ^ (1 / 3)
Else
End If
Next rng
End Sub
```

#### 21. Highlight Cells with Misspelled Words <a href="#id-25-21-highlight-cells-with-misspelled-words" id="id-25-21-highlight-cells-with-misspelled-words"></a>

If you find hard to check all the cells for spelling error, then this code is for you. It will check each cell from the selection and highlight the cell where is a misspelled word.

```
Sub HighlightMisspelledCells()
Dim rng As Range
For Each rng In ActiveSheet.UsedRange
If Not Application.CheckSpelling(word:=rng.Text) Then
rng.Style = "Bad"
End If
Next rng
End Sub
```

#### 22. Highlight Cells with Error in the Entire Worksheet <a href="#id-26-22-highlight-cells-with-error-in-the-entire-worksheet" id="id-26-22-highlight-cells-with-error-in-the-entire-worksheet"></a>

To highlight and count all the cells in which you have an error, this code will help you. Just run this code and it will return a message with the number error cells and highlight all the cells.

```
Sub highlightErrors()
Dim rng As Range
Dim i As Integer
For Each rng In ActiveSheet.UsedRange
If WorksheetFunction.IsError(rng) Then
i = i + 1
rng.Style = "bad"
End If
Next rng
MsgBox _
"There are total " & i _
& " error(s) in this worksheet."
End Sub
```

#### 23. Highlight Cells with a Specific Text in Worksheet <a href="#id-27-23-highlight-cells-with-a-specific-text-in-worksheet" id="id-27-23-highlight-cells-with-a-specific-text-in-worksheet"></a>

This code will help you to count the cells which have a specific value which you will mention and after that highlight all those cells.

```
Sub highlightSpecificValues()
Dim rng As range
Dim i As Integer
Dim c As Variant
c = InputBox("Enter Value To Highlight")
For Each rng In ActiveSheet.UsedRange
If rng = c Then
rng.Style = "Note"
i = i + 1
End If
Next rng
MsgBox "There are total " & i & " " & c & " in this worksheet."
End Sub
```

#### 24. Highlight all the Blank Cells Invisible Space <a href="#id-28-24-highlight-all-the-blank-cells-invisible-space" id="id-28-24-highlight-all-the-blank-cells-invisible-space"></a>

Sometimes there are some cells which are blank, but they have a single space and due to this, it’s really hard to identify them. This code will check all the cell in the worksheet and highlight all the cells which have a single space.

```
Sub blankWithSpace()
Dim rng As Range
For Each rng In ActiveSheet.UsedRange
If rng.Value = " " Then
rng.Style = "Note"
End If
Next rng
End Sub
```

#### 25. Highlight Max Value in the Range <a href="#id-29-25-highlight-max-value-in-the-range" id="id-29-25-highlight-max-value-in-the-range"></a>

It will check all the selected cells and highlight the cell with the maximum value.

```
Sub highlightMaxValue()
Dim rng As Range
For Each rng In Selection
If rng = WorksheetFunction.Max(Selection) Then
rng.Style = "Good"
End If
Next rng
End Sub
```

#### 26. Highlight Min Value in the Range <a href="#id-30-26-highlight-min-value-in-the-range" id="id-30-26-highlight-min-value-in-the-range"></a>

It will check all the selected cells and highlight the cell with the Minimum value.

```
Sub Highlight_Min_Value()
Dim rng As Range
For Each rng In Selection
If rng = WorksheetFunction.Min(Selection) Then
rng.Style = "Good"
End If
Next rng
End Sub
```

#### 27. Highlight Unique Values <a href="#id-31-27-highlight-unique-values" id="id-31-27-highlight-unique-values"></a>

This code will highlight all the cells from the selection which has a unique value.

```
Sub highlightUniqueValues()
Dim rng As Range
Set rng = Selection
rng.FormatConditions.Delete
Dim uv As UniqueValues
Set uv = rng.FormatConditions.AddUniqueValues
uv.DupeUnique = xlUnique
uv.Interior.Color = vbGreen
End Sub
```

#### 28. Highlight Difference in Columns <a href="#id-32-28-highlight-difference-in-columns" id="id-32-28-highlight-difference-in-columns"></a>

Using this code, you can highlight the difference between two columns (corresponding cells).

```
Sub columnDifference()
Range("H7:H8,I7:I8").Select
Selection.ColumnDifferences(ActiveCell).Select
Selection.Style= "Bad"
End Sub
```

#### 29. Highlight Difference in Rows <a href="#id-33-29-highlight-difference-in-rows" id="id-33-29-highlight-difference-in-rows"></a>

And by using this code you can highlight difference between two row (corresponding cells).

```
Sub rowDifference()
Range("H7:H8,I7:I8").Select
Selection.RowDifferences(ActiveCell).Select
Selection.Style= "Bad"
End Sub
```

### Printing Codes

```
Sub printComments()
With ActiveSheet.PageSetup
.printComments = xlPrintSheetEnd
End With
End Sub
```

Use this macro to activate settings to print cell comments in the end of the page. Let’s say you have 10 pages to print, after using this code you will get all the comments on 11th last page.

#### 31. Print Narrow Margin <a href="#id-36-31-print-narrow-margin" id="id-36-31-print-narrow-margin"></a>

Use this VBA code to take a print with a narrow margin. When you run this macro it will automatically change margins to narrow.

```
Sub printNarrowMargin()
With ActiveSheet.PageSetup
.LeftMargin = Application
.InchesToPoints (0.25)
.RightMargin = Application.InchesToPoints(0.25)
.TopMargin = Application.InchesToPoints(0.75)
.BottomMargin = Application.InchesToPoints(0.75)
.HeaderMargin = Application.InchesToPoints(0.3)
.FooterMargin = Application.InchesToPoints(0.3)
End With
ActiveWindow.SelectedSheets.PrintOut _
Copies:=1, _
Collate:=True, _
IgnorePrintAreas:=False
End Sub
```

#### 32. Print Selection <a href="#id-37-32-print-selection" id="id-37-32-print-selection"></a>

This code will help you print selected range. You don’t need to go to printing options and set printing range. Just select a range and run this code.

```
Sub printSelection()
Selection.PrintOut Copies:=1, Collate:=True
End Sub
```

#### 33. Print Custom Pages <a href="#id-38-33-print-custom-pages" id="id-38-33-print-custom-pages"></a>

Instead of using the setting from print options you can use this code to print custom page range. Let’s say you want to print pages from 5 to 10. You just need to run this VBA code and enter start page and end page.

```
Sub printCustomSelection()
Dim startpage As Integer
Dim endpage As Integer
startpage = _
InputBox("Please Enter Start Page number.", "Enter Value")
If Not WorksheetFunction.IsNumber(startpage) Then
MsgBox _
"Invalid Start Page number. Please try again.", "Error"
Exit Sub
End If
endpage = _
InputBox("Please Enter End Page number.", "Enter Value")
If Not WorksheetFunction.IsNumber(endpage) Then
MsgBox _
"Invalid End Page number. Please try again.", "Error"
Exit Sub
End If
Selection.PrintOut From:=startpage, _
To:=endpage, Copies:=1, Collate:=True
End Sub
```

### Worksheet Codes

#### 34. Hide all but the Active Worksheet <a href="#id-40-34-hide-all-but-the-active-worksheet" id="id-40-34-hide-all-but-the-active-worksheet"></a>

Now, let’s say if you want to hide all the worksheets in your workbook other than the active worksheet. This macro code will do this for you.

```
Sub HideWorksheet()
Dim ws As Worksheet
For Each ws In ThisWorkbook.Worksheets
If ws.Name &lt;&gt; ThisWorkbook.ActiveSheet.Name Then
ws.Visible = xlSheetHidden
End If
Next ws
End Sub
```

**Related:** [**VBA Functions List**](https://excelchamps.com/vba/functions/)

#### 35. Unhide all Hidden Worksheets <a href="#id-41-35-unhide-all-hidden-worksheets" id="id-41-35-unhide-all-hidden-worksheets"></a>

And if you want to un-hide all the worksheets which you have hide with previous code, here is the code for that.

```
Sub UnhideAllWorksheet()
Dim ws As Worksheet
For Each ws In ActiveWorkbook.Worksheets
ws.Visible = xlSheetVisible
Next ws
End Sub
```

#### 36. Delete All but the Active Worksheet <a href="#id-42-36-delete-all-but-the-active-worksheet" id="id-42-36-delete-all-but-the-active-worksheet"></a>

If you want to delete all the worksheets other than the active sheet, this macro is useful for you. When you run this macro, it will compare the name of the active worksheet with other worksheets and then delete them.

```
Sub DeleteWorksheets()
Dim ws As Worksheet
For Each ws In ThisWorkbook.Worksheets
If ws.name &lt;&gt; ThisWorkbook.ActiveSheet.name Then
Application.DisplayAlerts = False
ws.Delete
Application.DisplayAlerts = True
End If
Next ws
End Sub
```

#### 37. Protect all Worksheets Instantly <a href="#id-43-37-protect-all-worksheets-instantly" id="id-43-37-protect-all-worksheets-instantly"></a>

If you want to protect your all worksheets in one go here is a code for you. When you run this macro, you will get an input box to enter a password. Once you enter your password, click OK. And make sure to take care about CAPS.

```
Sub ProtectAllWorskeets()
Dim ws As Worksheet
Dim ps As String
ps = InputBox("Enter a Password.", vbOKCancel)
For Each ws In ActiveWorkbook.Worksheets
ws.Protect Password:=ps
Next ws
End Sub
```

#### 38. Resize All Charts in a Worksheet <a href="#id-44-38-resize-all-charts-in-a-worksheet" id="id-44-38-resize-all-charts-in-a-worksheet"></a>

Make all chart same in size. This macro code will help you to make all the charts of the same size. You can change the height and width of charts by changing it in macro code.

```
Sub Resize_Charts()
Dim i As Integer
For i = 1 To ActiveSheet.ChartObjects.Count
With ActiveSheet.ChartObjects(i)
.Width = 300
.Height = 200
End With
Next i
End Sub
```

#### 39. Insert Multiple Worksheets <a href="#id-45-39-insert-multiple-worksheets" id="id-45-39-insert-multiple-worksheets"></a>

You can use this code if you want to add multiple worksheets in your workbook in a single shot. When you run this macro code you will get an input box to enter the total number of sheets you want to enter.

```
Sub InsertMultipleSheets()
Dim i As Integer
i = _
InputBox("Enter number of sheets to insert.", _
"Enter Multiple Sheets")
Sheets.Add After:=ActiveSheet, Count:=i
End Sub
```

#### 40. Protect Worksheet <a href="#id-46-40-protect-worksheet" id="id-46-40-protect-worksheet"></a>

If you want to protect your worksheet you can use this macro code. All you have to do just mention your password in the code.

```
Sub ProtectWS()
ActiveSheet.Protect "mypassword", True, True
End Sub
```

#### 41. Un-Protect Worksheet <a href="#id-47-41-un-protect-worksheet" id="id-47-41-un-protect-worksheet"></a>

If you want to unprotect your worksheet you can use this macro code. All you have to do just mention your password which you have used while protecting your worksheet.

```
Sub UnprotectWS()
ActiveSheet.Unprotect "mypassword"
End Sub
```

#### 42. Sort Worksheets <a href="#id-48-42-sort-worksheets" id="id-48-42-sort-worksheets"></a>

This code will help you to sort worksheets in your workbook according to their name.

```
Sub SortWorksheets()
Dim i As Integer
Dim j As Integer
Dim iAnswer As VbMsgBoxResult
iAnswer = MsgBox("Sort Sheets in Ascending Order?" & Chr(10) _
& "Clicking No will sort in Descending Order", _
vbYesNoCancel + vbQuestion + vbDefaultButton1, "Sort Worksheets")
For i = 1 To Sheets.Count
For j = 1 To Sheets.Count - 1
If iAnswer = vbYes Then
If UCase$(Sheets(j).Name) &gt; UCase$(Sheets(j + 1).Name) Then
Sheets(j).Move After:=Sheets(j + 1)
End If
ElseIf iAnswer = vbNo Then
If UCase$(Sheets(j).Name) &lt; UCase$(Sheets(j + 1).Name) Then Sheets(j).Move After:=Sheets(j + 1)
End If
End If
Next j
Next i
End Sub
```

#### 43. Protect all the Cells with Formulas <a href="#id-49-43-protect-all-the-cells-with-formulas" id="id-49-43-protect-all-the-cells-with-formulas"></a>

To protect cell with formula with a single click you can use this code.

```
Sub lockCellsWithFormulas()
With ActiveSheet
.Unprotect
.Cells.Locked = False
.Cells.SpecialCells(xlCellTypeFormulas).Locked = True
.Protect AllowDeletingRows:=True
End With
End Sub
```

#### 44. Delete all Blank Worksheets <a href="#id-50-44-delete-all-blank-worksheets" id="id-50-44-delete-all-blank-worksheets"></a>

Run this code and it will check all the worksheets in the active workbook and delete if a worksheet is blank.

```
Sub deleteBlankWorksheets()
Dim Ws As Worksheet
On Error Resume Next
Application.ScreenUpdating= False
Application.DisplayAlerts= False
For Each Ws In Application.Worksheets
If Application.WorksheetFunction.CountA(Ws.UsedRange) = 0 Then
Ws.Delete
End If
Next
Application.ScreenUpdating= True
Application.DisplayAlerts= True
End Sub
```

#### 45. Unhide all Rows and Columns <a href="#id-51-45-unhide-all-rows-and-columns" id="id-51-45-unhide-all-rows-and-columns"></a>

Instead of unhiding rows and columns on by one manually you can use this code to do this in a single go.

```
Sub UnhideRowsColumns()
Columns.EntireColumn.Hidden = False
Rows.EntireRow.Hidden = False
End Sub
```

#### 46. Save Each Worksheet as a Single PDF <a href="#id-52-46-save-each-worksheet-as-a-single-pdf" id="id-52-46-save-each-worksheet-as-a-single-pdf"></a>

This code will simply save all the worksheets in a separate PDF file. You just need to change the folder name from the code.

```
Sub SaveWorkshetAsPDF()
Dimws As Worksheet
For Each ws In Worksheets
ws.ExportAsFixedFormat _
xlTypePDF, _
"ENTER-FOLDER-NAME-HERE" &; _
ws.Name & ".pdf"
Next ws
End Sub
```

#### 47. Disable Page Breaks <a href="#id-53-47-disable-page-breaks" id="id-53-47-disable-page-breaks"></a>

To disable page breaks use this code. It will simply disable page breaks from all the open workbooks.

```
Sub DisablePageBreaks()
Dim wb As Workbook
Dim wks As Worksheet
Application.ScreenUpdating = False
For Each wb In Application.Workbooks
For Each Sht In wb.Worksheets
Sht.DisplayPageBreaks = False
Next Sht
Next wb
Application.ScreenUpdating = True
End Sub
```

### Workbook Codes

These codes will help you to perform workbook level tasks in an easy way and with minimum efforts.&#x20;

#### 48. Create a Backup of a Current Workbook <a href="#id-55-48-create-a-backup-of-a-current-workbook" id="id-55-48-create-a-backup-of-a-current-workbook"></a>

This is one of the most useful macros which can help you to save a backup file of your current workbook.

```
Sub FileBackUp()
ThisWorkbook.SaveCopyAs Filename:=ThisWorkbook.Path & _
"" & Format(Date, "mm-dd-yy") & " " & _
ThisWorkbook.name
End Sub
```

It will save a backup file in the same directory where your current file is saved and it will also add the current date with the name of the file.

#### 49. Close all Workbooks at Once <a href="#id-56-49-close-all-workbooks-at-once" id="id-56-49-close-all-workbooks-at-once"></a>

Use this macro code to close all open workbooks. This macro code will first check all the workbooks one by one and close them.

```
Sub CloseAllWorkbooks()
Dim wbs As Workbook
For Each wbs In Workbooks
wbs.Close SaveChanges:=True
Next wb
End Sub
```

If any of the worksheets is not saved, you’ll get a message to save it.

#### 50. Copy Active Worksheet into a New Workbook <a href="#id-57-50-copy-active-worksheet-into-a-new-workbook" id="id-57-50-copy-active-worksheet-into-a-new-workbook"></a>

Let’s say if you want to copy your active worksheet in a new workbook, just run this macro code and it will do the same for you.

```
Sub CopyWorksheetToNewWorkbook()
ThisWorkbook.ActiveSheet.Copy _
Before:=Workbooks.Add.Worksheets(1)
End Sub
```

It’s a super time saver.

#### 51. Active Workbook in an Email <a href="#id-58-51-active-workbook-in-an-email" id="id-58-51-active-workbook-in-an-email"></a>

Use this macro code to quickly send your active workbook in an e-mail. You can change the subject, email, and body text in code and if you want to send this mail directly, use “.Send” instead of “.Display”.

```
Sub Send_Mail()
Dim OutApp As Object
Dim OutMail As Object
Set OutApp = CreateObject("Outlook.Application")
Set OutMail = OutApp.CreateItem(0)
With OutMail
.to = "Sales@FrontLinePaper.com"
.Subject = "Growth Report"
.Body = "Hello Team, Please find attached Growth Report."
.Attachments.Add ActiveWorkbook.FullName
.display
End With
Set OutMail = Nothing
Set OutApp = Nothing
End Sub
```

#### 52. Add Workbook to a Mail Attachment <a href="#id-59-52-add-workbook-to-a-mail-attachment" id="id-59-52-add-workbook-to-a-mail-attachment"></a>

Once you run this macro it will open your default mail client and attached active workbook with it as an attachment.

```
Sub OpenWorkbookAsAttachment()
Application.Dialogs(xlDialogSendMail).Show
End Sub
```

#### 53. Welcome Message <a href="#id-60-53-welcome-message" id="id-60-53-welcome-message"></a>

You can use auto\_open to perform a task on opening a file and all you have to do just name your macro “auto\_open”.

```
Sub auto_open()
MsgBox _
"Welcome To ExcelChamps &amp; Thanks for downloading this file."
End Sub
```

#### 54. Closing Message <a href="#id-61-54-closing-message" id="id-61-54-closing-message"></a>

You can use close\_open to perform a task on opening a file and all you have to do just name your macro “close\_open”.

```
Sub auto_close()
MsgBox "Bye Bye! Don't forget to check other cool stuff on
excelchamps.com"
End Sub
```

#### 55. Count Open Unsaved Workbooks <a href="#id-62-55-count-open-unsaved-workbooks" id="id-62-55-count-open-unsaved-workbooks"></a>

Let’s you have 5-10 open workbooks; you can use this code to get the number of workbooks which are not saved yet.

```
Sub VisibleWorkbooks()
Dim book As Workbook
Dim i As Integer
For Each book In Workbooks
If book.Saved = False Then
i = i + 1
End If
Next book
MsgBox i
End Sub
```

### Pivot Table Codes

#### 56. Hide Pivot Table Subtotals <a href="#id-64-56-hide-pivot-table-subtotals" id="id-64-56-hide-pivot-table-subtotals"></a>

If you want to hide all the subtotals, just run this code. First of all, make sure to select a cell from your pivot table and then run this macro.

```
Sub HideSubtotals()
Dim pt As PivotTable
Dim pf As PivotField
On Error Resume Next
Set pt = ActiveSheet.PivotTables(ActiveCell.PivotTable.Name)
If pt Is Nothing Then
MsgBox "You must place your cursor inside of a PivotTable."
Exit Sub
End If
For Each pf In pt.PivotFields
pf.Subtotals(1) = True
pf.Subtotals(1) = False
Next pf
End Sub
```

#### 57. Refresh All Pivot Tables <a href="#id-65-57-refresh-all-pivot-tables" id="id-65-57-refresh-all-pivot-tables"></a>

A super quick method to [refresh all pivot tables](https://excelchamps.com/pivot-table/refresh-all/). Just run this code and all of your pivot tables in your workbook will be refresh in a single shot.

```
Sub vba_referesh_all_pivots()
Dim pt As PivotTable
For Each pt In ActiveWorkbook.PivotTables
pt.RefreshTable
Next pt
End Sub
```

#### 58. Create a Pivot Table <a href="#id-66-58-create-a-pivot-table" id="id-66-58-create-a-pivot-table"></a>

Follow this step-by-step guide to [create a pivot table using VBA](https://excelchamps.com/vba/vba-pivot-table/).

#### 59. Auto Update Pivot Table Range <a href="#id-67-59-auto-update-pivot-table-range" id="id-67-59-auto-update-pivot-table-range"></a>

If you are not using Excel tables, then you can use this code to [update pivot table range](https://excelchamps.com/pivot-table/auto-update-range/).

```
Sub UpdatePivotTableRange()
Dim Data_Sheet As Worksheet
Dim Pivot_Sheet As Worksheet
Dim StartPoint As Range
Dim DataRange As Range
Dim PivotName As String
Dim NewRange As String
Dim LastCol As Long
Dim lastRow As Long
'Set Pivot Table &amp; Source Worksheet
Set Data_Sheet = ThisWorkbook.Worksheets("PivotTableData3")
Set Pivot_Sheet = ThisWorkbook.Worksheets("Pivot3")
'Enter in Pivot Table Name
PivotName = "PivotTable2"
'Defining Staring Point &amp; Dynamic Range
Data_Sheet.Activate
Set StartPoint = Data_Sheet.Range("A1")
LastCol = StartPoint.End(xlToRight).Column
DownCell = StartPoint.End(xlDown).Row
Set DataRange = Data_Sheet.Range(StartPoint, Cells(DownCell, LastCol))
NewRange = Data_Sheet.Name &amp; "!" &amp; DataRange.Address(ReferenceStyle:=xlR1C1)
'Change Pivot Table Data Source Range Address
Pivot_Sheet.PivotTables(PivotName). _
ChangePivotCache ActiveWorkbook. _
PivotCaches.Create(SourceType:=xlDatabase, SourceData:=NewRange)
'Ensure Pivot Table is Refreshed
Pivot_Sheet.PivotTables(PivotName).RefreshTable
'Complete Message
Pivot_Sheet.Activate
MsgBox "Your Pivot Table is now updated."
End Sub
```

#### 60. Disable/Enable Get Pivot Data <a href="#id-68-60-disableenable-get-pivot-data" id="id-68-60-disableenable-get-pivot-data"></a>

To disable/enable GetPivotData function you need to [go to the Excel options](https://excelchamps.com/excel-basics/options/). But with this code you can do it in a single click.

```
Sub activateGetPivotData()
Application.GenerateGetPivotData = True
End Sub
Sub deactivateGetPivotData()
Application.GenerateGetPivotData = False
End Sub
```

### Charts Codes

#### 61. Change Chart Type <a href="#id-70-61-change-chart-type" id="id-70-61-change-chart-type"></a>

This code will help you to convert chart type without using chart options from the tab. All you have to do just specify to which type you want to convert. Below code will convert selected chart to a clustered column chart.

```
Sub ChangeChartType()
ActiveChart.ChartType = xlColumnClustered
End Sub
```

There are different codes for different types, you can [find all those types from here](https://msdn.microsoft.com/en-us/library/office/ff838409.aspx).

#### 62. Paste Chart as an Image <a href="#id-71-62-paste-chart-as-an-image" id="id-71-62-paste-chart-as-an-image"></a>

This code will help you to convert your chart into an image. You just need to select your chart and run this code.

```
Sub ConvertChartToPicture()
ActiveChart.ChartArea.Copy
ActiveSheet.Range("A1").Select
ActiveSheet.Pictures.Paste.Select
End Sub
```

#### 63. Add Chart Title <a href="#id-72-63-add-chart-title" id="id-72-63-add-chart-title"></a>

First of all, you need to select your chart and the run this code. You will get an input box to enter chart title.

```
Sub AddChartTitle()
Dim i As Variant
i = InputBox("Please enter your chart title", "Chart Title")
On Error GoTo Last
ActiveChart.SetElement (msoElementChartTitleAboveChart)
ActiveChart.ChartTitle.Text = i
Last:
Exit Sub
End Sub
```

### Advanced Codes

#### 64. Save Selected Range as a PDF <a href="#id-74-64-save-selected-range-as-a-pdf" id="id-74-64-save-selected-range-as-a-pdf"></a>

If you want to hide all the subtotals, just run this code. First of all, make sure to select a cell from your pivot table and then run this macro.

```
Sub HideSubtotals()
Dim pt As PivotTable
Dim pf As PivotField
On Error Resume Next
Set pt = ActiveSheet.PivotTables(ActiveCell.PivotTable.name)
If pt Is Nothing Then
MsgBox "You must place your cursor inside of a PivotTable."
Exit Sub
End If
For Each pf In pt.PivotFields
pf.Subtotals(1) = True
pf.Subtotals(1) = False
Next pf
End Sub
```

#### 65. Create a Table of Content <a href="#id-75-65-create-a-table-of-content" id="id-75-65-create-a-table-of-content"></a>

Let’s say you have more than 100 worksheets in your workbook and it’s hard to navigate now. Don’t worry this macro code will rescue everything.

```
Sub TableofContent()
Dim i As Long
On Error Resume Next
Application.DisplayAlerts = False
Worksheets("Table of Content").Delete
Application.DisplayAlerts = True
On Error GoTo 0
ThisWorkbook.Sheets.Add Before:=ThisWorkbook.Worksheets(1)
ActiveSheet.Name = "Table of Content"
For i = 1 To Sheets.Count
With ActiveSheet
.Hyperlinks.Add _
Anchor:=ActiveSheet.Cells(i, 1), _
Address:="", _
SubAddress:="'" &amp; Sheets(i).Name &amp; "'!A1", _
ScreenTip:=Sheets(i).Name, _
TextToDisplay:=Sheets(i).Name
End With
Next i
End Sub
```

When you run this code, it will create a new worksheet and create a index of worksheets with a hyperlink to them.

#### 66. Convert Range into an Image <a href="#id-76-66-convert-range-into-an-image" id="id-76-66-convert-range-into-an-image"></a>

Paste selected range as an image. You just have to select the range and once you run this code it will automatically [insert a picture for that range](https://excelchamps.com/advanced-excel/camera-tool/).

```
Sub PasteAsPicture()
Application.CutCopyMode = False
Selection.Copy
ActiveSheet.Pictures.Paste.Select
End Sub
```

#### 67. Insert a Linked Picture <a href="#id-77-67-insert-a-linked-picture" id="id-77-67-insert-a-linked-picture"></a>

This VBA code will convert your selected range into a linked picture and you can use that image anywhere you want.

```
Sub LinkedPicture()
Selection.Copy
ActiveSheet.Pictures.Paste(Link:=True).Select
End Sub
```

#### 68. Use Text to Speech <a href="#id-78-68-use-text-to-speech" id="id-78-68-use-text-to-speech"></a>

Just select a range and run this code. Excel will speak all the text what you have in that range, cell by cell.

```
Sub Speak()
Selection.Speak
End Sub
```

#### 69. Activate Data Entry Form <a href="#id-79-69-activate-data-entry-form" id="id-79-69-activate-data-entry-form"></a>

There is a [default data entry form](https://excelchamps.com/advanced-excel/data-entry-form/) which you can use for data entry.

```
Sub DataForm()
ActiveSheet.ShowDataForm
End Sub
```

#### 70. Use Goal Seek <a href="#id-80-70-use-goal-seek" id="id-80-70-use-goal-seek"></a>

Goal Seek can be super helpful for you to solve complex problems. Learn more about [goal seek from here](https://excelchamps.com/advanced-excel/goal-seek/) before you use this code.

```
Sub GoalSeekVBA()
Dim Target As Long
On Error GoTo Errorhandler
Target = InputBox("Enter the required value", "Enter Value")
Worksheets("Goal_Seek").Activate
With ActiveSheet.Range("C7")
.GoalSeek_ Goal:=Target, _
ChangingCell:=Range("C2")
End With
Exit Sub
Errorhandler: MsgBox ("Sorry, value is not valid.")
End Sub
```

#### 71. VBA Code to Search on Google <a href="#id-81-71-vba-code-to-search-on-google" id="id-81-71-vba-code-to-search-on-google"></a>

```
Sub SearchWindow32()
Dim chromePath As String
Dim search_string As String
Dim query As String
query = InputBox("Enter here your search here", "Google Search")
search_string = query
search_string = Replace(search_string, " ", "+")
'Uncomment the following line for Windows 64 versions and comment out Windows 32 versions'
'chromePath = "C:Program FilesGoogleChromeApplicationchrome.exe"
'Uncomment the following line for Windows 32 versions and comment out Windows 64 versions
'chromePath = "C:Program Files (x86)GoogleChromeApplicationchrome.exe"
Shell (chromePath &amp; " -url http://google.com/#q=" &amp; search_string)
End Sub
```

### Formula Codes

#### 72. Convert all Formulas into Values <a href="#id-83-72-convert-all-formulas-into-values" id="id-83-72-convert-all-formulas-into-values"></a>

Simply convert formulas into values. When you run this macro it will quickly change the [formulas into absolute values](https://excelchamps.com/excel-basics/formula-to-value/).

```
Sub convertToValues()
Dim MyRange As Range
Dim MyCell As Range
Select Case _
MsgBox("You Can't Undo This Action. " _
&amp; "Save Workbook First?", vbYesNoCancel, _
"Alert")
Case Is = vbYes
ThisWorkbook.Save
Case Is = vbCancel
Exit Sub
End Select
Set MyRange = Selection
For Each MyCell In MyRange
If MyCell.HasFormula Then
MyCell.Formula = MyCell.Value
End If
Next MyCell
End Sub
```

#### 73. Remove Spaces from Selected Cells <a href="#id-84-73-remove-spaces-from-selected-cells" id="id-84-73-remove-spaces-from-selected-cells"></a>

One of the most useful macros from this list. It will check your selection and then remove all the extra spaces from that.

```
Sub RemoveSpaces()
Dim myRange As Range
Dim myCell As Range
Select Case MsgBox("You Can't Undo This Action. " _
&amp; "Save Workbook First?", _
vbYesNoCancel, "Alert")
Case Is = vbYesThisWorkbook.Save
Case Is = vbCancel
Exit Sub
End Select
Set myRange = Selection
For Each myCell In myRange
If Not IsEmpty(myCell) Then
myCell = Trim(myCell)
End If
Next myCell
End Sub
```

#### 74. Remove Characters from a String <a href="#id-85-74-remove-characters-from-a-string" id="id-85-74-remove-characters-from-a-string"></a>

Simply remove characters from the starting of a text string. All you need is to refer to a cell or insert a text into the function and number of characters to remove from the text string.

```
Public Function removeFirstC(rng As String, cnt As Long)
removeFirstC = Right(rng, Len(rng) - cnt)
End Function
```

It has two arguments “rng” for the text string and “cnt” for the count of characters to remove. **For Example:** If you want to [remove first characters from a cell](https://excelchamps.com/blog/remove-first-character/), you need to enter 1 in cnt.

#### 75. Add Insert Degree Symbol in Excel <a href="#id-86-75-add-insert-degree-symbol-in-excel" id="id-86-75-add-insert-degree-symbol-in-excel"></a>

Let’s say you have a list of numbers in a column and you want to [add degree symbol](https://excelchamps.com/excel-basics/degree/) with all of them.

```
Sub degreeSymbol( )
Dim rng As Range
For Each rng In Selection
rng.Select
If ActiveCell &lt;&gt; "" Then
If IsNumeric(ActiveCell.Value) Then
ActiveCell.Value = ActiveCell.Value &amp; "°"
End If
End If
Next
End Sub
```

#### 76. Reverse Text <a href="#id-87-76-reverse-text" id="id-87-76-reverse-text"></a>

All you have to do just enter “rvrse” function in a cell and refer to the cell in which you have text which you want to reverse.

```
Public Function rvrse(ByVal cell As Range) As String
rvrse = VBA.strReverse(cell.Value)
End Function
```

#### 77. Activate R1C1 Reference Style <a href="#id-88-77-activate-r1c1-reference-style" id="id-88-77-activate-r1c1-reference-style"></a>

This macro code will help you to activate [R1C1 reference style](https://excelchamps.com/formulas/r1c1/) without using Excel options.

```
Sub ActivateR1C1()
If Application.ReferenceStyle = xlA1 Then
Application.ReferenceStyle = xlR1C1
Else
Application.ReferenceStyle = xlR1C1
End If
End Sub
```

#### 78. Activate A1 Reference Style <a href="#id-89-78-activate-a1-reference-style" id="id-89-78-activate-a1-reference-style"></a>

This macro code will help you to activate A1 reference style without using Excel options.

```
Sub ActivateA1()
If Application.ReferenceStyle = xlR1C1 Then
Application.ReferenceStyle = xlA1
Else
Application.ReferenceStyle = xlA1
End If
End Sub
```

#### 79. Insert Time Range <a href="#id-90-79-insert-time-range" id="id-90-79-insert-time-range"></a>

With this code, you can insert a time range in sequence from 00:00 to 23:00.

```
Sub TimeStamp()
Dim i As Integer
For i = 1 To 24
ActiveCell.FormulaR1C1 = i &amp; ":00"
ActiveCell.NumberFormat = "[$-409]h:mm AM/PM;@"
ActiveCell.Offset(RowOffset:=1, ColumnOffset:=0).Select
Next i
End Sub
```

#### 80. Convert Date into Day <a href="#id-91-80-convert-date-into-day" id="id-91-80-convert-date-into-day"></a>

If you have dates in your worksheet and you want to convert all those dates into days then this code is for you. Simply select the range of cells and run this macro.

```
Sub date2day()
Dim tempCell As Range
Selection.Value = Selection.Value
For Each tempCell In Selection
If IsDate(tempCell) = True Then
With tempCell
.Value = Day(tempCell)
.NumberFormat = "0"
End With
End If
Next tempCell
End Sub
```

#### 81. Convert Date into Year <a href="#id-92-81-convert-date-into-year" id="id-92-81-convert-date-into-year"></a>

This code will convert dates into years.

```
Sub date2year()
Dim tempCell As Range
Selection.Value = Selection.Value
For Each tempCell In Selection
If IsDate(tempCell) = True Then
With tempCell
.Value = Year(tempCell)
.NumberFormat = "0"
End With
End If
Next tempCell
End Sub
```

#### 82. Remove Time from Date <a href="#id-93-82-remove-time-from-date" id="id-93-82-remove-time-from-date"></a>

If you have time with the date and you want to remove it then you can use this code.

```
Sub removeTime()
Dim Rng As Range
For Each Rng In Selection
If IsDate(Rng) = True Then
Rng.Value = VBA.Int(Rng.Value)
End If
Next
Selection.NumberFormat = "dd-mmm-yy"
End Sub
```

#### 83. Remove Date from Date and Time <a href="#id-94-83-remove-date-from-date-and-time" id="id-94-83-remove-date-from-date-and-time"></a>

It will return only time from a date and time value.

```
Sub removeDate()
Dim Rng As Range
For Each Rng In Selection
If IsDate(Rng) = True Then
Rng.Value = Rng.Value - VBA.Fix(Rng.Value)
End If
NextSelection.NumberFormat = "hh:mm:ss am/pm"
End Sub
```

#### 84. Convert to Upper Case <a href="#id-95-84-convert-to-upper-case" id="id-95-84-convert-to-upper-case"></a>

Select the cells and run this code. It will check each and every cell of selected range and then convert it into upper case text.

```
Sub convertUpperCase()
Dim Rng As Range
For Each Rng In Selection
If Application.WorksheetFunction.IsText(Rng) Then
Rng.Value = UCase(Rng)
End If
Next
End Sub
```

#### 85. Convert to Lower Case <a href="#id-96-85-convert-to-lower-case" id="id-96-85-convert-to-lower-case"></a>

This code will help you to convert selected text into lower case text. Just select a range of cells where you have text and run this code. If a cell has a number or any value other than text that value will remain same.

```
Sub convertLowerCase()
Dim Rng As Range
For Each Rng In Selection
If Application.WorksheetFunction.IsText(Rng) Then
Rng.Value= LCase(Rng)
End If
Next
End Sub
```

#### 86. Convert to Proper Case <a href="#id-97-86-convert-to-proper-case" id="id-97-86-convert-to-proper-case"></a>

And this code will convert selected text into the proper case where you have the first letter in capital and rest in small.

```
Sub convertProperCase()
Dim Rng As Range
For Each Rng In Selection
If WorksheetFunction.IsText(Rng) Then
Rng.Value = WorksheetFunction.Proper(Rng.Value)
End If
Next
End Sub
```

#### 87. Convert to Sentence Case <a href="#id-98-87-convert-to-sentence-case" id="id-98-87-convert-to-sentence-case"></a>

In text case, you have the first letter of the first word in capital and rest all in words in small for a single sentence and this code will help you convert [normal text into sentence case](https://excelchamps.com/formulas/sentence-case/).

```
Sub convertTextCase()
Dim Rng As Range
For Each Rng In Selection
If WorksheetFunction.IsText(Rng) Then
Rng.Value = UCase(Left(Rng, 1)) &amp; LCase(Right(Rng, Len(Rng) - 1))
End If
Next Rng
End Sub
```

#### 88. Remove a Character from Selection <a href="#id-99-88-remove-a-character-from-selection" id="id-99-88-remove-a-character-from-selection"></a>

To remove a particular character from a selected cell you can use this code. It will show you an input box to enter the character you want to remove.

```
Sub removeChar()
Dim Rng As Range
Dim rc As String
rc = InputBox("Character(s) to Replace", "Enter Value")
For Each Rng In Selection
Selection.Replace What:=rc, Replacement:=""
Next
End Sub
```

#### 89. Word Count from Entire Worksheet <a href="#id-100-89-word-count-from-entire-worksheet" id="id-100-89-word-count-from-entire-worksheet"></a>

It can help you to count all the words from a worksheet.

```
Sub Word_Count_Worksheet()
Dim WordCnt As Long
Dim rng As Range
Dim S As String
Dim N As Long
For Each rng In ActiveSheet.UsedRange.Cells
S = Application.WorksheetFunction.Trim(rng.Text)
N = 0
If S &lt;&gt; vbNullString Then
N = Len(S) - Len(Replace(S, " ", "")) + 1
End If
WordCnt = WordCnt + N
Next rng
MsgBox "There are total " _
&amp; Format(WordCnt, "#,##0") &amp; _
" words in the active worksheet"
End Sub
```

#### 90. Remove the Apostrophe from a Number <a href="#id-101-90-remove-the-apostrophe-from-a-number" id="id-101-90-remove-the-apostrophe-from-a-number"></a>

If you have numeric data with an apostrophe before each number, you run this code to remove it.

```
Sub removeApostrophes()
Selection.Value = Selection.Value
End Sub
```

#### 91. Remove Decimals from Numbers <a href="#id-102-91-remove-decimals-from-numbers" id="id-102-91-remove-decimals-from-numbers"></a>

This code will help you remove all the decimals from the numbers from the selected range.

```
Sub removeDecimals()
Dim lnumber As Double
Dim lResult As Long
Dim rng As Range
For Each rng In Selection
rng.Value = Int(rng)
rng.NumberFormat = "0"
Next rng
End Sub
```

#### 92. Multiply all the Values by a Number <a href="#id-103-92-multiply-all-the-values-by-a-number" id="id-103-92-multiply-all-the-values-by-a-number"></a>

Let’s have a list of numbers, and you want to multiply all the numbers with a particular one.

```
Sub addNumber()
Dim rng As Range
Dim i As Integer
i = InputBox("Enter number to multiple", "Input Required")
For Each rng In Selection
If WorksheetFunction.IsNumber(rng) Then
rng.Value = rng + i
Else
End If
Next rng
End Sub
```

**To use this code**, Select that range of cells and run this code. It will first ask you for the number with whom you want to multiply and then instantly multiply all the numbers with it.

#### 93. Add a Number in all the Numbers <a href="#id-104-93-add-a-number-in-all-the-numbers" id="id-104-93-add-a-number-in-all-the-numbers"></a>

Just like multiplying, you can also add a number into a set of numbers.

```
Sub addNumber()
Dim rng As Range
Dim i As Integer
i = InputBox("Enter number to multiple", "Input Required")
For Each rng In Selection
If WorksheetFunction.IsNumber(rng) Then
rng.Value = rng + i
Else
End If
Next rng
End Sub
```

#### 94. Calculate the Square Root <a href="#id-105-94-calculate-the-square-root" id="id-105-94-calculate-the-square-root"></a>

You can use this code to calculate square root without applying a formula. It will simply check all the selected cells and convert numbers to their square root.

```
Sub getSquareRoot()
Dim rng As Range
Dim i As Integer
For Each rng In Selection
If WorksheetFunction.IsNumber(rng) Then
rng.Value = Sqr(rng)
Else
End If
Next rng
End Sub
```

#### 95. Calculate the Cube Root <a href="#id-106-95-calculate-the-cube-root" id="id-106-95-calculate-the-cube-root"></a>

You can use this code to calculate cube root without applying a formula. It will simply check all the selected cells and convert numbers to their cube root.

```
Sub getCubeRoot()
Dim rng As Range
Dimi As Integer
For Each rng In Selection
If WorksheetFunction.IsNumber(rng) Then
rng.Value = rng ^ (1 / 3)
Else
End If
Nextrng
End Sub
```

#### 96. Add A-Z Alphabets in a Range <a href="#id-107-96-add-a-z-alphabets-in-a-range" id="id-107-96-add-a-z-alphabets-in-a-range"></a>

Just like serial numbers you can also insert alphabets in your worksheet. Below are the codes which you can use.

```
Sub addsAlphabets1()
Dim i As Integer
For i = 65 To 90
ActiveCell.Value = Chr(i)
ActiveCell.Offset(1, 0).Select
Next i
End SubSub addsAlphabets2()
Dim i As Integer
For i = 97 To 122
ActiveCell.Value = Chr(i)
ActiveCell.Offset(1, 0).Select
Next i
End Sub
```

#### 97. Convert Roman Numbers into Arabic Numbers <a href="#id-108-97-convert-roman-numbers-into-arabic-numbers" id="id-108-97-convert-roman-numbers-into-arabic-numbers"></a>

Sometimes, it’s really hard to understand Roman numbers as serial numbers. This code will help you to convert Roman numbers into Arabic numbers.

```
Sub convertToNumbers()
Dim rng As Range
Selection.Value = Selection.Value
For Each rng In Selection
If Not WorksheetFunction.IsNonText(rng) Then
rng.Value = WorksheetFunction.Arabic(rng)
End If
Next rng
End Sub
```

#### 98. Remove Negative Signs <a href="#id-109-98-remove-negative-signs" id="id-109-98-remove-negative-signs"></a>

This code will check all the cells in the selection and convert all the negative numbers into positive ones. Just select a range and run this code.

```
Sub removeNegativeSign()
Dim rng As Range
Selection.Value = Selection.Value
For Each rng In Selection
If WorksheetFunction.IsNumber(rng) Then
rng.Value = Abs(rng)
End If
Next rng
End Sub
```

#### 99. Replace Blank Cells with Zeros <a href="#id-110-99-replace-blank-cells-with-zeros" id="id-110-99-replace-blank-cells-with-zeros"></a>

For data with blank cells, you can use the code below to add zeros in all those cells. It makes easier to use those cells in further calculations.

```
Sub replaceBlankWithZero()
Dim rng As Range
Selection.Value = Selection.Value
For Each rng In Selection
If rng = "" Or rng = " " Then
rng.Value = "0"
Else
End If
Next rng
End Sub
```

#### 100. Create a Simple Timer

```
Sub SimpleTimer()
    Dim countDown As Date
    countDown = Now + TimeValue("00:01:00") ' Set timer for 1 minute
    Do Until Now >= countDown
        DoEvents
    Loop
    MsgBox "Time's up!"
End Sub
```

#### 101. Convert Text to Columns Automatically

```
Sub TextToColumnsAuto()
    Dim rng As Range
    Set rng = ThisWorkbook.Sheets("Sheet1").Range("A1:A100")
    rng.TextToColumns Destination:=rng, DataType:=xlDelimited, Comma:=True
End Sub
```

#### 102. Unprotect All Sheets in a Workbook

```
Sub UnprotectSheets()
    Dim ws As Worksheet
    For Each ws In ThisWorkbook.Sheets
        ws.Unprotect Password:="password"
    Next ws
End Sub
```

#### 103. Protect All Sheets in a Workbook

```
Sub CombineWorkbooks()
    Dim FilesToOpen
    Dim x As Integer
    FilesToOpen = Application.GetOpenFilename(FileFilter:="Microsoft Excel Files (*.xls; *.xlsx; *.xlsm), *.xls; *.xlsx; *.xlsm", MultiSelect:=True, Title:="Files to Merge")    If TypeName(FilesToOpen) = "Boolean" Then Exit Sub
    x = 1
    While x <= UBound(FilesToOpen)
        Workbooks.Open Filename:=FilesToOpen(x)
        Sheets().Move After:=ThisWorkbook.Sheets(ThisWorkbook.Sheets.Count)
        x = x + 1
    Wend
End Sub
```

#### 104. Combine Multiple Excel Files Into One Workbook

```
Sub ProtectSheets()
    Dim ws As Worksheet
    For Each ws In ThisWorkbook.Sheets
        ws.Protect Password:="password"
    Next ws
End Sub
```

#### 105. Send an Email via Outlook

```
Sub SendEmail()
    Dim OutApp As Object
    Dim OutMail As Object
    Set OutApp = CreateObject("Outlook.Application")
    Set OutMail = OutApp.CreateItem(0)    With OutMail
        .To = "recipient@example.com"
        .CC = ""
        .BCC = ""
        .Subject = "This is the Subject Line"
        .Body = "Hello World!"
        .Send
    End With    Set OutMail = Nothing
    Set OutApp = Nothing
End Sub
```

#### 106. Insert Multiple Rows Between Each Row in a Worksheet

```
Sub InsertRows()
    Dim i As Long
    For i = ThisWorkbook.Sheets("Sheet1").UsedRange.Rows.Count To 1 Step -1
        ThisWorkbook.Sheets("Sheet1").Rows(i + 1).Resize(2).Insert
    Next i
End Sub
```

#### 107. Automatically Save a Backup Copy of a Workbook

```
Sub SaveBackup()
    Dim backupPath As String
    backupPath = "C:\Backup\MyWorkbook_" & Format(Now(), "yyyymmdd_hhmmss") & ".xlsm"
    ThisWorkbook.SaveCopyAs backupPath
End Sub
```

#### 108. Delete All Charts in a Worksheet

```
Sub DeleteCharts()
    Dim cht As ChartObject
    For Each cht In ActiveSheet.ChartObjects
        cht.Delete
    Next cht
End Sub
```

#### 109. Automatically Close Workbook After Inactivity

```
Sub AutoClose()
    Dim countDown As Date
    countDown = Now + TimeValue("00:10:00") ' Set timer for 10 minutes
    Do Until Now >= countDown
        If Not Application.Interactive Then Exit Sub
        DoEvents
    Loop
    ThisWorkbook.Close SaveChanges:=False
End Sub
```

#### 110. Export Each Worksheet to a New Workbook

```
Sub ExportSheetsToWorkbooks()
    Dim ws As Worksheet
    For Each ws In ThisWorkbook.Worksheets
        ws.Copy
        ActiveWorkbook.SaveAs "C:\ExportedSheets\" & ws.Name & ".xlsx"
        ActiveWorkbook.Close False
    Next ws
End Sub
```

#### 111. Create a Directory from VBA

```
Sub CreateDirectory()
    Dim path As String
    path = "C:\NewFolder"
    If Not Dir(path, vbDirectory) <> "" Then
        MkDir path
    End If
End Sub
```

#### 112. Convert Numbers to Words (Functions)

```
Function NumberToWords(ByVal MyNumber)
    Dim Units As String, Teens As String, Tens As String
    Dim Result As String
    ' Arrays for converting number to words
    Units = "|One|Two|Three|Four|Five|Six|Seven|Eight|Nine"
    Teens = "|Eleven|Twelve|Thirteen|Fourteen|Fifteen|Sixteen|Seventeen|Eighteen|Nineteen"
    Tens = "|Ten|Twenty|Thirty|Forty|Fifty|Sixty|Seventy|Eighty|Ninety"
    ' Logic to convert number to words goes here
    ' Return the result as a string
    Result = "Logic not implemented"
    NumberToWords = Result
End Sub
```

#### 113. Add a Watermark to a Worksheet

```
Sub AddWatermark()
    ActiveSheet.Shapes.AddTextEffect(msoTextEffect1, "Confidential", "Arial", 50, msoFalse, msoFalse, 100, 100).Select
    With Selection.ShapeRange.Fill
        .Visible = msoTrue
        .ForeColor.RGB = RGB(217, 217, 217)
        .Transparency = 0.5
    End With
End Sub
```

#### 114. Sort Data in a Worksheet Automatically

```
Sub AutoSort()
    With ThisWorkbook.Sheets("Sheet1").Range("A1:D100")
        .Sort Key1:=.Cells(1, 1), Order1:=xlAscending, Header:=xlYes
    End With
End Sub
```

#### 115. Print All Workbooks in a Folder

```
Sub PrintAllWorkbooks()
    Dim folderPath As String
    Dim filename As String
    folderPath = "C:\MyFolder\"
    filename = Dir(folderPath & "*.xls*")
    Do While filename <> ""
        Workbooks.Open Filename:=folderPath & filename
        ActiveWorkbook.PrintOut Copies:=1
        ActiveWorkbook.Close False
        filename = Dir()
    Loop
End Sub
```

#### 116. Highlight Cells That Contain Formulas

```
Sub HighlightFormulas()
    Dim cell As Range
    For Each cell In ActiveSheet.UsedRange
        If cell.HasFormula Then
            cell.Interior.Color = RGB(255, 255, 0)
        End If
    Next cell
End Sub
```

#### More Codes and Example

* [Create a User Defined Function \[UDF\] in Excel using VBA](https://excelchamps.com/vba/user-defined-function/)
* [VBA Interview Questions](https://excelchamps.com/vba/interview-questions/)
* [Add a Comment in a VBA Code (Macro)](https://excelchamps.com/vba/comment/)
* [Add a Line Break in a VBA Code (Single Line into Several Lines)](https://excelchamps.com/vba/line-break/)
* [Add a New Line (Carriage Return) in a String in VBA](https://excelchamps.com/vba/new-line/)
* [Record a Macro in Excel](https://excelchamps.com/vba/record-macro/)
* [VBA Exit Sub Statement](https://excelchamps.com/vba/exit-sub/)
* [VBA Immediate Window (Debug.Print)](https://excelchamps.com/vba/immediate-window-debug-print/)
* [VBA Module](https://excelchamps.com/vba/module/)
* [VBA Objects](https://excelchamps.com/vba/objects/)
* [VBA With](https://excelchamps.com/vba/with/)
* [Add Developer Tab on Excel Ribbon | Windows + Mac](https://excelchamps.com/vba/add-developer-tab/)
* [Count Rows using VBA in Excel](https://excelchamps.com/vba/rows-count/)
* [Excel VBA Font (Color, Size, Type, and Bold)](https://excelchamps.com/vba/font/)
* [Excel VBA Hide and Unhide a Column or a Row](https://excelchamps.com/vba/hide-unhide-column-row/)
* [Excel VBA Range – Working with Range and Cells in VBA](https://excelchamps.com/vba/range/)
* [Apply Borders on a Cell using VBA in Excel](https://excelchamps.com/vba/borders/)
* [Find Last Row, Column, and Cell using VBA in Excel](https://excelchamps.com/vba/find-last-row-column-cell/)
* [Insert a Row using VBA in Excel](https://excelchamps.com/vba/insert-row/)
* [Merge Cells in Excel using a VBA Code](https://excelchamps.com/vba/merge/)
* [Select a Range/Cell using VBA in Excel](https://excelchamps.com/vba/select-range/)
* [SELECT ALL the Cells in a Worksheet using a VBA Code](https://excelchamps.com/vba/select-all/)
* [ActiveCell in VBA in Excel](https://excelchamps.com/vba/active-cell/)
* [Special Cells Method in VBA in Excel](https://excelchamps.com/vba/special-cells/)
* [UsedRange Property in VBA in Excel](https://excelchamps.com/vba/usedrange/)
* [VBA AutoFit (Rows, Column, or the Entire Worksheet)](https://excelchamps.com/vba/autofit/)
* [VBA ClearContents (from a Cell, Range, or Entire Worksheet)](https://excelchamps.com/vba/clear-contents/)
* [VBA Copy Range to Another Sheet + Workbook](https://excelchamps.com/vba/copy-cell-to-new-worksheet/)
* [VBA Enter Value in a Cell (Set, Get and Change)](https://excelchamps.com/vba/cell-value/)
* [VBA Insert Column (Single and Multiple)](https://excelchamps.com/vba/insert-column/)
* [VBA Named Range | (Static + from Selection + Dynamic)](https://excelchamps.com/vba/named-range/)
* [VBA Range Offset](https://excelchamps.com/vba/range-offset/)
* [VBA Sort Range | (Descending, Multiple Columns, Sort Orientation](https://excelchamps.com/vba/sort-range/)
* [VBA Wrap Text (Cell, Range, and Entire Worksheet)](https://excelchamps.com/vba/wrap-text/)
* [Extract Hyperlink Address (URL) VBA](https://excelchamps.com/vba/extract-hyperlink/)
* [CLEAR an Entire Sheet using VBA in Excel](https://excelchamps.com/vba/clear-sheet/)
* [Copy and Move a Sheet in Excel using VBA](https://excelchamps.com/vba/copy-sheet/)
* [COUNT Sheets using VBA in Excel](https://excelchamps.com/vba/count-sheets/)
* [DELETE a SHEET using VBA in Excel](https://excelchamps.com/vba/delete-sheet/)
* [Hide & Unhide a Sheet using VBA in Excel](https://excelchamps.com/vba/hide-sheet/)
* [PROTECT and UNPROTECT a Sheet using VBA in Excel](https://excelchamps.com/vba/protect-sheet/)
* [RENAME a Sheet using VBA in Excel](https://excelchamps.com/vba/rename-sheet/)
* [Write a VBA Code to Create a New Sheet in Excel (Macro)](https://excelchamps.com/vba/add-new-sheet/)
* [VBA Worksheet Object -Working with Excel Worksheet in VBA](https://excelchamps.com/vba/objects/worksheet/)
* [Activate a Sheet using VBA](https://excelchamps.com/vba/activate-sheet/)
* [Copy an Excel File (Workbook) using VBA – Macro Code](https://excelchamps.com/vba/copy-excel-file/)
* [VBA Activate Workbook (Excel File)](https://excelchamps.com/vba/activate-workbook/)
* [VBA Close Workbook (Excel File)](https://excelchamps.com/vba/close-workbook/)
* [VBA Combine Workbooks (Excel Files)](https://excelchamps.com/vba/combine-workbooks/)
* [VBA Create New Workbook (Excel File)](https://excelchamps.com/vba/create-workbook/)
* [VBA Delete Workbook (Excel File)](https://excelchamps.com/vba/delete-file/)
* [VBA Open Workbook (Excel File)](https://excelchamps.com/vba/open-workbook/)
* [VBA Protect/Unprotect Workbook (Excel File)](https://excelchamps.com/vba/protect-workbook/)
* [VBA Rename Workbook (Excel File)](https://excelchamps.com/vba/rename-workbook/)
* [VBA Save Workbook (Excel File)](https://excelchamps.com/vba/save-workbook/)
* [VBA ThisWorkbook (Current Excel File)](https://excelchamps.com/vba/this-workbook/)
* [VBA Workbook – A Guide to Work with Workbooks in VBA](https://excelchamps.com/vba/objects/workbook/)
* [Declare Global Variable (Public) in VBA](https://excelchamps.com/vba/global-variable/)
* [Use a Range or a Cell as a Variable in VBA](https://excelchamps.com/vba/range-variable/)
* [Option Explicit Statement in VBA](https://excelchamps.com/vba/option-explicit/)
* [Variable in a Message Box](https://excelchamps.com/vba/variable-message-box/)
* [VBA Constants](https://excelchamps.com/vba/constants/)
* [VBA Dim Statement](https://excelchamps.com/vba/dim/)
* [VBA Variables (Declare, Data Types, and Scope)](https://excelchamps.com/vba/variables/)
* [VBA Add New Value to the Array](https://excelchamps.com/vba/arrays/add-new-value-array/)
* [VBA Array](https://excelchamps.com/vba/arrays/)
* [VBA Array Length (Size)](https://excelchamps.com/vba/arrays/array-size/)
* [VBA Array with Strings](https://excelchamps.com/vba/arrays/array-with-strings/)
* [VBA Clear Array (Erase)](https://excelchamps.com/vba/arrays/clear-array/)
* [VBA Dynamic Array](https://excelchamps.com/vba/arrays/dynamic-array/)
* [VBA Loop Through an Array](https://excelchamps.com/vba/arrays/vba-loop-array/)
* [VBA Multi-Dimensional Array](https://excelchamps.com/vba/arrays/multi-dimensional-array/)
* [VBA Range to an Array](https://excelchamps.com/vba/arrays/range-to-an-array/)
* [VBA Search for a Value in an Array](https://excelchamps.com/vba/arrays/search-value-array/)
* [VBA Sort Array](https://excelchamps.com/vba/arrays/sort-array/)
* [Average Values in Excel using VBA](https://excelchamps.com/vba/average/)
* [Get Today’s Date and Current Time using VBA](https://excelchamps.com/vba/todays-date-current-time/)
* [Sum Values in Excel using VBA](https://excelchamps.com/vba/sum/)
* [Match Function in VBA](https://excelchamps.com/vba/match/)
* [MOD in VBA](https://excelchamps.com/vba/mod/)
* [Random Number](https://excelchamps.com/vba/random-number/)
* [VBA Calculate (Cell, Range, Row, & Workbook)](https://excelchamps.com/vba/calculate/)
* [VBA Concatenate](https://excelchamps.com/vba/concatenate/)
* [VBA Worksheet Function (Use Excel Functions in a Macro)](https://excelchamps.com/vba/worksheet-function/)
* [VBA Check IF a Sheet Exists](https://excelchamps.com/vba/check-sheet-exists/)
* [VBA Check IF a Cell is Empty + Multiple Cells](https://excelchamps.com/vba/check-empty-cell/)
* [VBA Check IF a Workbook Exists in a Folder (Excel File)](https://excelchamps.com/vba/check-if-workbook-exists/)
* [VBA Check IF a Workbook is Open (Excel File)](https://excelchamps.com/vba/check-workbook-open/)
* [VBA Exit IF](https://excelchamps.com/vba/exit-if/)
* [VBA IF – IF Then Else Statement](https://excelchamps.com/vba/if/)
* [VBA IF And (Test Multiple Conditions)](https://excelchamps.com/vba/if-and/)
* [VBA IF Not](https://excelchamps.com/vba/if-not/)
* [VBA IF OR (Test Multiple Conditions)](https://excelchamps.com/vba/if-or/)
* [VBA Nested IF](https://excelchamps.com/vba/nested-if/)
* [VBA Select Case](https://excelchamps.com/vba/select-case/)
* [VBA Automation Error (Error 440)](https://excelchamps.com/vba/automation-error-440/)
* [VBA Error 400](https://excelchamps.com/vba/error-400/)
* [VBA ERROR Handling](https://excelchamps.com/vba/error-handling/)
* [VBA Invalid Procedure Call Or Argument Error (Error 5)](https://excelchamps.com/vba/invalid-procedure-call-or-argument-error-5/)
* [VBA Object Doesn’t Support this Property or Method Error (Error 438)](https://excelchamps.com/vba/object-doesnt-support-this-property-or-method-error-438/)
* [VBA Object Required Error (Error 424)](https://excelchamps.com/vba/object-required-error-424/)
* [VBA Out of Memory Error (Error 7)](https://excelchamps.com/vba/out-of-memory-error-7/)
* [VBA Overflow Error (Error 6)](https://excelchamps.com/vba/overflow-error-6/)
* [VBA Runtime Error (Error 1004)](https://excelchamps.com/vba/runtime-error-1004/)
* [VBA Subscript Out of Range Runtime Error (Error 9)](https://excelchamps.com/vba/subscript-out-of-range-error-9/)
* [VBA Type Mismatch Error (Error 13)](https://excelchamps.com/vba/type-mismatch-error-13/)
* [Excel VBA Do While Loop and (Do Loop While) – A Guide](https://excelchamps.com/vba/do-while/)
* [Loop Through All the Sheets using VBA in Excel](https://excelchamps.com/vba/loop-sheets/)
* [Loop Through a Range using VBA (Columns, Row, and UsedRange)](https://excelchamps.com/vba/loop-through-range/)
* [VBA FOR LOOP (For Next, For Each) – The Guide + Examples](https://excelchamps.com/vba/for-loop/)
* [VBA GoTo Statement](https://excelchamps.com/vba/goto/)
* [VBA Loops (Beginner to Advanced) – A Guide](https://excelchamps.com/vba/loops/)
* [Input Box in VBA](https://excelchamps.com/vba/input-box/)
* [VBA Create and Write to a Text File](https://excelchamps.com/vba/text-files/)
* [VBA ScreenUpdating](https://excelchamps.com/vba/screen-updating/)
* [VBA Status Bar (Hide, Show, and Progress)](https://excelchamps.com/vba/status-bar/)
* [VBA Wait and Sleep Commands to Pause and Delay](https://excelchamps.com/vba/wait-sleep/)
* [Save an Excel Macro-Enabled Workbook (.xlsm File Type)](https://excelchamps.com/vba/macro-enabled-workbook/)
* [Search on Google using a VBA](https://excelchamps.com/vba/search-google/)
