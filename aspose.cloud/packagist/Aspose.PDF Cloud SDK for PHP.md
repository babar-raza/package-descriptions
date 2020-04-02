# PHP REST API to Process PDF in Cloud

This Cloud SDK allows you to [easily build cloud-based PDF creator](https://products.aspose.cloud/pdf/net), editor & converter apps in PHP language for various cloud platforms.

## PDF Processing Features

- Add PDF document's header & footer in text or image format.
- Add tables & stamps (text or image) to PDF documents.
- Append multiple PDF documents to an existing file.
- Work with PDF attachments, annotations, & form fields.
- Apply encryption or decryption to PDF documents & set password.
- Delete all stamps & tables from a page or entire PDF document.
- Delete a specific stamp or table from the PDF document by its ID.
- Replace a single or multiple instances of a text on a PDF page or from entire document.
- Extensive support for converting PDF documents to various other file formats.
- Extract various elements of PDF file & make PDF document optimized.

## New Features in Version 20.3

- Prepared Aspose.PDF Cloud using the latest version of Aspose.PDF for .NET.

For the detailed notes, please visit [Aspose.PDF Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/pdfcloud/Aspose.PDF+Cloud+20.3+Release+Notes).

## Read & Write PDF Formats

PDF, EPUB, HTML, TeX, SVG, XML, XPS, FDF, XFDF

## Save PDF As

XLS, XLSX, PPTX, DOC, DOCX, MobiXML, JPEG, EMF, PNG, BMP, GIF, TIFF, Text

## Read PDF Formats

MHT, PCL, PS, XSLFO, MD

## Getting Started with Aspose.PDF Cloud SDK for PHP

This repository contains Aspose.PDF Cloud SDK for PHP source code. To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) ([free registration](https://id.containerize.com/signup?clientId=prod.discourse.aspose&redirectUrl=https://forum.aspose.cloud/session/sso) is required).

Please check the [GitHub Repository](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-php) for the source code and examples.

## How to use the SDK

You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/pdf-sdk-php) (recommended).

## Requirements

- PHP 5.4.0 and later

## Unit Tests

Aspose PDF SDK includes a suite of unit tests within the "tests" subdirectory. These Unit Tests also serves as examples of how to use the Aspose PDF SDK.

To run the unit tests:

```console
composer install
./vendor/bin/phpunit
```

## Usage

APIs of this SDK can be called as follows:

```php
<?php
use Aspose\PDF\Api\PdfApi;
use Aspose\PDF\Configuration;

class PdfApiUsage
{

    protected $pdfApi;
    protected $tempFolder;
    protected $config;

    protected function setUp()
    {
        // Get App key and App SID from https://cloud.aspose.com
        $appSid = '';
        $appKey = '';

        $this->tempFolder = 'TempPdfCloud';

        $this->config = new Configuration();
        $this->config->setAppKey($appKey);
        $this->config->setAppSid($appSid);

        $this->pdfApi = new PdfApi(null, $this->config);
    }

    public function testGetPageAnnotations()
    {
        $name = 'PdfWithAnnotations.pdf';
        $pageNumber = 2;

        $response = $this->pdfApi->getPageAnnotations($name, $pageNumber, null, $this->tempFolder);
    }
}
```

## Fetch Annotations from a PDF Document using PHP Code

```php
require __DIR__.'/../vendor/autoload.php';

use Aspose\PDF\Api\PdfApi;
use Aspose\PDF\Configuration;


$appSid = 'XXXXXXXXX';
$appKey = 'XXXXXXXXX';


$tempFolder = null;

$config = new Configuration();
$config->setAppKey($appKey);
$config->setAppSid($appSid);

$pdfApi = new PdfApi(null, $config);
$name = 'PdfWithAnnotations.pdf';


$response = $pdfApi->getDocumentAnnotations($name, null, $tempFolder);

echo $response
```

## Licensing

All Aspose.PDF Cloud SDKs are licensed under [MIT License](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-php/blob/HEAD/LICENSE).

[Product Page](https://products.aspose.cloud/pdf/net) | [Documentation](https://docs.aspose.cloud/display/pdfcloud/Home) | [API Reference](https://apireference.aspose.cloud/pdf/) | [Code Samples](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/pdf/) | [Free Support](https://forum.aspose.cloud/c/pdf) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
