# PHP Cloud REST API for Document Editing

Use this REST API to enhance your PHP apps to [edit documents, spreadsheets, presentations](https://products.groupdocs.cloud/editor/php) of 40+ file formats from within your cloud apps.

## Cloud Document Editor Features

- Edit word processing documents in flow or paged mode.
- Extract font information for a consistent look and feel of the edited documents.
- Support for the editing of multi-tabbed spreadsheets.
- Ability to specify the index of the currently edited worksheet.
- Works with DSV (Delimiter Separated Values) files.
- Specify the separator for the CSV and TSV files.
- Flexible conversion options for dates and numbers in TSV, CSV files.
- Optimize memory usage of large CSV, TSV files.
- Fix incorrect document structure of the XML files.
- Recognize email addresses and URIs in the XML files.
- Support for highlighting and formatting options for XML files.
- Ability to extract basic information about the document.
- Support to work with files and folders in the cloud.

## Supported File Formats

**Word Processing:** DOC, DOCX, DOCM, DOT, DOTM, DOTX, FlatOPC, ODT, OTT, RTF, WordML
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLTX, XLTM, XLSB, XLAM, SXC, SpreadsheetML, ODS, FODS, DIF, DSV, CSV, TSV
**Presentation:** PPT (95), PPT (97-2003), PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, POTM, ODP, OTP
**Markup:** HTML, XML
**Other:** TXT

## Platform Independence

GroupDocs.Editor Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Dependencies

- PHP 5.5 or later

## Authorization

To use SDK you need AppSID and AppKey authorization keys. You can get your AppSID and AppKey at [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## Installation & Usage

### Composer

The package is available at [Packagist](https://packagist.org/) and it can be installed via [Composer](http://getcomposer.org/) by executing following command:

`composer require groupdocscloud/groupdocs-editor-cloud`

Or you can install SDK via [Composer](http://getcomposer.org/) directly from this repository, add the following to `composer.json`:

```php
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-php.git"
    }
  ],
  "require": {
    "groupdocscloud/groupdocs-editor-cloud": "*"
  }
}
```

Then run `composer install`.

## Manual Installation

Clone or download this repository, then run `composer install` in the root directory to install dependencies and include `autoload.php` into your code file:

```php
require_once('/path/to/groupdocs-editor-cloud-php/vendor/autoload.php');
```

## Tests

To run the unit tests set your AppSID and AppKey in [json.config](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-php/blob/master/tests/GroupDocs/Editor/config.json) and execute following commands:

```php
php composer.phar install
./vendor/bin/phpunit
```

## Getting Started

Please follow the installation procedure and then run the following:

```php
<?php

require_once(__DIR__ . '/vendor/autoload.php');

//TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud (free registration is required).
$configuration = new GroupDocs\Editor\Configuration();
$configuration->setAppSid("XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX");
$configuration->setAppKey("XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX");

$infoApi = new GroupDocs\Editor\InfoApi($configuration); 

try {
    $response = $infoApi->getSupportedFileFormats();

    foreach ($response->getFormats() as $key => $format) {
        echo $format->getFileFormat() . " - " .  $format->getExtension(), "\n";
    }
} catch (Exception $e) {
    echo  "Something went wrong: ",  $e->getMessage(), "\n";
    PHP_EOL;
}

?>
```

## Use PHP REST API to Work with DOCX Files in Cloud

```php
use GroupDocs\Editor\Model;
use GroupDocs\Editor\Model\Requests;


$AppSid = ""; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$AppKey = ""; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
$configuration = new GroupDocs\Editor\Configuration();
$configuration->setAppSid($AppSid);
$configuration->setAppKey($AppKey);

$editApi = new GroupDocs\Editor\EditApi($configuration);
$fileApi = new GroupDocs\Editor\FileApi($configuration);

// The document already uploaded into the storage
// Load it into editable state
$fileInfo = new Model\FileInfo();
$fileInfo->setFilePath("WordProcessing/password-protected.docx");
$fileInfo->setPassword("password");
$loadOptions = new Model\WordProcessingLoadOptions();
$loadOptions->setFileInfo($fileInfo);
$loadOptions->setOutputPath("output");
$loadResult = $editApi->load(new Requests\loadRequest($loadOptions));

// Download html document
$htmlFile = $fileApi->downloadFile(new Requests\downloadFileRequest($loadResult->getHtmlPath()));
$html = file_get_contents($htmlFile->getRealPath());

// Edit something...
$html = str_replace("Sample test text", "Hello world", $html);

// Upload html back to storage
file_put_contents($htmlFile->getRealPath(), $html);
$uploadRequest = new Requests\uploadFileRequest($loadResult->getHtmlPath(), $htmlFile->getRealPath());
$fileApi->uploadFile($uploadRequest);

// Save html back to docx
$saveOptions = new Model\WordProcessingSaveOptions();
$saveOptions->setFileInfo($fileInfo);
$saveOptions->setOutputPath("output/edited.docx");
$saveOptions->setHtmlPath($loadResult->getHtmlPath());
$saveOptions->setResourcesPath($loadResult->getResourcesPath());
$saveResult = $editApi->save(new Requests\saveRequest($saveOptions));

// Done.
echo "Document edited: " . $saveResult->getPath();
```

## Licensing

GroupDocs.Editor Cloud SDK for PHP is licensed under [MIT License](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-php/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/editor/php) | [Documentation](https://wiki.groupdocs.cloud/editorcloud/) | [API Reference](https://apireference.groupdocs.cloud/editor/) | [Code Samples](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-php) | [Blog](https://blog.groupdocs.cloud/) | [Free Support](https://forum.groupdocs.cloud/c/editor) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
