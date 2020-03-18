# .NET REST API for Spreadsheet Processing in Cloud

This Cloud SDK enhances your Ruby cloud-based apps to [process & manipulate Microsoft Excel spreadsheets](https://products.aspose.cloud/cells/ruby) in the cloud, without MS Office.

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

## Enhancements in Version 20.2

- Automatically refresh authorization Token in SDK.

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

## Getting Started with Aspose.Cells Cloud SDK for Ruby

The complete source code is available at the [GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/aspose_cells_cloud) (recommended).

## Prerequisites

To use Aspose.Cells Cloud SDK for Ruby you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Installation

To install this package do the following:

Update your `Gemfile`

```console
gem 'aspose_cells_cloud', '~> 19.9'
```

or install directly

```console
gem install aspose_cells_cloud
```

## Sample usage

```ruby
@instance = AsposeCellsCloud::CellsApi.new("appsid","appkey")
 name = 'Book1.xlsx'
 text = 'test'
 folder = 'Temp'
 @instance.cells_workbook_post_workbooks_text_search(name, text, { :folder=>folder})
```

## Tests

[Tests](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/spec) contain various examples of using the SDK.

## Licensing

All Aspose.Cells Cloud SDKs are licensed under [MIT License](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/cells/ruby) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [API Reference](https://apireference.aspose.cloud/cells/) | [Code Samples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
