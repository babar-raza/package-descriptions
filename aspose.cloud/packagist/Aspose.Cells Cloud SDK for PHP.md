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

## New Features in Version 20.3

- Support to export whole page of sheet or an area to `JPEG` format.
- Support to add workbook background.

## Enhancements in Version 20.3

- Update `Aspose.Cells.DLL` to 20.2.4 for Aspose.Cells Cloud.
- Enhancements in creating and splitting workbooks.

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

The complete source code is available at the [GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php). You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/cells-sdk-php) (recommended). For more details, please visit our [documentation website](https://docs.aspose.cloud/display/cellscloud/Available+SDKs).

## Prerequisites

To use Aspose Cells Cloud SDK you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Installation via Composer

*cells-sdk-php* is available on [Packagist](https://packagist.org/packages/aspose/cells-sdk-php) as the `cells-sdk-php` package. Run the following command:

```console
composer require aspose/cells-sdk-php
```

To use the SDK, use Composer's [autoload](https://getcomposer.org/doc/00-intro.md#autoloading):

```php
require_once('vendor/autoload.php');
```

## Using PHP Code to Import Data in Excel Worksheet

```php
require_once realpath(__DIR__ . '/..') . '/vendor/autoload.php';
require_once realpath(__DIR__ . '/..') . '/Utils.php';

use Aspose\Cells\CellsApi;
use Aspose\Cells\AsposeApp;

class Workbook {

    public $cells;

    public function __construct() {
        AsposeApp::$appSID = Utils::appSID;
        AsposeApp::$apiKey = Utils::apiKey;
        $this->cells = new CellsApi();
    }

    public function postImportDataCloudFile() {
        $options = array('{"BatchData":null,"DestinationWorksheet":"Sheet1","IsInsert":false,"ImportDataType":"BatchData","Source":{"FileSourceType":1,"FilePath":"Batch_data_json.txt"}}',
            '{"FirstRow":1,"FirstColumn":2,"IsVertical":true,"Data":null,"DestinationWorksheet":"Sheet1","IsInsert":true,"ImportDataType":"StringArray","Source":{"FileSourceType":1,"FilePath":"Array_string_json.txt"}}',
            '{"FirstRow":1,"FirstColumn":2,"IsVertical":true,"Data":null,"DestinationWorksheet":"Sheet1","IsInsert":true,"ImportDataType":"IntArray","Source":{"FileSourceType":1,"FilePath":"Array_int_json.txt"}}',
            '{"FirstRow":1,"FirstColumn":2,"IsVertical":true,"Data":null,"DestinationWorksheet":"Sheet1","IsInsert":true,"ImportDataType":"DoubleArray","Source":{"FileSourceType":1,"FilePath":"Array_double_json.txt"}}'
            );

        $dataFiles = array("Batch_data_json.txt", "Array_string_json.txt", "Array_int_json.txt", "Array_double_json.txt");

        foreach($options as $index=>$option) {
            // Upload file to Aspose Cloud Storage
            $name = "Book1.xlsx";
            Utils::uploadFile($name);
            $dataFile = $dataFiles[$index];
            Utils::uploadFile($dataFile);

            $body = $option;

            $result = $this->cells->PostImportDataCloudFile($name, $storage = null, $folder = null, $body);
            print_r($result);
        }
    }
}

$workbook = new Workbook();
$workbook->postImportDataCloudFile();
```

## Tests

[Tests](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/test/Api) contain various examples of using the SDK.

## Licensing

All Aspose.Cells Cloud SDKs are licensed under [MIT License](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/cells/php) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [Live Demo](https://products.aspose.app/cells/family) | [API Reference](https://apireference.aspose.cloud/cells/) | [Code Samples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
