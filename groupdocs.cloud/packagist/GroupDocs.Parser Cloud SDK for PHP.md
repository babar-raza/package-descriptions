# Document Parser PHP Cloud REST API

This [document parser & data extraction REST API](https://products.groupdocs.cloud/parser/php) can be used to enhance your PHP cloud-based applications to perform parsing operations.

## Cloud Document Parser Features

- Create easy to define templates with data field and table definitions.
- Parse documents with pre-defined templates.
- Extract data from invoices or from other sort of documents.
- Supports extracting text and images.
- Extract data from regular documents as well as from email or archive containers.
- Obtain data from PDF portfolios.
- Fetch text fields, numbers and tables from common documents.
- Save your templates in the storage and parse your documents with them.
- Ability to extract HTML or Markdown (MD) text for a quick preview.
- Fetch specific pages of plain as well as formatted text.
- Extract formatted (bold, italic, hyperlink etc.) text in the MD format.
- Support for extracting text in HTML formatting (paragraph, hyperlinks, lists etc.).
- Retrieve all images from a document and save them.
- Obtain basic information about documents, archives, emails, and attachments etc.
- Extract data from a document contained inside a ZIP archive, email or PDF portfolio.

## New Features & Enhancements in Version 20.6

- Added `Node.js`, `PHP`, `Python`, and `Ruby` SDK for GroupDocs.Parser Cloud.
- Implemented extraction of encoding.
- Implemented additional image information extraction.

For the detailed notes, pelase visit [GroupDocs.Parser for Cloud 20.6 Release Notes](https://wiki.groupdocs.cloud/parsercloud/release-notes/release-notes-2020/groupdocs-parser-for-cloud-20-6-release-notes).

## Parse Document By Template Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF

## Extract Text Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Emails:** EML, EMLX, MSG
**Notes:** ONE

## Extract Document Info Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Emails:** PST, OST, EML, EMLX, MSG
**Notes:** ONE
**Archives:** ZIP

## Extract Images Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Emails:** EML, EMLX, MSG
**Archives:** ZIP

## Extract Container Items Info Supported Formats

**Portable:** PDF
**Emails:** PST, OST, EML, EMLX, MSG
**Archives:** ZIP

## Getting Started

You do not need to install anything to get started with GroupDocs.Parser Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Please check the [GitHub Repository](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-php-samples) for other common usage scenarios.

## Dependencies

- PHP 5.5 or later

## Authorization

To use SDK you need `AppSID` and `AppKey` authorization keys. You can get your `AppSID` and `AppKey` at [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## Installation & Usage

### Composer

The package is available at [Packagist](https://packagist.org/) and it can be installed via [Composer](http://getcomposer.org/) by executing following command:

```shell
composer require groupdocscloud/groupdocs-parser-cloud
```

Or you can install SDK via [Composer](http://getcomposer.org/) directly from this repository, add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-php.git"
    }
  ],
  "require": {
    "groupdocscloud/groupdocs-parser-cloud": "*"
  }
}
```

Then run `composer install`

### Manual Installation

Clone or download this repository, then run `composer install` in the root directory to install dependencies and include `autoload.php` into your code file:

```php
require_once('/path/to/groupdocs-parser-cloud-php/vendor/autoload.php');
```

## Tests

To run the unit tests set your `AppSID` and `AppKey` in [json.config](tests/GroupDocs/Parser/config.json) and execute following commands:

```shell
php composer.phar install
./vendor/bin/phpunit
```

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php

require_once(__DIR__ . '/vendor/autoload.php');

//TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud (free registration is required).
$configuration = new GroupDocs\Parser\Configuration();
$configuration->setAppSid("XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX");
$configuration->setAppKey("XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX");

$infoApi = new GroupDocs\Parser\InfoApi($configuration); 

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

## Prerequisites

- `PHP` with `Composer` installed
- Get your `AppSID` and `AppKey` at [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## How to Run the Examples

The package contains PHP examples. Follow the given steps to proceed run:

- Extract the downloaded project.
- Edit `Utils.php` and put `appSid` and `appKey`, obtained from [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud).
- Go to "Examples" directory of the project.
- Execute `composer update` command.
- Run examples using `php .\RunExamples.php` command.

For more details, please visit [Getting Started](https://docs.groupdocs.cloud/display/parsercloud/Getting+Started).

[Product Page](https://products.groupdocs.cloud/parser/php) | [Documentation](https://wiki.groupdocs.cloud/parsercloud/) | [Demo](https://products.groupdocs.app/parser/family) | [API Reference](https://apireference.groupdocs.cloud/parser/) | [Examples](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-php-samples) | [Blog](https://blog.groupdocs.cloud/category/parser/) | [Free Support](https://forum.groupdocs.cloud/c/parser) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
