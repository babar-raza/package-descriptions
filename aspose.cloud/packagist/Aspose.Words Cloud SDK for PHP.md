# PHP REST API for Cloud Document Processing

This cloud SDK provides seamless integration of [cloud document processing & manipulation features](https://products.aspose.cloud/words/net) into your cloud-based PHP apps.

## Document Processing Features

- Programmatically create new documents of various file formats.
- Fetch a web page via its URL and save it in Microsoft Word file format.
- Get document information, by default, in JSON/XML representation.
- Fetch statistical data of a document.
- Render complex elements (table, DrawingObject etc.) of the document in supported formats.
- Remove all macros contained in a specific document.
- Convert a document to desired file format along with detailed settings.
- Convert an encrypted PDF document into MS Word document format.
- So many more features.

## Enhancements in Version 20.1

- Moved property `ColorMode` from `SaveOptionsData` to `FixedPageSaveOptionsData`.
- Replaced `MemoryStream` and `byte[]` with `SixLabors.ImageSharp.IImage` in image processing.
- Included support of `ICC` profiles and implement `ICCBased` color space.

For the detailed notes, please visit [Aspose.Words Cloud 20.1 Release Notes](https://docs.aspose.cloud/display/wordscloud/Aspose.Words+Cloud+20.1+Release+Notes).

## Read & Write Document Formats

**Microsoft Word:** DOC, DOCX, RTF, DOT, DOTX, DOTM, FlatOPC (XML)
**OpenOffice:** ODT, OTT
**WordprocessingML:** XML
**Web:** HTML, MHTML, HtmlFixed
**Text:** TXT
**Fixed Layout:** PDF

## Save Document As

**Fixed Layout:** PDF/A, XPS, OpenXPS, PS
**Images:** JPEG, PNG, BMP, SVG, TIFF, EMF
**Others:** PCL

## Getting Started with Aspose.Words Cloud SDK for PHP

This repository contains Aspose.Words Cloud SDK for PHP source code. To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) ([free registration](https://id.containerize.com/signup?clientId=prod.discourse.aspose&redirectUrl=https://forum.aspose.cloud/session/sso) is required).

Please check the [GitHub Repository](https://github.com/aspose-words-cloud/aspose-words-cloud-php) for the source code and examples.

## How to use the SDK

You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/aspose-words-cloud) (recommended).

## Installation via Composer

Aspose.Words Cloud SDK for PHP is available on `Packagist` as the `aspose-words-cloud` package. Run the following command:

```console
composer require aspose/aspose-words-cloud
```

To use the SDK, use Composer's [autoload](https://getcomposer.org/doc/00-intro.md#autoloading):

```php
require __DIR__ . '/vendor/autoload.php';
```

### Split Specific Pages of a DOCX Document to PDF using PHP Code

```php
<?php
    require_once realpath(__DIR__ . '/..') . '/vendor/autoload.php';

    use Aspose\Storage\Api\StorageApi;
    use Aspose\Words\Configuration;
    use Aspose\Words\WordsApi;
    use Aspose\Words\Model\Requests;
    use Aspose\Words\Model\SaveOptionsData;
    use Aspose\Words\Model\DocumentEntryList;
    use Aspose\Words\Model\DocumentEntry;

    class Document {

        public $wordsApi;
        public $storageApi;

        public function __construct() {
            #$BaseUrl = "https://api.aspose.cloud/v1.1/";
            $AppKey = ""; // Get AppKey and AppSID from https://dashboard.aspose.cloud/
            $AppSid = ""; // Get AppKey and AppSID from https://dashboard.aspose.cloud/

            $config = new Configuration();
            $config->setAppKey($AppKey)->setAppSid($AppSid);
            $this->wordsApi = new WordsApi(null, $config);

            $this->storageApi = new StorageApi();
            $this->storageApi->getConfig()->setAppKey($AppKey)->setAppSid($AppSid);//->setHost($BaseUrl);
        }

        public function uploadFile($fileName) {
            $file = realpath(__DIR__ . '/../..') . '/TestData/Common/' . $fileName;
            $putRequest = new Aspose\Storage\Model\Requests\PutCreateRequest($fileName, $file);
            $this->storageApi->PutCreate($putRequest);
        }

        public function splitSpecificPagesToNewPDFs() {
            $fileName = "test_multi_pages.docx";
            $format = "pdf";
            $from = 1; // Splitting starts from the first page of the document
            $to = 2; // splitting ends at the last page of the document
            $folder = null; // Input file exists at the root of the storage
            $destName = null;

            // Upload source document to Cloud Storage
            $this->uploadFile($fileName);

            $request = new Requests\PostSplitDocumentRequest($fileName, $folder, null, null, null, $destName, $format, $from, $to);
            $result = $this->wordsApi->postSplitDocument($request);
            print_r($result);
        }

    }

    $document = new Document();
    $document->splitSpecificPagesToNewPDFs();
?>
```

## Samples

[Tests](https://github.com/aspose-words-cloud/aspose-words-cloud-php/blob/HEAD/tests/Aspose/Words) contain various examples of using the SDK.

## Licensing

All Aspose.Words Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-words-cloud/aspose-words-cloud-php/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/words/php) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [Live Demo](https://products.aspose.app/words/family) | [API Reference](https://apireference.aspose.cloud/words/) | [Code Samples](https://github.com/aspose-words-cloud/aspose-words-cloud-php) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
