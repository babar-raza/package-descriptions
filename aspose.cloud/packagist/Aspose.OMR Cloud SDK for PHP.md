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

## Requirements

- [PHP 5.6 or later](https://www.php.net/releases/)

### PHP 5.6/Windows

- Please make sure that local repository path and all paths of all required packages do not exceed maximum length of a path (usually 255 symbols).
- Aspose.OMR for Cloud use [Guzzle](http://guzzle3.readthedocs.io/getting-started/overview.html) library to perform REST requests. Guzzle framework uses cURL (libcurl) as transport library. On windows platform you can face problems with accessing https resources depending on libcurl version you are using.
        If you are using libcurl built with OpenSSL, you need to download [CA Certificates](https://curl.haxx.se/docs/caextract.html) and update your php.ini:
  
  ```curl
    ....
    [curl]
    curl.cainfo="<full path to cacert.pem file>"
    [openssl]
    openssl.cafile="<full path to cacert.pem file>"
    ...
  ```

- If you are using libcurl built with WinSSL, you are ready to go becuase WinSSL uses windows certificates store

OpenSSL and WinSSL based libcurl versions can be downloaded from here. Just choose your platform (x86 or x64) and OpenSSL (look for `ssl` string in the file name) or WinSSL (look for winssl string in the file name)

## Installation

- Sign Up. Before you begin, you need to sign up for an account on our [Dashboard](https://dashboard.aspose.cloud/) and retrieve your [credentials](https://dashboard.aspose.cloud/#/apps).
- Minimum requirements. This SDK requires [PHP 5.6 or later](https://www.php.net/releases/).
- Install Aspose.Imaging Cloud PHP SDK. Please, add the following [Packagist package](https://packagist.org/packages/aspose/aspose-imaging-cloud) to your project.

Please, add the following to your composer.json as a dependency.

```console
{
    "require": {
        "aspose/aspose-imaging-cloud": ">=20.2"
    }
}
```

Import the dependencies to your code as follows.

```php
use \Aspose\Imaging\ImagingApi;
use \Aspose\Imaging\Configuration;
use \Aspose\Imaging\Model;
use \Aspose\Imaging\Model\Requests;
```

## Usage

### Update submodule

Make sure you've cloned [aspose-omr-cloud-demo-data](https://github.com/aspose-omr-cloud/aspose-omr-cloud-demo-data) submodule, that contains all data required to run demo. In case you are missing submodules use the following git commands to initialize and update them:

```console
git submodule init
git submodule update --remote --merge
```

## Limitations

- Recognition process works well with the bubbles which are at least 75% filled.
- Works on perspective (side viewed/out of focus) & rotated images under certain conditions, e.g., rotation angle within 25 degrees.
- OMR operation will show results only in text format.
- Performing OCR operation is not supported for now.

[Product Page](https://products.aspose.cloud/omr/net) | [Documentation](https://docs.aspose.cloud/display/omrcloud/Home) | [Live Demo](https://products.aspose.app/omr/family) | [API Reference](https://apireference.aspose.cloud/omr/) | [Code Samples](https://github.com/aspose-omr-cloud) | [Blog](https://blog.aspose.cloud/category/omr/) | [Free Support](https://forum.aspose.cloud/c/omr) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
