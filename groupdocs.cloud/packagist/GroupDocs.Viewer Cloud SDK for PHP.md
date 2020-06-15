# PHP Cloud REST API for Document Rendering

This REST API enhances your PHP based cloud apps to [render](https://products.groupdocs.cloud/viewer/php) 85+ types of file formats to image, PDF or HTML formats from within your apps.

## Cloud Document Viewer Features

- Support for rendering lots of document and image file formats.
- Fetch the list of all installed fonts or delete the fonts cache.
- Download HTML page resources, e.g., images, CSS, fonts etc.
- Render a document to PDF for HTML or image representation and download it.
- Fetch document information via various methods.
- Obtain list of links to document pages as HTML or images.
- Fetch and download ZIP archive of document pages as HTML or images.
- Rotate and reorder document pages.
- Specify image quality while rendering PDF as HTML.
- Decrease the resultant file size by excluding fonts when rendering as HTML.
- Render specific sections of worksheets defined as "print area" as HTML.
- Choose to include or exclude hidden content in Excel documents.
- Make the output content in HTML and SVG minified.
- Render a document to responsive HTML.
- Render email messages & render Outlook data files as HTML.
- Get list of all email attachments in its HTML or image representation.
- Download resources of a specific email attachment page for HTML representation.

## New Features in Version 20.5

- Added support for [Docker version of GroupDocs.Viewer Cloud](https://hub.docker.com/r/groupdocs/viewer-cloud) by SDKs.

For the detailed notes, please visit [GroupDocs.Viewer Cloud 20.5 Release Notes](https://wiki.groupdocs.cloud/viewercloud/release-notes/release-notes-2020/groupdocs-viewer-cloud-20-5-release-notes/).

## Supported File Formats

**Word Processing:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Spreadsheet:** XLS, XLSB, XLSM, XLSX, ODS, OTS, CSV, TSV
**Presentation:** PPT, PPTM, PPTX, PPS, PPSM, PPSX, POTX, POTM, ODP, OTP
**Project Management:** MPP, MPT
**Email:** EML, EMLX, MSG, OST, PST
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**Markup:** HTML, MHTML
**Diagram:** VDW, VDX, VSD, VSDM, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Note:** ONE
**Portable:** PDF, TEX, XPS
**Image:** BMP, CGM, DCM, DJVU, DNG, EMF, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PCL, PNG, PS, PSD, SVG, TIF, TIFF, WEBP, WMF
**eBook:** EPUB, MOBI

## Dependencies

- PHP 5.5 or later

## Authorization

To use SDK you need AppSID and AppKey authorization keys. You can get your AppSID and AppKey at [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## Installation & Usage

### Composer

The package is available at [Packagist](https://packagist.org/) and it can be installed via [Composer](http://getcomposer.org/) by executing following command:

`composer require groupdocscloud/groupdocs-viewer-cloud`

Or you can install SDK via [Composer](http://getcomposer.org/) directly from this repository, add the following to `composer.json`:

```php
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php.git"
    }
  ],
  "require": {
    "groupdocscloud/groupdocs-viewer-cloud": "*"
  }
}
```

Then run `composer install`.

## Manual Installation

Clone or download this repository, then run `composer install` in the root directory to install dependencies and include `autoload.php` into your code file:

```php
require_once('/path/to/groupdocs-viewer-cloud-php/vendor/autoload.php');
```

## Tests

To run the unit tests set your AppSID and AppKey in [json.config](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php/blob/master/tests/GroupDocs/Viewer/config.json) and execute following commands:

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
$configuration = new GroupDocs\Viewer\Configuration();
$configuration->setAppSid("XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX");
$configuration->setAppKey("XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX");

$infoApi = new GroupDocs\Viewer\InfoApi($configuration); 

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

## DWF File View Options using PHP REST API

```php
include(dirname(__DIR__) . '\CommonUtils.php');

$apiInstance = CommonUtils::GetViewApiInstance();

$viewOptions = new GroupDocs\Viewer\Model\ViewOptions();

$fileInfo = new GroupDocs\Viewer\Model\FileInfo();
$fileInfo->setFilePath("viewerdocs\\three-layouts.dwf");
$fileInfo->setPassword("");
$fileInfo->setStorageName(CommonUtils::$MyStorage);

$viewOptions->setFileInfo($fileInfo);

$renderOptions = new GroupDocs\Viewer\Model\RenderOptions();

$cadOptions = new GroupDocs\Viewer\Model\CadOptions();
$cadOptions->setWidth(800);

$renderOptions->setCadOptions($cadOptions);

$viewOptions->setRenderOptions($renderOptions);

$request = new GroupDocs\Viewer\Model\Requests\CreateViewRequest($viewOptions);
$response = $apiInstance->createView($request);

echo "Expected response type is ViewResult: ", $response;
```

## Licensing

GroupDocs.Viewer Cloud SDK for PHP is licensed under [MIT License](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/viewer/php) | [Documentation](https://wiki.groupdocs.cloud/viewercloud/) | [Demo](https://products.groupdocs.app/viewer/family) | [API Reference](https://apireference.groupdocs.cloud/viewer/) | [Examples](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php) | [Blog](https://blog.groupdocs.cloud/category/viewer/) | [Free Support](https://forum.groupdocs.cloud/c/viewer) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
