Node.js Cloud SDK wraps Aspose.Cells REST API so you could seamlessly integrate Excel® file generation, manipulation, conversion & processing features into your own Node.js applications.

# Process Excel® Files in the Cloud with Node.js

[Aspose.Cells Cloud SDK for Node.js](https://products.aspose.cloud/cells/nodejs) allows developers to create, edit, process & convert Excel spreadsheets in the Cloud. The Excel Cloud SDK gets its functionality from Aspose.Cells Cloud API, allowing your Node.js apps to work with all Excel file formats and features including worksheet & cell management, conditional formatting, auto-filters, auto-shapes, charts, OleObjects, page breaks, ListObjects, Pivot Tables, charts and much more. 

## Excel File Processing Features

- Create Excel files from scratch using the API. 
- Load, process & convert spreadsheets via Cloud SDK.
- Add, update or delete worksheet, charts, pictures, shapes, hyperlinks & validations.
- Add or remove cells area for conditional formatting from Excel worksheets.
- Insert or delete, horizontal or vertical page breaks.
- Add ListObject or convert ListObjects to a range of cells.
- Summarize data with Pivot Tables & charts.
- Apply custom criteria to list filters of various types.
- Get, update, show or hide chart legend & titles.
- Manipulate page setup, header & footer.
- Create, update, fetch or delete document properties.
- Fetch the required shape from worksheet.
- Leverage the Power of Pivot Tables & ranges.

## New Features in Version 20.3

- Export area or page of worksheet to JPEG.
- Add background to the workbook.

For the detailed notes, please visit [Aspose.Cells Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/cellscloud/Aspose.Cells+Cloud+20.3+Release+Notes).

## Read & Write Spreadsheet Formats

**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**OpenOffice:** ODS
**SpreadsheetML:** XML
**Text:** CSV, TSV, TXT (TabDelimited)
**Web:** HTML, MHTML

## Save Spreadsheet As

DIF, PDF, XPS, TIFF, SVG, MD (Markdown)

## Read File Formats

SXC, FODS

## Storage API Support

Since version 19.9, SDK includes support of storage operations for better user experience and unification, so now there's no need to use 2 different SDKs!

It gives you an ability to:

- Upload, download, copy, move and delete files, including versions handling (if you are using Cloud storage that supports this feature - true by default).
- Create, copy, move and delete folders.
- Copy and move files and folders across separate storages in scope of a single operation.
- Check if certain file, folder or storage exists.

## Getting Started with Aspose.Cells Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install asposecellscloud --save` from the command line to install Aspose.Cells Cloud SDK for Node.js via NPM.

The complete source code is available at [GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

## Convert Excel to PDF via Node.js
```js
var fs = require('fs');
var path = require('path');
var assert = require('assert');
const localPath = "../TestData/";
describe('cellsWorkbookPutConvertWorkbook', function() {
  it('should call cellsWorkbookPutConvertWorkbook successfully', function() {
    const cellsApi =new api.CellsApi(AppSid, AppKey);
    const filename = "Book1.xlsx";
    var data =fs.createReadStream(localPath  + filename);
    var req = new model.UploadFileRequest();
    req.path = "Temp/" + filename;
    req.file = data;

    return cellsApi.uploadFile(req)
      .then(() => {
        var req = new model.CellsWorkbook_PutConvertWorkbookRequest({
          workbook : fs.createReadStream(localPath  + filename),
          format : "pdf",
        });

        return cellsApi.cellsWorkbookPutConvertWorkbook(req)
          .then((result) => {
            expect(result.body.toString().length).to.greaterThan(0);
          });
      });
  });
});
```

## Hide Excel Columns via Node.js

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

[Product Page](https://products.aspose.cloud/cells/nodejs) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [Live Demo](https://products.aspose.app/cells/family) | [API Reference](https://apireference.aspose.cloud/cells/) | [Examples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)

