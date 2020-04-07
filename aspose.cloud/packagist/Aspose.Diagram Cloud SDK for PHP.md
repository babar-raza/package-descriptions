# PHP Cloud REST API for Visio Processing

This cloud SDK enables your PHP cloud apps to [create & process Visio diagrams](https://products.aspose.cloud/diagram/net) from within your apps without installing Microsoft Visio.

## Visio Processing Features

- Retrieve document information of a Visio diagram.
- Programmatically create a new Microsoft Visio diagram file.
- Convert Visio flow-charts to other supported formats.
- Upload your business oriented Visio diagrams to cloud storage.
- Export Visio files to raster images, fixed-layout and HTML formats.

## New Features in Version 19.10

- General enhancements to the Aspose.Diagram Cloud REST API.
- Added `SaveOption` parameter for `saveAs` API.
- Enhancement in the `Convert` API.
- Added support for multiple files exports that convert files to HTML.
- Integrated Aspose.Storage Cloud feature into Aspose.Diagram Cloud.

For the detailed notes, please visit [Aspose.Diagram Cloud 19.10 Release Notes](https://docs.aspose.cloud/display/diagramcloud/Aspose.Diagram+Cloud+19.10+Release+Notes).

## Read & Write Visio Formats

**Microsoft Visio:** VSDX, VSX, VTX, VDX, VSSX, VSTX, VSDM, VSSM, VSTM

## Save Visio As

**Fixed Layout:** PDF, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG, EMF
**Web:** HTML
**Other:** XAML, SWF

## Read Visio Formats

**Microsoft Visio:** VDW, VSD, VSS, VST

## How to use the SDK

The complete source code is available at the [GitHub Repository](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-php). You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/diagram-sdk-php) (recommended). For more details, please visit our [documentation website](https://docs.aspose.cloud/display/diagramcloud/Home).

## Prerequisites

To use Aspose Cells Cloud SDK you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Installation via Composer

*diagram-sdk-php* is available on [Packagist](https://packagist.org/packages/aspose/diagram-sdk-php) as the `diagram-sdk-php` package. Run the following command:

```console
composer require aspose/diagram-sdk-php
```

To use the SDK, use Composer's [autoload](https://getcomposer.org/doc/00-intro.md#autoloading):

```php
require_once('vendor/autoload.php');
```

## Examples

Please, look at [Examples](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-php/blob/master/EXAMPLES.md) document for basic usage or use the [Examples](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-php/blob/master/Examples) folder for more sophisticated scenarios.

## Use PHP Code to Convert VDX Diagram to other Formats

```php
require_once(__DIR__ . '/vendor/autoload.php');
require_once(__DIR__ . '/Utils.php');

use Aspose\Diagram\Cloud\Api\DiagramFileApi;
use \Aspose\Diagram\Cloud\Configuration;
use \Aspose\Diagram\Cloud\Model;
use \Aspose\Diagram\Cloud\ObjectSerializer;

class DiagramFile {

    public $diagramApi;

    public function __construct() {
        $this->diagramApi = new DiagramFileApi();
        $config = $this->diagramApi->getConfig();
        $token = Utils::getAccessToken();
        $config ->setAccessToken($token);
    }

    public function saveFileAsAnotherFormat() {
        $fileName ='file_get_1.vdx';
        $isOverwrite = 'true';
        $folder= "";
        $format = new \Aspose\Diagram\Cloud\Model\FileFormatRequest();
        $format->setFormat("pdf");
        $newfilename = "file_saveas_php.pdf";
        $result = $this->diagramApi->DiagramFilePostSaveAs($fileName, $format, $newfilename, $folder, $isOverwrite);
        $json = json_decode($result);
        print_r ( $json );
    }
}

$diagramFile = new DiagramFile();
$diagramFile->saveFileAsAnotherFormat();
```

[Product Page](https://products.aspose.cloud/diagram/php) | [Documentation](https://docs.aspose.cloud/display/diagramcloud/Home) | [Live Demo](https://products.aspose.app/diagram/family) | [API Reference](https://apireference.aspose.cloud/diagram/) | [Code Samples](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-php) | [Blog](https://blog.aspose.cloud/category/diagram/) | [Free Support](https://forum.aspose.cloud/c/diagram) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
