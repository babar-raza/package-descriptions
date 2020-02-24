This cloud SDK assists you to seamlessly integrate barcode generation, processing & conversion functionality into your Node.js cloud apps.

Generate new barcodes (Linear, 2D & Postal), configure barcode properties and attributes, such as, barcode height, dimensions, image format, and more. Scan existing barcodes belonging to 60+ symbologies, including, Codabar, PDF417, QR, MicroQR, EAN, Postnet, UPC, RM4SCC and many more.

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

**Linear barcode symbologies**:
EAN13, EAN8, UPCA, UPCE, Interleaved2of5, Standard2of5, MSI, Code11, Codabar, EAN14(SCC14), SSCC18, ITF14, Matrix 2 of 5, PZN, Code128, Code39 Extended, Code39 Standard, Code93 Extended, Code16K, Code93 Standard, IATA 2 of 5, OPC, GS1Code128, ISBN, ISMN, ISSN, ITF6, VIN, Pharmacode, DatabarOmniDirectional, DatabarTruncated, DatabarLimited, DatabarExpanded, DatabarStackedOmniDirectional, DatabarExpandedStacked, DatabarStacked, PatchCode, Supplement (Decode only).

**2D barcode symbologies**:
PDF417, MacroPDF417, MicroPDF417, CompactPDF417 (Decode only), DataMatrix, Aztec, QR, MicroQR, DotCode, MaxiCode, Italian Post 25, GS1DataMatrix, Code16K.

**Postal barcode symbologies**:
Postnet, Planet, USPS OneCode, Australia Post, Deutsche Post Identcode, Deutsche Post Leticode, RM4SCC, SingaporePost, AustralianPosteParcel, SwissPostParcel, UpcaGs1DatabarCoupon.

## Platform Independence

Aspose.BarCode Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.BarCode Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.BarCode for Cloud via NPM, please execute from the command line, `npm install aspose-barcode-cloud-node --save`.

## Using C# to Generate PDF417 Barcode

```js
const { barcode, fs } = require("aspose-barcode-cloud-node", "fs");

var api = new barcode.BarCodeApi(AppSid, AppKey);

api.barCodeGetBarCodeGenerate("Aspose.BarCode for Cloud Sample", "Pdf417", "png").then((apiResult) => {
       if (apiResult.response.statusCode == 200) {
           fs.writeFile("out.png", apiResult.body);
           console.log("Saved to out.png ");
       }
});
```

[Product Page](https://products.aspose.cloud/barcode/nodejs) | [Documentation](https://docs.aspose.cloud/display/barcodecloud/Home) | [API Reference](https://apireference.aspose.cloud/barcode/) | [Code Samples](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-node) | [Blog](https://blog.aspose.cloud/category/barcode/) | [Free Support](https://forum.aspose.cloud/c/barcode) | [Free Trial](https://dashboard.aspose.cloud/#/apps)