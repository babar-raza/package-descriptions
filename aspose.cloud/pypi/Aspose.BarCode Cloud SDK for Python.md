# Process Barcodes in the Cloud via Python SDK

- `API version: 3.0`
- `Package version: 20.6.0`

[Aspose.BarCode for Cloud](https://products.aspose.cloud/barcode/cloud) is a REST API for Linear, 2D and postal barcode generation and recognition in the cloud. API recognizes and generates barcode images in a variety of formats. Barcode REST API allows to specify barcode image attributes like image width, height, border style and output image format in order to customize the generation process. Developers can also specify the barcode type and text attributes such as text location and font styles in order to suit the application requirements.

This repository contains Aspose.BarCode Cloud SDK for Python source code. This SDK allows you to work with Aspose.BarCode for Cloud REST APIs in your Python 2 or Python 3 applications quickly and easily.

## BarCode Processing Features

- [Generate](https://docs.aspose.cloud/display/barcodecloud/Generate%2C+Format+and+Manipulate+a+Barcode+using+Cloud+Storage#Generate,FormatandManipulateaBarcodeusingCloudStorage-SDKExamples), scan and customize `1D` (linear), `2D` and `postal` barcodes.
- Generate and recognize [barcodes with `checksum` option](https://docs.aspose.cloud/display/barcodecloud/Generate%2C+Format+and+Manipulate+a+Barcode+using+Cloud+Storage#Generate,FormatandManipulateaBarcodeusingCloudStorage-GenerateBarcodewithChecksumOption).
- Fetch barcode as an image stream or save barcode to the local disk.
- Configure barcode height, width, angle quality, margin & resolution.
- Configure barcode to be auto-sized or [set `X` & `Y` dimensions](https://docs.aspose.cloud/display/barcodecloud/Generate%2C+Format+and+Manipulate+a+Barcode+using+Cloud+Storage#Generate,FormatandManipulateaBarcodeusingCloudStorage-SetXandYDimensionsofaBarcode).
- Generate a new barcode with specified code text location.
- Apply bar height and barcode image format.
- Rotate barcode image at a certain angle & generate multiple barcodes.
- Scan image to recognize barcode from a specific region of that image.
- Recognize specified number of barcodes.
- Apply image processing algorithms to read barcodes.

## New Features & Enhancements in Version 20.8

- Added `patchCode.ExtraBarcodeText` & `patchCode.PatchFormat` parameters.

For the detailed notes, please visit [Aspose.BarCode Cloud 20.8 Release Notes](https://docs.aspose.cloud/display/barcodecloud/Aspose.BarCode+Cloud+20.8+Release+Notes).

## Read & Write BarCode Formats

JPEG, TIFF, PNG, BMP, GIF

## Save BarCode As

EMF, SVG

## Supported Barcode Symbologies

**Linear barcode symbologies**:
EAN13, EAN8, UPCA, UPCE, Interleaved2of5, Standard2of5, MSI, Code11, Codabar, EAN14(SCC14), SSCC18, ITF14, Matrix 2 of 5, PZN, Code128, Code39 Extended, Code39 Standard, Code93 Extended, Code16K, Code93 Standard, IATA 2 of 5, OPC, GS1Code128, ISBN, ISMN, ISSN, ITF6, VIN, Pharmacode, DatabarOmniDirectional, DatabarTruncated, DatabarLimited, DatabarExpanded, DatabarStackedOmniDirectional, DatabarExpandedStacked, DatabarStacked, PatchCode, Supplement (Decode only).

**2D barcode symbologies**:
PDF417, MacroPDF417, MicroPDF417, CompactPDF417 (Decode only), DataMatrix, Aztec, QR, MicroQR, DotCode, MaxiCode, Italian Post 25, GS1DataMatrix, Code16K.

**Postal barcode symbologies**:
Postnet, Planet, USPS OneCode, Australia Post, Deutsche Post Identcode, Deutsche Post Leticode, RM4SCC, SingaporePost, AustralianPosteParcel, SwissPostParcel, UpcaGs1DatabarCoupon.

## Getting Started with Aspose.BarCode Cloud SDK for Python

To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) (free registration in Aspose Cloud is required for this).

## How to use the SDK

The complete source code is available in this repository folder. You can either directly use it in your project via source code or get [from PyPi](https://pypi.org/project/aspose-barcode-cloud/) (*recommended*).

## Prerequisites

To use Aspose.BarCode Cloud SDK for Python you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Supported Python versions

- `Python 2.7`
- `Python 3.4+`

## Requirements

- `six >= 1.10`
- `urllib3 >= 1.15.1`

## Installation

### Install aspose-barcode-cloud via pip

From the *command line*:

```sh
pip install aspose-barcode-cloud
```

Then *import* the package:

```python
import aspose_barcode_cloud
```

## Sample usage

The examples below show how you can generate and recognize `Code128` barcode and save it into local file using aspose-barcode-cloud:

```python
from __future__ import print_function

from pprint import pprint

import aspose_barcode_cloud
from aspose_barcode_cloud.rest import ApiException

# Configure OAuth2 access token for authorization: JWT
configuration = aspose_barcode_cloud.Configuration(
    app_sid="App SID from https://dashboard.aspose.cloud/#/apps",
    app_key="App Key from https://dashboard.aspose.cloud/#/apps",
)

# create an instance of the API class
api = aspose_barcode_cloud.BarcodeApi(aspose_barcode_cloud.ApiClient(configuration))
type = aspose_barcode_cloud.EncodeBarcodeType.CODE128  # str | Type of barcode to generate.
text = 'text_example'  # str | Text to encode.

try:
    # Generate barcode.
    response = api.get_barcode_generate(type, text)
    with open('example.png', 'wb') as f:
        f.write(response.data)
    print("Barcode saved to file 'example.png'")
except ApiException as e:
    print("Exception when calling BarcodeApi->get_barcode_generate: %s\n" % e)


# Recognize barcode
response = api.post_barcode_recognize_from_url_or_content(image='example.png',
                                                          preset=aspose_barcode_cloud.PresetType.HIGHPERFORMANCE)
pprint(response)
```

## Licensing

All Aspose.BarCode for Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-python/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/barcode/python) | [Docs](https://docs.aspose.cloud/display/barcodecloud/Home) | [Demos](https://products.aspose.app/barcode/family) | [API Reference](https://apireference.aspose.cloud/barcode/) | [Examples](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-python) | [Blog](https://blog.aspose.cloud/category/barcode/) | [Free Support](https://forum.aspose.cloud/c/barcode) | [Free Trial](https://dashboard.aspose.cloud/#/apps)