# Barcode Proecssing in the Cloud via REST API

This [cloud SDK assists you to seamlessly integrate barcode generation](https://products.aspose.cloud/barcode/go), processing & conversion functionality into your cloud apps developed using Golang.

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

## Getting Started

To use [Aspose.BarCode Cloud SDK for Go](https://products.aspose.cloud/barcode/go) you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is a free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

Please check the [GitHub Repository](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-go/) for common usage scenarios.

## Dependencies

- `github.com/antihax/optional`
- `github.com/google/uuid`
- `golang.org/x/oauth2`


## Installation

### Using Go Modules (recommended)

- Go to existing module directory, or [create a new module](https://blog.golang.org/using-go-modules).
- Run `go get` command.
  `go get -u github.com/aspose-barcode-cloud/aspose-barcode-cloud-go@v0.2006.1`

### Using GOPATH (for Go < 1.11 )

- Run `go get` command outside module directory.
  `go get -u github.com/aspose-barcode-cloud/aspose-barcode-cloud-go/barcode`

## Generate an Image with Barcode using Golang

The examples below shows how to generate `QR` barcode and save it into a local file:

```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-barcode-cloud/aspose-barcode-cloud-go/barcode"
    "github.com/aspose-barcode-cloud/aspose-barcode-cloud-go/barcode/jwt"
    "os"
)

func main() {
    jwtConf := jwt.NewConfig(
        "App SID from https://dashboard.aspose.cloud/#/apps",
        "App Key from https://dashboard.aspose.cloud/#/apps",
    )
    fileName := "testdata/generated.png"

    authCtx := context.WithValue(context.Background(),
        barcode.ContextJWT,
        jwtConf.TokenSource(context.Background()))

    client := barcode.NewAPIClient(barcode.NewConfiguration())

    data, _, err := client.BarcodeApi.GetBarcodeGenerate(authCtx,
        string(barcode.EncodeBarcodeTypeQR),
        "Go SDK example",
        nil)
    if err != nil {
        panic(err)
    }

    out, err := os.Create(fileName)
    if err != nil {
        panic(err)
    }
    defer out.Close()

    written, err := out.Write(data)
    if err != nil {
        panic(err)
    }

    fmt.Printf("Written %d bytes to file %s\n", written, fileName)
}
```

## Licensing

All Aspose.BarCode for Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-go/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/barcode/go) | [Documentation](https://docs.aspose.cloud/display/barcodecloud/Home) | [Demo](https://products.aspose.app/barcode/family) | [API Reference](https://apireference.aspose.cloud/barcode/) | [Examples](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-go/) | [Blog](https://blog.aspose.cloud/category/barcode/) | [Free Support](https://forum.aspose.cloud/c/barcode) | [Free Trial](https://dashboard.aspose.cloud/#/apps)