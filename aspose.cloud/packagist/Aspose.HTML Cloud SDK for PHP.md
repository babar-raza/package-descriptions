# HTML Rendering & Conversion PHP Cloud REST API

This cloud SDK assists to develop cloud-based [HTML page rendering, processing, translation & conversion](https://products.aspose.cloud/html/net) apps in PHP language via REST API.

## HTML Processing Features

- Fetch HTML page along with its resources as a ZIP archive by providing page URL.
- Based on page URL, retrieve all images of an HTML page as a ZIP package.
- Load data from local file to populate HTML document template.
- Use request body to populate HTML document template.
- Convert HTML page to numerous other file formats.

## New Features in Version 20.5

- Added `Configuration.AddDefaultHeader`. It provides ability to specify custom headers which will be added to each `HTTP` request beneath API calls.

For the detailed notes, please visit [Release Notes - 2020](https://docs.aspose.cloud/display/htmlcloud/Release+Notes+-+2020).

## Read & Write HTML Formats

HTML, XHTML, zipped HTML, zipped XHTML, MHTML, HTML containing SVG markup, Markdown, JSON

## Save HTML As

**Fixed Layout:** PDF, XPS
**Images:** TIFF, JPEG, PNG, BMP, GIF
**Other:** TXT, ZIP (images)

## Read HTML Formats

**eBook:** EPUB
**Other:** XML, SVG

## Getting Started with Aspose.HTML Cloud SDK for PHP

This repository contains Aspose.BarCode Cloud SDK for PHP source code. To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) ([free registration](https://id.containerize.com/signup?clientId=prod.discourse.aspose&redirectUrl=https://forum.aspose.cloud/session/sso) is required).

Please check the [GitHub Repository](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-php) for the source code and examples.

## How to use the SDK

You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/aspose-html-cloud-php) (recommended).

## Installation via Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```php
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/aspose-html-cloud/aspose-html-cloud-php.git"
    }
  ],
  "require": {
    "aspose/aspose-html-cloud-php": "dev-master"
  }
}
```

Then run `composer install`.

## Manual Installation

Download the files and include `autoload.php`:

```console
require_once('/path/to/aspose-html-cloud-php/vendor/autoload.php');
```

## Usage Example

Pass configuration to constructor (see in tests - BaseTest.php)

```php
$conf = array(
  "basePath" => "https://api.aspose.cloud/v3.0",
  "authPath" => "https://api.aspose.cloud/connect/token",
  "apiKey" => "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "appSID" => "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
  "testResult" => "\\testresult\\",
  "testData" => "\\testdata\\",
  "remoteFolder" => "HtmlTestDoc",
  "defaultUserAgent" => "Webkit",
  "debugFile" => "php://output",
  "debug" => false
);

self::$api_html = new HtmlApi($configuration);
self::$api_stor = new StorageApi($configuration);

// optional for test
self::$testFolder = realpath(__DIR__ . '/../..') . $configuration['testData'];
self::$testResult = realpath(__DIR__ . '/../..') . $configuration['testResult'];
```

### Note: do not forget to add in `php.ini`

```php
...
extension=php_openssl.dll
...
upload_max_filesize = 200M ; or 0 - unlimited
...
max_execution_time = 0 ; unlimited
...
default_socket_timeout = 3600 ; for long time operations
```

Please follow the [installation procedure](https://packagist.org/packages/aspose/aspose-html-cloud-php#user-content-installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$conf = array(
  "basePath" => "https://api.aspose.cloud/v3.0",
  "authPath" => "https://api.aspose.cloud/connect/token",
  "apiKey" => "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "appSID" => "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
  "testResult" => "\\testresult\\",
  "testData" => "\\testdata\\",
  "remoteFolder" => "HtmlTestDoc",
  "defaultUserAgent" => "Webkit",
  "debugFile" => "php://output",
  "debug" => false
);

$apiInstance = new Client\Invoker\Api\HtmlApi($conf);

$name = "name_example"; // string | Document name.
$out_format = "png"; // string | Resulting image format.
$width = 800; // int | Resulting image width.
$height = 1000; // int | Resulting image height.
$left_margin = 10; // int | Left resulting image margin.
$right_margin = 10; // int | Right resulting image margin.
$top_margin = 10; // int | Top resulting image margin.
$bottom_margin = 10; // int | Bottom resulting image margin.
$resolution = 300; // int | Resolution of resulting image.
$folder = "folder_example"; // string | The source document folder.
$storage = "storage_example"; // string | The source document storage.

try {
    $result = $apiInstance->getConvertDocumentToImage($name, $out_format, $width, $height, $left_margin, $right_margin, $top_margin, $bottom_margin, $resolution, $folder, $storage);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HtmlApi->getConvertDocumentToImage: ', $e->getMessage(), PHP_EOL;
}

?>
```

[Product Page](https://products.aspose.cloud/html/net) | [Documentation](https://docs.aspose.cloud/display/htmlcloud/Home) | [Demo](https://products.aspose.app/html/family) | [API Reference](https://apireference.aspose.cloud/html/) | [Examples](https://github.com/aspose-html-cloud/aspose-html-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/html/) | [Free Support](https://forum.aspose.cloud/c/html) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
