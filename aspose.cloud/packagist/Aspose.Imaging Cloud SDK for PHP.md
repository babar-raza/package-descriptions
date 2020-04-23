# Image Processing in Cloud via PHP REST API

This cloud SDK assists to [process & manipulate images](https://products.aspose.cloud/imaging/net) from within your PHP based cloud applications, without installing any 3rd party tool.

## Image Processing Features

- Fetch or update properties of cloud hosted images.
- Scale, flip, crop and export an image with a single API call.
- Resize, crop, flip, convert and export an image to other supported formats.
- Update image parameters of JPEG2000 & WEBP images.
- Access and multi-frame TIFF image and extract the desired frames from it.
- Rotate, flip, crop, resize or fetch properties of the selected TIFF frame.
- Merge multiple TIFF images.

## New Features in Version 20.2

- Support for image grayscale feature.

For the detailed notes, please visit [Aspose.Imaging Cloud 20.2 - Release Notes](https://docs.aspose.cloud/display/imagingcloud/Aspose.Imaging+Cloud+20.2+-+Release+Notes).

## Read & Write Image Formats

BMP, GIF, JPEG, JPEG2000, PSD, TIFF, WEBP, PNG, WMF, EMF, SVG

## Save Image As

PDF

## Read Image Formats

DJVU, DICOM, CDR, CMX, ODG, DNG

## Dependencies

- PHP 5.6 or later

## Getting Started

- Sign Up. Before you begin, you need to sign up for an account on our [Dashboard](https://dashboard.aspose.cloud/) and retrieve your [credentials](https://dashboard.aspose.cloud/#/apps).
- Minimum requirements. This SDK requires [PHP 5.6 or later](https://www.php.net/releases/).
- Install Aspose.Imaging Cloud PHP SDK. Please, add the following [Packagist package](https://packagist.org/packages/aspose/aspose-imaging-cloud) to your project.

Please, add the following to your *composer.json* as a dependency.

```php
{
    "require": {
        "aspose/aspose-imaging-cloud": ">=20.2"
    }
}
```

Import the dependencies to your code as follows:

```php
use \Aspose\Imaging\ImagingApi;
use \Aspose\Imaging\Configuration;
use \Aspose\Imaging\Model;
use \Aspose\Imaging\Model\Requests;
```

- Using the SDK. The best way to become familiar with how to use the SDK is to read the Developer Guide. The Getting Started Guide will help you to become familiar with the common concepts.

## Examples

Please, look at [Examples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-php/blob/master/EXAMPLES.md) document for basic usage or use the [Examples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-php/blob/master/Examples) folder for more sophisticated scenarios.

## Resize PSD Image using PHP Code

```php
namespace Aspose\Imaging\Examples;

use Aspose\Imaging\Model\Requests\CreateResizedImageRequest;
use Aspose\Imaging\Model\Requests\ResizeImageRequest;

class ResizeImage extends ImagingBase
{
    function __construct($imagingApi)
    {
        parent::__construct($imagingApi);
        $this->PrintHeader("Resize an image example");
    }

    /**
     * Resizes the image.
     */
    public function ResizeImageFromStorage()
    {
        echo "Resize an image from cloud storage" . PHP_EOL;

        // Upload local image to Cloud Storage
        $this->UploadSampleImageToCloud();

        // Please refer to https://docs.aspose.cloud/display/imagingcloud/Supported+File+Formats#SupportedFileFormats-Resize
        // for possible output formats
        $format = "gif";
        $newWidth = 100;
        $newHeight = 150;
        $folder = $this->CloudPath; // Input file is saved at the Examples folder in the storage
        $storage = null; // We are using default Cloud Storage

        $resizeImageRequest = new ResizeImageRequest($this->GetSampleImageFileName(), $newWidth, $newHeight, $format,
            $folder, $storage);
        echo "Call ResizeImage with params: new width: ${newWidth}, new height: ${newHeight}, $format: ${format}" . PHP_EOL;

        $updatedImage = self::$imagingApi->resizeImage($resizeImageRequest);
        $this->SaveUpdatedSampleImageToOutput($updatedImage, false);

        echo PHP_EOL;
    }

    /**
     * Gets the name of the example image file.
     * @return string
     */
    protected function GetSampleImageFileName()
    {
        return "ResizeSampleImage.psd";
    }
}
```

## Licensing

All Aspose.Imaging Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-php/blob/HEAD/LICENSE).

[Product Page](https://products.aspose.cloud/imaging/net) | [Documentation](https://docs.aspose.cloud/display/imagingcloud/Home) | [Live Demo](https://products.aspose.app/imaging/family) | [API Reference](https://apireference.aspose.cloud/imaging/) | [Examples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/imaging/) | [Free Support](https://forum.aspose.cloud/c/imaging) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
