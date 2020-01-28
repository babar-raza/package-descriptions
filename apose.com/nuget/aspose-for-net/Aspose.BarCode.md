A standalone C# library to help developers generate, recognize, customize & format 1D & 2D barcodes (40+ symbologies) from within .NET based applications.

Aspose.BarCode for .NET doesn't just create or recognize barcodes but it provides a complete framework to control almost everything about them. Developers can customization the barcode's appearance including bar height, color, margins, borders and so on. While scanning for barcode, developers can specify area where a barcode can be found as well as direct the engine to look for rotated barcodes.

## Barcode API Features
- Generate & recognize 40+ barcode symbologies
- Read 1D & 2D barcodes at any angle.
- Easily print barcode labels to physical or virtual printers.
- Format barcode text.
- Support for supplement data and checksum.
- Optimized code128 encoding.
- Specify image area to scan barcode.
- Create device resolution dependent images.

## Barcode Symbologies
**Numeric Only:** EAN13,  EAN8, UPCA, UPCE, ISBN, ISMN, ISSN, Interleaved2of5,  Standard2of5, MSI, Code11, Codabar, Postnet, Planet, EAN14(SCC14), SSCC18, ITF14, IATA2of5, DatabarOmniDirectional, DatabarStackedOmniDirectional, DatabarExpandedStacked,   DatabarStacked, DatabarLimited, DatabarTruncated
**Alpha-Numeric:** GS1Code128, Code128, Code39 Extended, Code39 Standard, Code93 Extended, Code93 Standard, Australia Post, Italian Post 25, Matrix2of5, DatabarExpanded. PatchCode
**2D Symbologies:** PDF417, DataMatrix, Aztec, QR, MicroQR, GS1DataMatrix, Code16K, CompactPDF417, Swiss QR (QR Bill)

## Barcode Generation & Recognition Formats
**Images:** JPEG, TIFF, PNG, BMP, GIF, EXIF

## Save BarCode Labels As
**Images:** EMF, SVG

## Platform Independence
Aspose.BarCode for .NET can easily be used in any .NET 32-bit or 64-bit application, including, WinForms, WPF, ASP.NET, and .NET core. In short, you can easily develop apps using Aspose.BarCode for .NET where the .NET framework is available.

## Getting Started with Aspose.BarCode for .NET
Are you ready to give Aspose.BarCode for .NET a try? Simply execute `Install-Package Aspose.BarCode` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.BarCode for .NET and want to upgrade the version, please execute `Update-Package Aspose.BarCode` to get the latest version.

### Generate a Barcode Label with Code128
Try the following snippet to see how Aspose.BarCode API performs in your environment or check the [GitHub Repository](https://github.com/aspose-barcode/Aspose.BarCode-for-.NET) for other common usage scenarios.
```csharp
// instantiate object and set different barcode properties
BarcodeGenerator  generator = new BarcodeGenerator (EncodeTypes.Code128, "1234567");
generator.Parameters.Barcode.XDimension.Millimeters = 1f;

// save the image to your system and set its image format to Jpeg
generator.Save(dir + "output.jpg", BarCodeImageFormat.Jpeg);
```

### Hide Barcode Text from the PNG Label via C#
Aspose.BarCode for .NET allows you to customize various properties of barcodes, such as, borders, color, type, bar height as well as barcode text. Following example shows, how simple it is to hide the barcode text using C#.
```csharp
string codeText = "This text is hidden.\n" + "This text is hidden.\n"; ;

// instantiate barcode object and set CodeText, Symbology , and  CodeLocation
BarcodeGenerator  generator = new BarcodeGenerator(EncodeTypes.DataMatrix, codeText);
generator.Parameters.Barcode.CodeTextParameters.Location = CodeLocation.None;
generator.Save(dir + "output.png", BarCodeImageFormat.Png);
```
[Product Page](https://products.aspose.com/barcode/net) | [Documentation](https://docs.aspose.com/display/barcodenet/Home) | [API Reference](https://apireference.aspose.com/net/barcode) | [Code Examples](https://github.com/aspose-barcode/Aspose.BarCode-for-.NET) | [Blog](https://blog.aspose.com/category/barcode/) | [Free Support](https://forum.aspose.com/c/barcode) | [Temporary License](https://purchase.aspose.com/temporary-license)