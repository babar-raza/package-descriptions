# PHP Cloud REST API for Document Conversion

This REST API allows your PHP cloud-based apps to [convert documents](https://products.groupdocs.cloud/conversion/php) of 50+ file formats from within your apps without any 3rd party tool.

## Cloud Document Conversion Features

- Specify document conversion settings.
- Specify page width & height while converting CAD diagrams.
- Choose specific CAD diagram layouts to be converted.
- Substitute specific fonts during cells document conversion.
- Convert specific cell range while converting to non-cell formats.
- Skip empty rows and columns when converting cells documents.
- Display or hide email header, "from", "to", "cc" & "bcc".
- Substitute specific fonts when converted some supported formats.
- Start converting from specified page number.
- Convert a specific number of pages from the specified page.
- Use PDF as an intermediary format while converting.
- Apply watermark during conversion process.

## New Features in Version 20.2

- **New Source Formats:** DIB, XLT, POT, XLAM, MPX, JPC, DWT, JPEG-LS.
- **New Target Formats:** WMF, EMF, XLAM.
- Supports encoding for source `CSV` and `TXT` documents.
- Supports `TimeZoneOffset` and `ConvertAttachments` for source Email documents.

## Enhancements in Version 20.2

- Improved quality of Diagram to Word document conversion.
- Converting multi-page `TIFF` to `PDF`.
- Improvement in `MPP` to `XLS` conversion.

For the detailed notes, please visit, [GroupDocs.Conversion Cloud 20.2 Release Notes](https://wiki.groupdocs.cloud/conversioncloud/release-notes/2020/groupdocs-conversion-cloud-20-2-release-notes/).

## Conversion File Formats

GroupDocs.Conversion Cloud SDK for .NET allows you to convert any of the following type of file formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLT, XLS2003, XLSB, XLSM, XLAM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX, POT
**Microsoft Visio:** VDW, VDX, VSD, VSDX, VSS, VST, VSX, VTX
**Microsoft Project:** MPP, MPT, MPX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**AutoCAD:** DWG, DWT, DXF
**Image:** BMP, GIF, ICO, JPEG, JPEG-LS, JPG, JPC, PNG, SVG, TIF, TIFF, DIB
**Email:** EML, EMLX, MSG
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML, MHT

to the following formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLS2003, XLSB, XLSM, XLAM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**Image:** BMP, GIF, ICO, JPEG, JPG, PNG, TIF, TIFF
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML
**Metafile:** WMF, EMF

## Dependencies

- PHP 5.5 or later

## Authorization

To use SDK you need AppSID and AppKey authorization keys. You can get your AppSID and AppKey at [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## Installation & Usage

### Composer

The package is available at [Packagist](https://dashboard.groupdocs.cloud) and it can be installed via [Composer](https://dashboard.groupdocs.cloud) by executing following command:

`composer require groupdocscloud/groupdocs-conversion-cloud`

Or you can install SDK via [Composer](https://dashboard.groupdocs.cloud) directly from this repository, add the following to `composer.json`:

```php
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-php.git"
    }
  ],
  "require": {
    "groupdocscloud/groupdocs-conversion-cloud": "*"
  }
}
```

Then run `composer install`.

### Manual Installation

Clone or download this repository, then run `composer install` in the root directory to install dependencies and include `autoload.php` into your code file:

```php
require_once('/path/to/groupdocs-conversion-cloud-php/vendor/autoload.php');
```

## Tests

To run the unit tests set your AppSID and AppKey in [json.config](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-php/blob/master/tests/GroupDocs/Conversion/config.json) and execute following commands:

```php
php composer.phar install
./vendor/bin/phpunit

Getting Started

Please follow the installation procedure and then run the following:

<?php

require_once(__DIR__ . '/vendor/autoload.php');

//TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud (free registration is required).
$configuration = new GroupDocs\Conversion\Configuration();
$configuration->setAppSid("XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX");
$configuration->setAppKey("XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX");

$api = new GroupDocs\Conversion\InfoApi($configuration); 

try {
    $request = new GroupDocs\Conversion\Model\Requests\GetSupportedConversionTypesRequest();
    $response = $api->getSupportedConversionTypes($request);

    foreach($response as $key => $format) {
          echo $format->getSourceFormat();
    }
} catch (Exception $e) {
    echo  "Something went wrong: ",  $e->getMessage(), "\n";
    PHP_EOL;
}

?>
```

## Use PHP REST API to Convert DOCX Document Format

```php
include(dirname(__DIR__) . '\CommonUtils.php');

$convertApi = CommonUtils::GetConvertApiInstance();

$settings = new GroupDocs\Conversion\Model\ConvertSettings();

$settings->setStorageName(CommonUtils::$MyStorage);
$settings->setFilePath("conversions\\password-protected.docx");
$settings->setFormat("xlsx");

$loadOptions = new GroupDocs\Conversion\Model\DocxLoadOptions();
$loadOptions->setPassword("password");
$loadOptions->setHideWordTrackedChanges(true);
$loadOptions->setDefaultFont("Arial");

$settings->setLoadOptions($loadOptions);

$convertOptions = new GroupDocs\Conversion\Model\XlsxConvertOptions();
$convertOptions->setFromPage(1);
$convertOptions->setPagesCount(2);
$convertOptions->setFromPage(1);
$convertOptions->setPassword("password");
$convertOptions->setUsePdf(true);
$settings->setConvertOptions($convertOptions);

$settings->setOutputPath("converted\\tocells");

$request = new GroupDocs\Conversion\Model\Requests\ConvertDocumentRequest($settings);

$response = $convertApi->convertDocument($request);
echo "Document converted successfully: ", $response[0]->getUrl();
```

## Licensing

GroupDocs.Conversion Cloud SDK for PHP is licensed under [MIT License](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-php/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/conversion/php) | [Documentation](https://wiki.groupdocs.cloud/conversioncloud/) | [Live Demo](https://products.groupdocs.app/conversion/family) | [API Reference](https://apireference.groupdocs.cloud/conversion/) | [Code Samples](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-php) | [Blog](https://blog.groupdocs.cloud/category/conversion/) | [Free Support](https://forum.groupdocs.cloud/c/conversion) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
