# PHP REST API for OMR Processing

This Cloud SDK enables you to [perform Optical Mark Recognition (OMR)](https://products.aspose.cloud/omr/net) operations on human-marked data from within your cloud-based PHP apps.

## OMR Processing Features

- Perform recognition of scanned photos and images for OMR operations.
- Ability to perform OMR on rotated & perspective (within 25 deg) photos.
- Extract & recognize human-marked data from scanned tests, exams, surveys etc.
- Supports the export of OMR results to CSV file format.
- Use textual markup to generate OMR templates, generate surveys and test sheets.
- Availability of GUI application for managing OMR templates.
- Specify number of OMR based questions & answers in the template.
- Availability of GUI OMR editor as a cloud client.
- Provide JSON rules to perform OMR answer grading.
- Clip an area of interest from an image, save it as JPEG & perform OMR on it.
- Perform highly accurate optical mark recognition (OMR).

## Save OMR As

CSV

## Read OMR Formats

JPEG, PNG, BMP, TIFF, PDF

## Platform Independence

Aspose.OMR Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.OMR Cloud SDK for PHP

This repository contains Aspose.OMR Cloud SDK for PHP source code. To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) ([free registration](https://id.containerize.com/signup?clientId=prod.discourse.aspose&redirectUrl=https://forum.aspose.cloud/session/sso) is required).

Please check the [GitHub Repository](https://github.com/aspose-omr-cloud/aspose-omr-cloud-php) for the source code and examples.

## How to use the SDK

You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/aspose-omr-cloud) (recommended).

## Requirements

- PHP 5.6 and later

## PHP 5.6/Windows

- Please make sure that local repository path and all paths of all required packages do not exceed maximum length of a path (usually 255 symbols).
- Aspose.OMR for Cloud use Guzzle library to perform REST requests. Guzzle framework uses cURL (`libcurl`) as transport library. On windows platform you can face problems with accessing https resources depending on `libcurl` version you are using.
  - If you are using `libcurl` built with `OpenSSL`, you need to download CA Certificates and update your `php.ini`:

    ```php
    ....
    [curl]
    curl.cainfo="<full path to cacert.pem file>"
    [openssl]
    openssl.cafile="<full path to cacert.pem file>"
    ...
    ```
  
  - If you are using `libcurl` built with WinSSL, you are ready to go because `WinSSL` uses windows certificates store

`OpenSSL` and `WinSSL` based `libcurl` versions can be downloaded from [here](https://curl.haxx.se/gknw.net/7.40.0/). Just choose your platform (x86 or x64) and `OpenSSL` (look for `ssl` string in the file name) or `WinSSL` (look for `winssl` string in the file name)

## Installation

### Clone repository

Clone `aspose-omr-cloud` with submodules:

```console
git clone https://github.com/aspose-omr-cloud/aspose-omr-cloud-php.git --recurse-submodules
```

### Composer

To install the bindings via Composer, add the following to `composer.json`:

```php
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/aspose-omr-cloud/aspose-omr-cloud-php.git"
    }
  ],
  "require": {
    "aspose/aspose-omr-cloud": "*@dev"
  }
}
```

Then run `composer install`.

### Manual Installation

Download the files and include `autoload.php`:

```console
require_once('/path/to/Aspose.OMR for Cloud/vendor/autoload.php');
```

## Limitations

- Recognition process works well with the bubbles which are at least 75% filled.
- Works on perspective (side viewed/out of focus) & rotated images under certain conditions, e.g., rotation angle within 25 degrees.
- OMR operation will show results only in text format.
- Performing OCR operation is not supported for now.

[Product Page](https://products.aspose.cloud/omr/net) | [Documentation](https://docs.aspose.cloud/display/omrcloud/Home) | [API Reference](https://apireference.aspose.cloud/omr/) | [Code Samples](https://github.com/aspose-omr-cloud) | [Blog](https://blog.aspose.cloud/category/omr/) | [Free Support](https://forum.aspose.cloud/c/omr) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
