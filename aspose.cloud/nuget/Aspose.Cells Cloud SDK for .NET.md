# .NET Cloud SDK for Spreadsheet Processing in the Cloud

This Cloud SDK enhances your C#, ASP.NET, & other .NET cloud-based apps to [process & manipulate Microsoft Excel spreadsheets](https://products.aspose.cloud/cells/net) in the cloud, without MS Office.

## Spreadsheet Processing Features

- Add, update or delete charts, worksheet pictures, shapes, hyperlinks & validations.
- Add or remove cells area for conditional formatting, or OleObjects from Excel worksheets.
- Insert or delete, horizontal or vertical page breaks
- Add ListObject at a specific place within an Excel file & convert them to a range of cells.
- Delete specific or all ListObjects in a worksheet or summarize its data with pivot table.
- Apply custom criteria to list filters of various types.
- Get, update, show or hide chart legend & titles.
- Manipulate page setup, header & footer.
- Create, update, fetch or delete document properties.
- Fetch the required shape from worksheet.
- Load & Process Excel Spreadsheets via Cloud SDK.
- Cloud SDK to Read & Process Excel Worksheets.
- Leverage the Power of Pivot Tables & Ranges.

## New Features & Enhancements in Version 20.6

- Ability to support the text water marker.
- Support to convert images in `get` workbook API.
- Upgrade `Dynabic.Billing` for Aspose.Cells Cloud.
- Enhancement for `Cells` object operating in `Task` API.

For the detailed notes, please visit [Aspose.Cells Cloud 20.6 Release Notes](https://docs.aspose.cloud/display/cellscloud/Aspose.Cells+Cloud+20.6+Release+Notes).

## Read & Write Spreadsheet Formats

**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM\
**OpenOffice:** ODS\
**SpreadsheetML:** XML\
**Text:** CSV, TSV, TXT (TabDelimited)\
**Web:** HTML, MHTML

## Save Spreadsheet As

DIF, PDF, XPS, TIFF, SVG, MD (Markdown)

## Read Spreadsheet Formats

SXC, FODS

## Getting Started with Aspose.Cells Cloud SDK for .NET

You do not need to install anything to get started with Aspose.Cells Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.Cells-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.Cells assembly in your project. If you already have Aspose.Cells Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.Cells-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) for other common usage scenarios.

## Using C# to Add a New Worksheet to an Excel File

The following code snippet demonstrates how to add a new worksheet to a Microsoft Excel document using C# code:

```csharp
CellsWorksheetsApi instance = new CellsWorksheetsApi(GetConfiguration());
string name = "Input.xlsx";
string sheetName = "Sheet1";
int? position = 1;
string sheettype = "VB";
string folder = null;
UpdateDataFile(folder, name);
var response = instance.CellsWorksheetsPutAddNewWorksheet(name, sheetName, position, sheettype, folder);
```

## Using C# to Convert an Excel File to another File Format

The following code example elaborates how you can use C# code to convert an Excel document to another file format in the cloud:

```csharp
// Upload source file to aspose cloud storage
storageApi.PutCreate(inputfileName, "", "", System.IO.File.ReadAllBytes(Common.GetDataDir() + inputfileName));

// Invoke Aspose.Cells Cloud SDK API to convert excel workbook to different format
SaveResponse apiResponse = cellsApi.PostDocumentSaveAs(inputfileName, outputFileName, isAutoFitRows, isAutoFitColumns, storage, folder, body);
```

[Product Page](https://products.aspose.cloud/cells/net) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [Demo](https://products.aspose.app/cells/family) | [API Reference](https://apireference.aspose.cloud/cells/) | [Examples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
