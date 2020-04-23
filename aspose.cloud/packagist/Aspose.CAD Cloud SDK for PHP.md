# AutoCAD File Processing PHP Cloud REST API

This Cloud SDK helps you perform [AutoCAD drawing conversion, processing & manipulation](https://products.aspose.cloud/cad/php) from within your PHP cloud apps without AutoCAD.

## CAD Processing Features

- Export CAD drawings to other file formats.
- Get image properties of a CAD drawing.
- Change scale of an AutoCAD sketch.
- Flip and rotate a CAD image.
- Upload or download CAD drawings to the cloud storage.
- Copy, move, delete CAD files from the cloud storage.

## Read & Write CAD Formats

DXF (R12/2007/2010)

## Save CAD As

**Fixed Layout:** PDF (as a vector and as a raster)
**Images:** BMP, PNG, JPG, JPEG, JPEG2000, TIF, TIFF, PSD, GIF, WMF

## Read CAD Formats

DWG (13, 14, 2000, 2004), DWG (2010, 2013, 2014), DWG (2015, 2017, 2018), DWT (13, 14, 2000, 2004), DWT (2010, 2013, 2014), DWT (2015, 2017, 2018), DWF, DGN v7, IGES (IGS), PLT, Industry Foundation Classes (IFC), STereoLithography (STL)

## How to use the SDK

The complete source code is available at the [GitHub Repository](https://github.com/aspose-cad-cloud/aspose-cad-cloud-php). You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/cad-sdk-php) (recommended). For more details, please visit our [documentation website](https://docs.aspose.cloud/display/cadcloud/Available+SDKs).

## Prerequisites

To use Aspose CAD for Cloud PHP SDK you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Dependencies

- PHP 5.6 or later
- referenced packages (see [here](https://github.com/aspose-cad-cloud/aspose-cad-cloud-php/blob/master/composer.json) for more details)

## Installation via Composer

*cad-sdk-php* is available on Packagist as the `cad-sdk-php` package. Run the following command:

```console
composer require aspose/cad-sdk-php
```

To use the SDK, use Composer's [autoload](https://getcomposer.org/doc/00-intro.md#autoloading):

```php
require_once('vendor/autoload.php');
```

## PHP Code to Convert CAD Drawing to Raster Image

```php
public function getDrawingSaveAs()
    {
        $localName = "galeon.stl";
        $outputFormat = "jpg";
        $remoteName = $localName;
        $subfolder = "";
        $fullName = self::$baseRemoteFolder . $subfolder . $remoteName;
        $destName = self::$baseTestOut . $remoteName ."." . $outputFormat;

        $file = realpath(__DIR__ . self::$relativeRootPath) . '/TestData/' . $localName;
        $putRequest = new \Aspose\Storage\Model\Requests\PutCreateRequest($fullName, $file);
        $this->storage->PutCreate($putRequest);

        $request = new \Aspose\CAD\Model\Requests\GetDrawingSaveAsRequest($remoteName, $outputFormat, $folder=trim(self::$baseRemoteFolder . $subfolder), null, null);

        list($response, $code, $headers) = $this->CAD->getDrawingSaveAsWithHttpInfo($request);
        Assert::assertEquals(200, $code);
    }
```

[Tests](https://github.com/aspose-cad-cloud/aspose-cad-cloud-php/blob/master/tests/Aspose/cad) contain various examples of using the SDK. Please put your credentials into [Configuration](https://github.com/aspose-cad-cloud/aspose-cad-cloud-php/blob/master/src/Aspose/cad/Configuration.php).

[Product Page](https://products.aspose.cloud/cad/php) | [Documentation](https://docs.aspose.cloud/display/cadcloud/Home) | [Demo](https://products.aspose.app/cad/family) | [API Reference](https://apireference.aspose.cloud/cad/) | [Examples](https://github.com/aspose-cad-cloud/aspose-cad-cloud-php) | [Blog](https://blog.aspose.cloud/category/cad/) | [Free Support](https://forum.aspose.cloud/c/cad) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
