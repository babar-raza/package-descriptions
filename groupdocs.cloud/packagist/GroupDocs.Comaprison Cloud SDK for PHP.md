# Document Comparison PHP Cloud REST API

This cloud REST API enhances your PHP cloud apps to [compare two documents](https://products.groupdocs.cloud/comparison/php), fetch, accept or reject the changes. Supports 90+ file formats.

## Cloud Document Comparison Features

- Compare two documents and fetch changes.
- Fetch document changes based on change category, such as, numeric only.
- Accept or reject the changes that come up after document comparison.
- Get the image stream of resultant document via `JsonRequest` object.
- Save the resultant document to streams as set of images.
- Get the resultant document path.
- Add summary page to resultant document after comparison.
- Show deleted components in the resultant document.
- Detect style changes.
- Get or set password to the the resultant document.

## New Features in Version 19.5

- This is the first release of a completely new version of the API `GroupDocs.Comparison.Cloud v2.0`.
- `V2` provides much simpler and intuitive API as compared to `V1`.
- `V2` includes Storage and File API which enables you to manage storage and files.
- Internal cloud solution is based on the modern micro-service architecture.

For the detailed notes, please visit [GroupDocs.Comparison Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/comparisoncloud/release-notes/2019/groupdocs-comparison-cloud-19-5-release-notes/).

## Supported Document Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX, XLTM, XLTX, ODS, OTS, CSV, TSV
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POTM, POTX, ODP, OTP
**Microsoft Visio:** VDW, VDX, VSD, VSDML, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Microsoft Project:** MPP, MPT
**Microsoft OneNote:** ONE
**Email:** EML, EMLX, MSG, OST, PST
**Adobe Photoshop:** PSD
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**eBook:** EPUB, MOBI
**Image:** BMP, CGM, DCM, DJVU, DNG, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PNG, SVG, TIF, TIFF, WEBP
**Markup:** HTML, MHT, MHTML, XML
**Portable:** PDF, TEX, XPS
**Metafile:** EMF, WMF
**Other:** PCL, PS

## Dependencies

- PHP 5.5 or later

## Authorization

To use SDK you need AppSID and AppKey authorization keys. You can get your AppSID and AppKey at [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## Installation & Usage

### Composer

The package is available at [Packagist](https://dashboard.groupdocs.cloud) and it can be installed via [Composer](http://getcomposer.org/) by executing following command:

`composer require groupdocscloud/groupdocs-comparison-cloud`

Or you can install SDK via [Composer](http://getcomposer.org/) directly from this repository, add the following to `composer.json`:

```php
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-php.git"
    }
  ],
  "require": {
    "groupdocscloud/groupdocs-comparison-cloud": "*"
  }
}
```

Then run `composer install`.

### Manual Installation

Clone or download this repository, then run `composer install` in the root directory to install dependencies and include `autoload.php` into your code file:

```php
require_once('/path/to/groupdocs-comparison-cloud-php/vendor/autoload.php');
```

## Tests

To run the unit tests set your AppSID and AppKey in [json.config](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-php/blob/master/tests/GroupDocs/Comparison/config.json) and execute following commands:

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
$configuration = new GroupDocs\Comparison\Configuration();
$configuration->setAppSid("XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX");
$configuration->setAppKey("XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX");

$infoApi = new GroupDocs\Comparison\InfoApi($configuration);

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

## Compare Multiple Documents using PHP REST API

```php
include(dirname(__DIR__) . '\CommonUtils.php');

$apiInstance = CommonUtils::GetCompareApiInstance();

$sourceFileInfo = new GroupDocs\Comparison\Model\FileInfo();
$sourceFileInfo->setFilePath("comparisondocs\\source_protected.docx");
$sourceFileInfo->setPassword("1231");

// First target document
$targetFileInfo1 = new GroupDocs\Comparison\Model\FileInfo();
$targetFileInfo1->setFilePath("comparisondocs\\target_protected.docx");
$targetFileInfo1->setPassword("5784");

// Second target document
$targetFileInfo2 = new GroupDocs\Comparison\Model\FileInfo();
$targetFileInfo2->setFilePath("comparisondocs\\target_2_protected.docx");
$targetFileInfo2->setPassword("5784");

$options = new GroupDocs\Comparison\Model\Options();  
$options->setSourceFile($sourceFileInfo);
$options->setTargetFiles([$targetFileInfo1, $targetFileInfo2]);
$options->setOutputPath("comparisondocs\\result_multi_protected.docx");

$settings = new GroupDocs\Comparison\Model\Settings();  
$settings->setGenerateSummaryPage(true);
$settings->setShowDeletedContent(true);
$settings->setStyleChangeDetection(true);
$settings->setUseFramesForDelInsElements(false);
$settings->setMetaData(null);
$settings->setDetailLevel("Low");
$settings->setDiagramMasterSetting(null);
$settings->setCalculateComponentCoordinates(false);
$settings->setCloneMetadata("Default");
$settings->setMarkDeletedInsertedContentDeep(false);
$settings->setPassword("1111");
$settings->setPasswordSaveOption("User");

$deletedItemsStyle = new GroupDocs\Comparison\Model\ItemsStyle();
$deletedItemsStyle->setBeginSeparatorString("");
$deletedItemsStyle->setEndSeparatorString("");
$deletedItemsStyle->setFontColor("16711680");
$deletedItemsStyle->setHighlightColor("16711680");
$deletedItemsStyle->setBold(false);
$deletedItemsStyle->setItalic(false);
$deletedItemsStyle->setStrikeThrough(false);
$settings->setDeletedItemsStyle($deletedItemsStyle);

$insertedItemsStyle = new GroupDocs\Comparison\Model\ItemsStyle();
$insertedItemsStyle->setBeginSeparatorString("");
$insertedItemsStyle->setEndSeparatorString("");
$insertedItemsStyle->setFontColor("255");
$insertedItemsStyle->setHighlightColor("255");
$insertedItemsStyle->setBold(false);
$insertedItemsStyle->setItalic(false);
$insertedItemsStyle->setStrikeThrough(false);
$settings->setInsertedItemsStyle($insertedItemsStyle);
  
$styleChangedItemsStyle = new GroupDocs\Comparison\Model\ItemsStyle();
$styleChangedItemsStyle->setBeginSeparatorString("");
$styleChangedItemsStyle->setEndSeparatorString("");
$styleChangedItemsStyle->setFontColor("65280");
$styleChangedItemsStyle->setHighlightColor("65280");
$styleChangedItemsStyle->setBold(false);
$styleChangedItemsStyle->setItalic(false);
$styleChangedItemsStyle->setStrikeThrough(false);
$settings->setStyleChangedItemsStyle($styleChangedItemsStyle);

$options->setSettings($settings);

$request = new GroupDocs\Comparison\Model\Requests\comparisonsRequest($options);
$response = $apiInstance->comparisons($request);

echo "Expected response type is Link: ", $response->getHref();
```

## Licensing

GroupDocs.Comparison Cloud SDK for PHP is licensed under [MIT License](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-php/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/comparison/php) | [Documentation](https://wiki.groupdocs.cloud/comparisoncloud/) | [Live Demo](https://products.groupdocs.app/comparison/family) | [API Reference](https://apireference.groupdocs.cloud/comparison/) | [Code Samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-php) | [Blog](https://blog.groupdocs.cloud/category/comparison/) | [Free Support](https://forum.groupdocs.cloud/c/comparison) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
