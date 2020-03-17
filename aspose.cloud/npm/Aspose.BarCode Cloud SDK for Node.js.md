Node.js Cloud SDK wraps Aspose.BarCode Cloud API so you could seamlessly integrate Barcode Generation & Recognition features into your own Node.js apps.

# Barcode Generation & Recognition in the Cloud

[Aspose.BarCode Cloud SDK for Node.js](https://products.aspose.cloud/barcode/nodejs) helps you generate barcodes (Linear, 2D & Postal), configure barcode properties and attributes, such as, barcode height, dimensions, image format, and more. Scan existing barcodes from 60+ symbologies, including, Codabar, PDF417, QR, MicroQR, EAN, Postnet, UPC, RM4SCC and many more.

## Barcode Read & Write Features

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

## Generate & Recognize Barcode As

JPEG, TIFF, PNG, BMP, GIF

## Save BarCode Labels As

EMF, SVG

## Supported Barcode Symbologies

**Linear Barcode Symbologies**:

EAN13, EAN8, UPCA, UPCE, Interleaved2of5, Standard2of5, MSI, Code11, Codabar, EAN14(SCC14), SSCC18, ITF14, Matrix 2 of 5, PZN, Code128, Code39 Extended, Code39 Standard, Code93 Extended, Code16K, Code93 Standard, IATA 2 of 5, OPC, GS1Code128, ISBN, ISMN, ISSN, ITF6, VIN, Pharmacode, DatabarOmniDirectional, DatabarTruncated, DatabarLimited, DatabarExpanded, DatabarStackedOmniDirectional, DatabarExpandedStacked, DatabarStacked, PatchCode, Supplement (Decode only).

**2D Barcode Symbologies**:

PDF417, MacroPDF417, MicroPDF417, CompactPDF417 (Decode only), DataMatrix, Aztec, QR, MicroQR, DotCode, MaxiCode, Italian Post 25, GS1DataMatrix, Code16K.

**Postal Barcode Symbologies**:

Postnet, Planet, USPS OneCode, Australia Post, Deutsche Post Identcode, Deutsche Post Leticode, RM4SCC, SingaporePost, AustralianPosteParcel, SwissPostParcel, UpcaGs1DatabarCoupon.

## Getting Started with Aspose.BarCode Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install aspose-barcode-cloud-node --save` from the command line to install Aspose.BarCode Cloud SDK for Node.js via NPM.

The complete source code is available at [GitHub Repository](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-node).

## Using Node.js to Generate PDF417 Barcode

```js
const { barcode, fs } = require("aspose-barcode-cloud-node", "fs");
var api = new barcode.BarCodeApi(AppSid, AppKey);
api.barCodeGetBarCodeGenerate("Aspose.BarCode for Cloud Sample", "Pdf417", "png").then((apiResult) => {
       if (apiResult.response.statusCode == 200) {
           fs.writeFile("output.png", apiResult.body);
       }
});
```

## Send Barcode Image in Request for Scanning via Node.js

```js
var config = {'appSid':AppSID,'apiKey':AppKey , 'debug' : true};
var storageApi = new StorageApi(config);
var barcodeApi = new BarcodeApi(config);
var name = "template.jpeg";

storageApi.PutCreate(name  , null, null, data_path + name  , function(responseMessage) 
{
	barcodeApi.PostBarcodeRecognizeFromUrlorContent(null, null, null, null, null, data_path + name, function(responseMessage) 
	{
		responseMessage.body.Barcodes.forEach(function(barcode)
		{
			console.log("Type :: " + barcode.BarcodeType);
			console.log("Codetext :: " + barcode.BarcodeValue);
		});
	});
});
```

[Product Page](https://products.aspose.cloud/barcode/nodejs) | [Documentation](https://docs.aspose.cloud/display/barcodecloud/Home) | [API Reference](https://apireference.aspose.cloud/barcode/) | [Code Samples](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-node) | [Blog](https://blog.aspose.cloud/category/barcode/) | [Free Support](https://forum.aspose.cloud/c/barcode) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
