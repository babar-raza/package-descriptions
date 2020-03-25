# PHP REST API to Process Presentation in Cloud

This REST API enables your PHP cloud-based apps to [process & manipulate PPT, PPTX, ODP, OTP presentations](https://products.aspose.cloud/slides/net) in the cloud.

## Presentation Processing Features

- Fetch presentation images in any of the supported file formats.
- Copy layout side or clone master slide from the source presentation.
- Process slides shapes, slides notes, placeholders, colors & font theme info.
- Programmatically create presentation from HTML & export it to various formats.
- Merge multiple presentations or split single presentation into multiple ones.
- Extract and replace text from specific slide or entire presentation.

## Enhancements & Changes in Version 20.2

- Do not include empty & default field values in `JSON` response for Chart shape object.

For the detailed notes, please visit [Aspose.Slides Cloud 20.2 Release Notes](https://docs.aspose.cloud/display/slidescloud/Aspose.Slides+Cloud+20.2+Release+Notes).

## Read & Write Presentation Formats

**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX, PPTM, PPSM, POTX, POTM
**OpenOffice:** ODP, OTP

## Save Presentation As

**Fixed Layout:** PDF, PDF/A, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Web:** HTML
**Other:** SWF (export whole presentations)

## Platform Independence

Aspose.Slides Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.Slides Cloud SDK for PHP

This repository contains Aspose.Slides Cloud SDK for PHP source code. To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) ([free registration](https://id.containerize.com/signup?clientId=prod.discourse.aspose&redirectUrl=https://forum.aspose.cloud/session/sso) is required).

Please check the [GitHub Repository](https://github.com/aspose-slides-cloud/aspose-slides-cloud-php) for the source code and examples.

## How to use the SDK

You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/slides-sdk-php) (recommended).

## Installation

From the command line:

```console
composer require aspose/slides-sdk-php
```

## Convert a PPTX document to PDF format using PHP Code

The example code below uses the `slides-sdk-php` library:

```php
use Aspose\Slides\Cloud\Sdk\Api\Configuration;
use Aspose\Slides\Cloud\Sdk\Api\SlidesApi;
use Aspose\Slides\Cloud\Sdk\Model\ExportFormat;
use Aspose\Slides\Cloud\Sdk\Model\Requests\PostSlidesConvertRequest;

$config = new Configuration();
$config->setAppSid("MyAppSid");
$config->setAppKey("MyAppKey");
$api = new SlidesApi(null, $config);
$request = new PostSlidesConvertRequest(ExportFormat::PDF, fopen("MyPresentation.pptx", 'r'));
$result = $api->postSlidesConvert($request);
echo "My PDF was saved to " . $result->getPathname();
```

[Product Page](https://products.aspose.cloud/slides/net) | [Documentation](https://docs.aspose.cloud/display/slidescloud/Home) | [API Reference](https://apireference.aspose.cloud/slides/) | [Code Samples](https://github.com/aspose-slides-cloud/aspose-slides-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/slides/) | [Free Support](https://forum.aspose.cloud/c/slides) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
