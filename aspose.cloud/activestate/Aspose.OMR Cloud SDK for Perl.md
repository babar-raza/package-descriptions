# .NET REST API for OMR Processing

This Cloud SDK enables you to [perform Optical Mark Recognition (OMR)](https://products.aspose.cloud/omr/perl) operations on human-marked data from within your cloud-based C#, ASP.NET & other .NET apps.

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

You nee to install `Log::Any`, `URI::Query`, `Date::Parse` packages.

```console
ppm install Log::Any URI::Query Date::Parse
```

## Installation

- Clone repository with submodules

```console
git clone https://github.com/aspose-omr-cloud/aspose-omr-cloud-perl.git --recurse-submodules
```

## Optional requirements

To take full advantage of Aspose.OMR for Cloud, AsposeStorageCloud-StorageApi is required. Just `run ppm install AsposeStorageCloud-StorageApi`.

## Getting Started

Aspose.Cloud credentials are required to use Aspose.OMR for Cloud API. You can acquire App SID and App Key by registrating at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

### To load the API packages

```perl
use asposeomrcloud::OmrApi;
```

To load the models:

```perl
use asposeomrcloud::Object::AsposeResponse;
use asposeomrcloud::Object::FileInfo;
use asposeomrcloud::Object::OMRFunctionParam;
use asposeomrcloud::Object::OMRResponseDetails;
use asposeomrcloud::Object::OmrResponseContent;
use asposeomrcloud::Object::OmrResponseInfo;
use asposeomrcloud::Object::Payload;
use asposeomrcloud::Object::RecognitionStatistics;
use asposeomrcloud::Object::ServerStat;
use asposeomrcloud::Object::OMRResponse;
```

## Update submodule

Make sure you've cloned [aspose-omr-cloud-demo-data](https://github.com/aspose-omr-cloud/aspose-omr-cloud-demo-data) submodule, that contains all data required to run demo. In case you are missing submodules use the following git commands to initialize and update them:

```console
git submodule init
git submodule update --remote --merge
```

## Authentication

Library uses `OAUTH2` internally.

## Limitations

- Recognition process works well with the bubbles which are at least 75% filled.
- Works on perspective (side viewed/out of focus) & rotated images under certain conditions, e.g., rotation angle within 25 degrees.
- OMR operation will show results only in text format.
- Performing OCR operation is not supported for now.

[Product Page](https://products.aspose.cloud/omr/perl) | [Documentation](https://docs.aspose.cloud/display/omrcloud/Home) | [Live Demo](https://products.aspose.app/omr/family) | [API Reference](https://apireference.aspose.cloud/omr/) | [Code Samples](https://github.com/aspose-omr-cloud) | [Blog](https://blog.aspose.cloud/category/omr/) | [Free Support](https://forum.aspose.cloud/c/omr) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
