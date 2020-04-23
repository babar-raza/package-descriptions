# Perl REST API for Spreadsheet Processing in Cloud

This Cloud SDK enhances your Perl cloud-based apps to [process & manipulate Microsoft Excel spreadsheets](https://products.aspose.cloud/cells/perl) in the cloud, without MS Office.

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

## New Features in Version 20.3

- Support to export area or page of sheet to JPEG.
- Support to add background for workbook.

For the detailed notes, please visit [Aspose.Cells Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/cellscloud/Aspose.Cells+Cloud+20.3+Release+Notes).

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

## How to use the SDK

The complete source code is available at the [GitHub repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl). For more details, please visit our [documentation website](https://docs.aspose.cloud/display/cellscloud/Available+SDKs).

## Prerequisites

To use Aspose.Cells Cloud SDK for Perl you need to register an account with [Aspose Cloud](https://www.aspose.cloud) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Installation & Usage

### Sample usage

```perl
@instance = AsposeCellsCloud::CellsApi.new("appsid","appkey")
 name = 'Book1.xlsx'
 text = 'test'
 folder = 'Temp'
 @instance.cells_workbook_post_workbooks_text_search(name, text, { :folder=>folder})
```

## Tests

[Tests](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/t) contain various examples of using the SDK.

## Licensing

All Aspose.Cells Cloud SDKs are licensed under [MIT License](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/cells/perl) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [Demo](https://products.aspose.app/cells/family) | [API Reference](https://apireference.aspose.cloud/cells/) | [Examples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
