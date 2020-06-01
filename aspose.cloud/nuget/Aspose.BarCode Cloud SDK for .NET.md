# Barcode Proecssing in the Cloud via REST API

This [cloud SDK assists you to seamlessly integrate barcode generation](https://products.aspose.cloud/barcode/net), processing & conversion functionality into your C#, ASP.NET & other .NET cloud apps.

Generate new barcodes (Linear, 2D & Postal), configure barcode properties and attributes, such as, barcode height, dimensions, image format, and more. Scan existing barcodes belonging to 60+ symbologies, including, `Codabar`, `PDF417`, `QR`, `MicroQR`, `EAN`, `Postnet`, `UPC`, `RM4SCC` and many more.

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

## Enhancements in Version 20.5

- Improved the Barcode recognition API.
- Exposed all Barcode-specific generator parameters to API.

For the detailed notes, please visit [Aspose.BarCode Cloud 20.5 Release Notes](https://docs.aspose.cloud/display/barcodecloud/Aspose.BarCode+Cloud+20.5+Release+Notes).

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

## Getting Started with Aspose.BarCode Cloud SDK for .NET

You do not need to install anything to get started with Aspose.BarCode Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.BarCode-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.BarCode Cloud assembly in your project. If you already have Aspose.BarCode Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.BarCode-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-dotnet) for other common usage scenarios.

## Using C# to Create a CodablockF Type Barcode

The following code snippet demonstrates how to create a CodablockF barcode using C# code:

```csharp
// please get your APP_KEY and APP_SID signing in https://dashboard.aspose.cloud/#/apps
BarcodeApi barcodeApi = new BarcodeApi(Common.APP_KEY, Common.APP_SID, Common.BASEPATH);

string text = "(01)23456789012";
string type = "codablockF";
string format = "jpg";
float? resolutionX = null;
float? resolutionY = null;
float? dimensionX = null;
float? dimensionY = null;
string enableChecksum = "";

ResponseMessage apiResponse = barcodeApi.GetBarcodeGenerate(text, type, format, resolutionX, resolutionY, dimensionX, dimensionY, enableChecksum);
```

[Product Page](https://products.aspose.cloud/barcode/net) | [Documentation](https://docs.aspose.cloud/display/barcodecloud/Home) | [Demo](https://products.aspose.app/barcode/family) | [API Reference](https://apireference.aspose.cloud/barcode/) | [Examples](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/barcode/) | [Free Support](https://forum.aspose.cloud/c/barcode) | [Free Trial](https://dashboard.aspose.cloud/#/apps)