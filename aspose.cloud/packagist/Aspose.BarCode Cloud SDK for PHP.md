This cloud SDK assists you to seamlessly integrate barcode generation, processing & conversion functionality into your PHP cloud apps.

## BarCode Processing Features

- Generate, san and customize 1D (linear), 2D and postal barcodes.
- Generate and recognize barcodes with checksum option.
- Fetch barcode as an image stream or save barcode to the local disk.
- Configure barcode height, width, angle quality, margin & resolution.
- Configure barcode to be auto-sized or set X & Y dimensions.
- Generate a new barcode with specified code text location.
- Apply bar height and barcode image format.
- Rotate barcode image at a certain angle & generate multiple barcodes.
- Scan image to recognize barcode from a specific region of that image.
- Recognize specified number of barcodes.
- Apply image processing algorithms to read barcodes.

## Read & Write BarCode Formats

JPEG, TIFF, PNG, BMP, GIF

## Save BarCode As

EMF, SVG

## Supported Barcode Symbologies

**Linear barcode symbologies:**
EAN13, EAN8, UPCA, UPCE, Interleaved2of5, Standard2of5, MSI, Code11, Codabar, EAN14(SCC14), SSCC18, ITF14, Matrix 2 of 5, PZN, Code128, Code39 Extended, Code39 Standard, Code93 Extended, Code16K, Code93 Standard, IATA 2 of 5, OPC, GS1Code128, ISBN, ISMN, ISSN, ITF6, VIN, Pharmacode, DatabarOmniDirectional, DatabarTruncated, DatabarLimited, DatabarExpanded, DatabarStackedOmniDirectional, DatabarExpandedStacked, DatabarStacked, PatchCode, Supplement (Decode only).

**2D barcode symbologies:**
PDF417, MacroPDF417, MicroPDF417, CompactPDF417 (Decode only), DataMatrix, Aztec, QR, MicroQR, DotCode, MaxiCode, Italian Post 25, GS1DataMatrix, Code16K.

**Postal barcode symbologie:s**
Postnet, Planet, USPS OneCode, Australia Post, Deutsche Post Identcode, Deutsche Post Leticode, RM4SCC, SingaporePost, AustralianPosteParcel, SwissPostParcel, UpcaGs1DatabarCoupon.

## Platform Independence

Aspose.BarCode Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.BarCode Cloud SDK for PHP

This repository contains Aspose.BarCode Cloud SDK for PHP source code. To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) (free registration of [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) is required for this).

Please check the [GitHub Repository](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-php) for the source code and examples.

## How to use the SDK

You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/barcode-cloud-php) (recommended).

## Installation via Composer

Aspose.BarCode Cloud SDK for PHP is available on `Packagist` as the `barcode-cloud-php` package. Run the following command:

```console
composer require aspose/barcode-cloud-php
```

To use the SDK, use Composer's [autoload](https://getcomposer.org/doc/00-intro.md#autoloading):

```php
require __DIR__ . '/vendor/autoload.php';
```

### Sample usage

```php
use Aspose\BarCode\Configuration;
use Aspose\BarCode\BarCodeApi;
use Aspose\BarCode\Requests\BarCodeGetBarCodeGenerateRequest;

$config = new Configuration();
$config->setAppKey("your_key");
$config->setAppSid("your_sid");

$request = new BarCodeGetBarCodeGenerateRequest();
$request->type = "QR";
$request->text = "PHP SDK Test";
$request->format = "png";

$api = new BarCodeApi(null, $config);
$response = $api->BarCodeGetBarCodeGenerate($request);

$type = 'image/png';
$size = $response->getSize();
header('Content-Type:'.$type);
header('Content-Length: ' . $size);
echo $response->fread($size);
```

## Licensing

All Aspose.BarCode for Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-php/blob/HEAD/LICENSE).

[Product Page](https://products.aspose.cloud/barcode/php) | [Documentation](https://docs.aspose.cloud/display/barcodecloud/Home) | [API Reference](https://apireference.aspose.cloud/barcode/) | [Code Samples](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-php) | [Blog](https://blog.aspose.cloud/category/barcode/) | [Free Support](https://forum.aspose.cloud/c/barcode) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
