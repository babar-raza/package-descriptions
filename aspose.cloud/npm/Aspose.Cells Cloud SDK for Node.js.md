This Cloud SDK enhances your Node.js cloud-based apps to process & manipulate Microsoft Excel spreadsheets in the cloud, without MS Office.

It enables your Node.js cloud-based programs to process workbooks, worksheets, spreadsheets, columns, rows, and individual cells. You can also work with Microsoft Excel OleObjects, pivot tables, ListObjects, shapes, tasks, hyperlinks and comments from within your your cloud-based applications. Aspose.Cells Cloud SDK for Node.js also lets you apply auto-filtering or perform conditional formatting on the spreadsheet level. Aspose.Cells Cloud SDK for Node.js is a wrapper around Aspose.Cells REST API and is available for use under an MIT license.

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

## Read & Write Spreadsheet Formats

**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**OpenOffice:** ODS
**SpreadsheetML:** XML
**Text:** CSV, TSV, TXT (TabDelimited)
**Web:** HTML, MHTML

## Save Spreadsheet As

DIF, PDF, XPS, TIFF, SVG, MD (Markdown)

## Read Spreadsheet Formats

SXC, FODS

## Platform Independence

Aspose.Cells Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.Cells Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.Cells for Cloud via NPM, please execute from the command line, `npm install aspose-cells-cloud-node --save`.

## Hide Worksheet Columns via Node.js

```js
const { CellsApi, Cells_PostHideWorksheetColumnsRequest } = require("asposecellscloud");

AppSid = ""
AppKey = ""
cellsApi = new CellsApi(AppSid, AppKey);
filename = "Book1.xlsx"

var req = new Cells_PostHideWorksheetColumnsRequest();
req.name = filename;
req.sheetName = "Sheet1";
req.startColumn = 1;
req.totalColumns = 2;
req.folder = "";

return cellsApi.cellsPostHideWorksheetColumns(req)
    .then((result) => {
        console.log(result)
    });
```

## Merge Worksheets in the Cloud via Node.js

```js
const { CellsApi, Cells_PostWorksheetMergeRequest } = require("asposecellscloud");

AppSid = ""
AppKey = ""
cellsApi = new CellsApi(AppSid, AppKey);
filename = "Book1.xlsx"

var req = new Cells_PostWorksheetMergeRequest();
req.name = filename;
req.sheetName = "Sheet1";
req.startRow = 1;
req.startColumn = 1;
req.totalRows = 4;
req.totalColumns = 4;
req.folder = "";

return cellsApi.cellsPostWorksheetMerge(req)
  .then((result) => {
    console.log(result)
  });
```

[Product Page](https://products.aspose.cloud/cells/net) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [API Reference](https://apireference.aspose.cloud/cells/) | [Code Samples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)