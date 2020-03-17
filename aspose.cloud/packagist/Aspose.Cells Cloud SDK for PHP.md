# PHP REST API for Spreadsheet Processing in Cloud

This Cloud SDK enhances your PHP cloud-based apps to [process & manipulate Microsoft Excel spreadsheets](https://products.aspose.cloud/cells/php) in the cloud, without MS Office.

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

## Enhancements in Version 20.2.0

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

## Getting Started with Aspose.Cells Cloud SDK for PHP

This repository contains Aspose.Cells Cloud SDK for PHP source code. To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) (free registration of [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) is required for this). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

Please check the [GitHub Repository](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-php) for the source code and examples.

## How to use the SDK

The complete source code is available in this repository folder. You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/cells-sdk-php) (recommended). For more details, please visit our [documentation website](https://docs.aspose.cloud/display/cellscloud/Available+SDKs).

## Installation via Composer

Aspose.Cells Cloud SDK for PHP is available on `Packagist` as the `cells-sdk-php` package. Run the following command:

```console
composer require aspose/cells-sdk-php
```

To use the SDK, use Composer's [autoload](https://getcomposer.org/doc/00-intro.md#autoloading):

```php
require_once('vendor/autoload.php');
```

## Sample usage

```php
$saveAsAPI = new CellsApi("appsid","appkey");
$name ='Book1.xlsx';
$saveOptions = null;
$newfilename = "newbook.xlsx";
$isAutoFitRows= 'true';
$isAutoFitColumns= 'true';
$folder = "Temp";
$result = $saveAsAPI->cellsSaveAsPostDocumentSaveAs($name, $saveOptions, $newfilename,$isAutoFitRows, $isAutoFitColumns,$folder);
```

## Tests

[Tests](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/test/Api) contain various examples of using the SDK.

## Licensing

All Aspose.Cells Cloud SDKs are licensed under [MIT License](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/cells/php) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [API Reference](https://apireference.aspose.cloud/cells/) | [Code Samples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
