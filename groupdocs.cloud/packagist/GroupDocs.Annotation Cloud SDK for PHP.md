# Document Annotation PHP Cloud REST API

This REST API enhances your PHP cloud apps to [import, export & process text & figure annotations](https://products.groupdocs.cloud/annotation/php) within documents for 35+ file formats.

## Cloud Document Annotation Features

- Fetch document description with meta data and coordinates of text on pages.
- Fetch annotation data from files of supported formats.
- Import annotation information from documents.
- Export annotation information to a document and fetch it as a stream.
- Remove document annotations.
- Get image representation of the document pages.
- Render documents to PDF format with storage URL or stream output.
- Add or remove document or image annotations of various types.

## New Features in Version 19.5

- This is the first release of a completely new version of the API `GroupDocs.Annotation.Cloud v2.0`.
- `V2` provides much simpler and intuitive API comparing with `V1`.
- `V2` includes Storage and File API which enables users to manage storage and files.

For the detailed notes, please visit [GroupDocs.Annotation Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/annotationcloud/release-notes/2019/groupdocs-annotation-cloud-19-5-release-notes/).

## Supported Annotation Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF, TXT
**Microsoft Excel:** XLS, XLSX, XLSB, XLSX
**Microsoft PowerPoint:** PPT, PPTX, PPSX
**Microsoft Visio:** VSD, VDX, VSS, VSDM
**OpenOffice:** OTT, ODT, ODP, OTP
**Image:** JPEG, TIFF, BMP, GIF, DJVU
**Metafile:** EMF, WMF
**Email:** EML, EMLX, MSG
**Portable:** PDF
**Medical Imagery:** DICOM
**Markup:** HTML, MHTML
**AutoCAD:** CAD

## Supported Text Annotation Types

**Text annotation** – add comments to selected text.
**Text replacement** – highlight which text should be replaced with what.
**Text redaction** – hide confidential text.
**Strikeout/underline** – highlight text with strikethroughs/underlines.
**Typewriter** – add sticky notes with rich text.

## Supported Figure Annotation Types

**Area annotation** – add notes to an area highlighted with a rectangle.
**Point annotation** – add notes to any point in the document.
**Area redaction** – hide confidential parts of an image or text.
**Polyline** – draw freehand lines and shapes.
**Pointer/arrow** – drop arrows pointing to an object.
**Watermark** – create text-based watermark overlays.
**Distance** – measure the distance between any objects in a document.

## Platform Independence

GroupDocs.Annotation Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Dependencies

- PHP 5.5 or later

## Authorization

To use SDK you need AppSID and AppKey authorization keys. You can get your AppSID and AppKey at [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## Installation & Usage

### Composer

The package is available at [Packagist](https://packagist.org/) and it can be installed via [Composer](http://getcomposer.org/) by executing following command:

`composer require groupdocscloud/groupdocs-annotation-cloud`

Or you can install SDK via [Composer](http://getcomposer.org/) directly from this repository, add the following to `composer.json`:

```console
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-php.git"
    }
  ],
  "require": {
    "groupdocscloud/groupdocs-annotation-cloud": "*"
  }
}
```

Then run `composer install`.

### Manual Installation

Clone or download this repository, then run `composer install` in the root directory to install dependencies and include `autoload.php` into your code file:

```php
require_once('/path/to/groupdocs-annotation-cloud-php/vendor/autoload.php');
```

## Tests

To run the unit tests set your AppSID and AppKey in [json.config](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-php/blob/master/tests/GroupDocs/Annotation/config.json) and execute following commands:

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
$configuration = new GroupDocs\Annotation\Configuration();
$configuration->setAppSid("XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX");
$configuration->setAppKey("XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX");

$infoApi = new GroupDocs\Annotation\InfoApi($configuration); 

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

## Add Annotation using PHP REST API

```php
include(dirname(__DIR__) . '\CommonUtils.php');

$apiInstance = CommonUtils::GetAnnotateApiInstance();

$a = new GroupDocs\Annotation\Model\AnnotationInfo();
$pt = new GroupDocs\Annotation\Model\Point();
$pt->setX(852);
$pt->setY(59.388262910798119);
$a->setAnnotationPosition($pt);
$box = new GroupDocs\Annotation\Model\Rectangle();
$box->setX(375.89276123046875);
$box->setY(59.388263702392578);
$box->setWidth(88.7330551147461);
$box->setHeight(37.7290153503418);
$a->setBox($box);
$a->setPageNumber(0);
$a->setPenColor(1201033);
$a->setPenStyle(0);
$a->setPenWidth(1);
$a->setType(GroupDocs\Annotation\Model\AnnotationInfo::TYPE_AREA);
$a->setCreatorName("Anonym A.");

$request = new GroupDocs\Annotation\Model\Requests\postAnnotationsRequest("annotationdocs\\ten-pages.docx", [$a]);
$apiInstance->postAnnotations($request);

echo "Expected response type is void: Annotation added.";
```

## Use PHP REST API to Add Text Strikethrough Annotation

```php
include(dirname(__DIR__) . '\CommonUtils.php');

$apiInstance = CommonUtils::GetAnnotateApiInstance();

$a = new GroupDocs\Annotation\Model\AnnotationInfo();
$pt = new GroupDocs\Annotation\Model\Point();
$pt->setX(852);
$pt->setY(59.388262910798119);
$a->setAnnotationPosition($pt);
$a->setPageNumber(2);
$a->setFontColor(1201033);
$a->setFontSize(12);
$a->setOpacity(0.7);
$a->setType(GroupDocs\Annotation\Model\AnnotationInfo::TYPE_TEXT_STRIKEOUT);
$a->setText("This is text strikeout annotation");
$a->setCreatorName("Anonym A.");

$request = new GroupDocs\Annotation\Model\Requests\postAnnotationsRequest("annotationdocs\\ten-pages.docx", [$a]);
$apiInstance->postAnnotations($request);

echo "Expected response type is void: Text Strikeout Annotation added.";
```

## Licensing

GroupDocs.Annotation Cloud SDK for PHP is licensed under [MIT License](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-php/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/annotation/php) | [Documentation](https://wiki.groupdocs.cloud/annotationcloud/) | [API Reference](https://apireference.groupdocs.cloud/annotation/) | [Code Samples](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-php) | [Blog](https://blog.groupdocs.cloud/category/annotation/) | [Free Support](https://forum.groupdocs.cloud/c/annotation) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
