# C++ REST API to Process Presentation in Cloud

This REST API enables your C++ cloud-based apps to [process & manipulate PPT, PPTX, ODP, OTP presentations](https://products.aspose.cloud/cells/cpp) in the cloud.

## Presentation Processing Features

- Document format conversion among 20+ supported formats.
- Download slides and shapes in PDF, SVG & various other formats.
- PowerPoint presentation split and merge capability.
- Full access to perform read & write operations on Document Object Model (DOM).
- Fetch presentation statistics and metadata.
- Suport of Aspose Storage API.

## Read & Write Presentation Formats

**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX, PPTM, PPSM, POTX, POTM\
**OpenOffice:** ODP, OTP, FODP

## Save Presentation As

**Fixed Layout:** PDF, PDF/A, XPS\
**Images:** JPEG, PNG, BMP, TIFF, SVG\
**Web:** HTML\
**Other:** SWF (export whole presentations)

## Prerequisites

To use Aspose Slides Cloud SDK you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Installation

From the command line:

```console
nuget install aspose.slides.sdk.v141
```

From Package Manager:

```console
PM> Install-Package aspose.slides.sdk.v141
```

## Convert a PPTX File to PDF format using Aspose.Slides Cloud library

```c++
std::shared_ptr<asposeslidescloud::api::SlidesApi> api = std::make_shared<asposeslidescloud::api::SlidesApi>(utility::conversions::to_string_t("MyAppSid"), utility::conversions::to_string_t("MyAppKey"));
api->getSlidesApiInfo().get()->getName();
std::shared_ptr<PostSlidesConvertRequest> request = std::make_shared<PostSlidesConvertRequest>();
request->setFormat(utility::conversions::to_string_t("pdf"));
request->setDocument(std::make_shared<std::ifstream>("MyPresentation.pptx", std::ios::binary));
std::ofstream fs("MyPresentation.pdf", std::ios::binary);
api->postSlidesConvert().get().writeTo(versionStream);
```

[Product Page](https://products.aspose.cloud/cells/cpp) | [Documentation](https://docs.aspose.cloud/display/slidescloud/Home) | [Demo](https://products.aspose.app/slides/family) | [API Reference](https://apireference.aspose.cloud/slides/) | [Examples](https://github.com/aspose-slides-cloud/aspose-slides-cloud-cpp) | [Blog](https://blog.aspose.cloud/category/slides/) | [Free Support](https://forum.aspose.cloud/c/slides) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
