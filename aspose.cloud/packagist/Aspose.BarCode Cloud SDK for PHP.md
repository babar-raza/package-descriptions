# PHP Rest API for Barcode Manipulation in Cloud

This cloud SDK assists you to seamlessly integrate [barcode generation, processing & conversion](https://products.aspose.cloud/barcode/php) functionality into your PHP cloud apps.

## BarCode Processing Features

- Generate, scan and customize 1D (linear), 2D and postal barcodes.
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

**Postal barcode symbologies:**
Postnet, Planet, USPS OneCode, Australia Post, Deutsche Post Identcode, Deutsche Post Leticode, RM4SCC, SingaporePost, AustralianPosteParcel, SwissPostParcel, UpcaGs1DatabarCoupon.

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

## Set Hight of the Bars in the Barcode using PHP

```php
//For complete examples and data files, please go to https://github.com/aspose-barcode/Aspose.BarCode-for-Cloud

\Aspose\Storage\AsposeApp::$apiKey = $apiKey;
\Aspose\Storage\AsposeApp::$appSID = $appSid;
\Aspose\Barcode\AsposeApp::$apiKey = $apiKey;
\Aspose\Barcode\AsposeApp::$appSID = $appSid;

// Instantiate Aspose Storage Cloud API SDK
$storageApi = new StorageApi ();

// Instantiate Aspose BarCode Cloud API SDK
$barcodeApi = new BarcodeApi ();

// Set the barcode file name created on server.
$name = "sample-barcode";

// Set Text to encode inside barcode
$text = "Aspose.BarCode";

// Set Barcode Symbology
$type = "Code128";

// Set Generated Barcode Image Format
$format = "PNG";

// Set Resolution along X and Y in dpi
$resolutionX = "0.0";
$resolutionY = "0.0";

// Set Width and Height of barcode unit
$dimensionX = "0.0";
$dimensionY = "0.0";

// Set Location, Measurement of the code
$codeLocation = "Above";
$grUnit = "mm";

// Set if barcode's size will be updated automatically
$autoSize = "true";

// Height of the bar.
$barHeight = "50.0";

// Set height, Width and quality of the image.
$imageHeight = "0.0";
$imageWidth = "0.0";
$imageQuality = "default";

// Set Angle of barcode orientation
$rotAngle = "0.0";

// Set Margin of image border
$topMargin = "0.0";
$bottomMargin = "0.0";
$leftMargin = "0.0";
$rightMargin = "0.0";

// Sets if checksum will be added to barcode image.
$enableChecksum = "Yes";

// Set 3rd party cloud storage server (if any)
$storage = "";

// Set folder location at cloud storage
$folder = "";

// Set local file (if any)
$file = null;

try {
    // invoke Aspose.BarCode Cloud SDK API to generate image with specific bars height
    $response = $barcodeApi->PutBarcodeGenerateFile ( $name, $text, $type, $format, $resolutionX, $resolutionY, $dimensionX, $dimensionY, $codeLocation, $grUnit, $autoSize, $barHeight, $imageHeight, $imageWidth, $imageQuality, $rotAngle, $topMargin, $bottomMargin, $leftMargin, $rightMargin, $enableChecksum, $storage, $folder, $file );
    print_r ( $response );

    if ($response != null && $response->Status = "OK") {

        // download generated barcode from cloud storage
        $result = $storageApi->GetDownload ( $name );

        // Save response stream to a file
        $fileName = $out_folder . $name . "." . $format;
        $fh = fopen ( $fileName, 'w' ) or die ( 'cant open file' );
        fwrite ( $fh, $result );
        fclose ( $fh );

    echo "Barcode has been generated.";
    }
} catch ( \Aspose\Barcode\ApiException $exp ) {
    echo "Exception:" . $exp->getMessage ();
}
```

## Licensing

All Aspose.BarCode for Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-php/blob/HEAD/LICENSE).

[Product Page](https://products.aspose.cloud/barcode/php) | [Documentation](https://docs.aspose.cloud/display/barcodecloud/Home) | [Live Demo](https://products.aspose.app/barcode/family) | [API Reference](https://apireference.aspose.cloud/barcode/) [Code Samples](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-php) | [Blog](https://blog.aspose.cloud/category/barcode/) | [Free Support](https://forum.aspose.cloud/c/barcode) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
