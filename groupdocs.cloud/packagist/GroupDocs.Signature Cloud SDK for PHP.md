# PHP Cloud REST API for eSigning Documents

Use this REST API to [search, verify & create signatures](https://products.groupdocs.cloud/signature/php) of 6 different types for a lot of file formats from within your PHP cloud apps.

## Cloud Document Signing Features

- Supports application of several types of document signatures.
- Specify pages (even, odd, specific etc.) to apply the signature on.
- Configure page padding options.
- Specify font, color, alignment & other appearance settings for the signature.
- Apply crop settings for the signature background.
- Setting to repeat the signature string to fill the specified area.
- Supports `CryptoApi` & `XmlDsig` methods of digital signatures.
- Configure alignment of text string along the barcode type signature.
- Support for various types of brushes to perform signature formatting.
- Apply signature to password-protected documents.
- Perform document signature verification.
- Get or set the time at which the document was digitally signed.
- Option to search some type of signatures from the document.

## New Features in Version 19.5

- This is the first release of a completely new version of the API `GroupDocs.Signature.Cloud v2.0`.
- `V2` provides a much simpler and intuitive API comparing with `V1`.
- `V2` includes Storage and File API which enables you to manage storage and files.

For the detailed notes, please visit [GroupDocs.Signature Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/signaturecloud/release-notes/release-notes-2019/groupdocs-signature-cloud-19-5-release-notes/).

## Signature Supported File Formats

The following file formats are supported for the barcode, image, QR-code, stamp and text type of signatures:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP
**Image:** BMP, GIF, JPG, JPEG, PNG, SVG, TIF, TIFF, WEBP, DJVU
**Metafile:** WMF
**CorelDraw:** CDR, CMX
**Adobe Photoshop:** PSD
**Adobe Acrobat:** PDF

## Digital Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**OpenOffice:** ODS, OTS
**Adobe Acrobat:** PDF

## FormField Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**OpenOffice:** ODS, OTS, ODP
**Adobe Acrobat:** PDF

## Metadata Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP
**Image:** JPG, JPEG, PNG, SVG, TIF, TIFF
**Adobe Photoshop:** PSD
**Adobe Acrobat:** PDF

## Supported Signature Types

- Text
- Image
- Barcode
- QR-code
- Digital
- Stamp

## Dependencies

- PHP 5.5 or later

## Authorization

To use SDK you need AppSID and AppKey authorization keys. You can your AppSID and AppKey at [GroupDocs Cloud for Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## Installation & Usage

### Composer

The package is available at [Packagist](https://packagist.org/) and it can be installed via [Composer](https://packagist.org/) by executing following command:

`composer require groupdocscloud/signature-sdk-php`

Or you can install SDK via Composer directly from this repository, add the following to `composer.json`:

```php
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-php.git"
    }
  ],
  "require": {
    "groupdocscloud/signature-sdk-php": "*"
  }
}
```

Then run `composer install`.

## Manual Installation

Clone or download this repository, then run `composer install` in the root directory to install dependencies and include `autoload.php` into your code file:

```php
require_once('/path/to/groupdocs-signature-cloud-php/vendor/autoload.php');
```

## Tests

To run the unit tests set your AppSID and AppKey in [json.config](https://packagist.org/) and execute following commands:

```php
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the installation procedure and then run the following:

```php
<?php

require_once(__DIR__ . '/vendor/autoload.php');

//TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud (free registration is required).
$configuration = new GroupDocs\Signature\Configuration();
$configuration->setAppSid("XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX");
$configuration->setAppKey("XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX");

$signatureApi = new GroupDocs\Signature\SignatureApi($configuration); 

try {
    $request = new GroupDocs\Signature\Model\Requests\GetSupportedFileFormatsRequest();
    $response = $signatureApi->getSupportedFileFormats($request);

    foreach ($response->getFormats() as $key => $format) {
        echo $format->getFileFormat() . " - " .  $format->getExtension(), "\n";
    }
} catch (Exception $e) {
    echo  "Something went wrong: ",  $e->getMessage(), "\n";
    PHP_EOL;
}

?>
```

## Get Supported Barcodes using PHP REST API

```php
include(dirname(__DIR__) . '\CommonUtils.php');

$apiInstance = CommonUtils::GetInfoApiInstance();

$response = $apiInstance->getSupportedBarcodes();

echo '<b>Supported Barcodes<br /></b>';
foreach($response->getBarcodeTypes() as $key => $format) {
  echo $format->getName(), "<br />";
}
```

## Licensing

GroupDocs.Signature for Cloud SDK for PHP is licensed under [MIT License](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-php/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/signature/php) | [Documentation](https://wiki.groupdocs.cloud/signaturecloud/) | [Live Demo](https://products.groupdocs.app/signature/family) | [API Reference](https://apireference.groupdocs.cloud/signature/) | [Examples](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-php) | [Blog](https://blog.groupdocs.cloud/category/signature/) | [Free Support](https://forum.groupdocs.cloud/c/signature) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
