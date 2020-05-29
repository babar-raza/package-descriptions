# Barcode Generation & Recognition Library for .NET Applications

[Aspose.BarCode for .NET](https://products.aspose.com/barcode/net) doesn't just create or recognize barcodes but it provides a complete framework to control almost everything about barcodes. Developers can customization the barcode's appearance including bar height, color, margins, borders and so on. While scanning for barcode, developers can specify area where a barcode can be found as well as direct the engine to look for rotated barcodes.

## Barcode API Features

- [Generate](https://docs.aspose.com/display/barcodenet/Generate+Barcodes+with+Aspose.BarCode+APIs) & [recognize](https://docs.aspose.com/display/barcodenet/Read+Barcodes+with+Aspose.BarCode+APIs) 40+ barcode symbologies with just a few lines of code.
- Read 1D & 2D barcodes at any angle.
- Easily print barcode labels to physical or virtual printers.
- [Export barcode as XML](https://docs.aspose.com/display/barcodenet/Barcode+in+XML).
- Support for [barcode supplement data and checksum](https://docs.aspose.com/display/barcodenet/Use+Checksum+and+Supplement+Data).
- Optimized code128 encoding.
- Specify image area to scan barcode.
- Create device resolution dependent images.

## Enhancements in Version 20.4

- Option to set Barcode value while creating barcode of type *PatchCode*.

## Public API and Backward Incompatible Changes

- Added property `Aspose.BarCode.Generation.BarcodeParameters.PatchCode`
- Added class `Aspose.BarCode.Generation.PatchCodeParameters`
- Added property `Aspose.BarCode.Generation.PatchCodeParameters.ExtraBarcodeText`
- Added property `Aspose.BarCode.Generation.PatchCodeParameters.PatchFormat`
- Added method `Aspose.BarCode.Generation.PatchCodeParameters.ToString`
- Added type `Aspose.BarCode.Generation.PatchFormat`
- Added field `Aspose.BarCode.Generation.PatchFormat.PatchOnly`
- Added field `Aspose.BarCode.Generation.PatchFormat.A4`
- Added field `Aspose.BarCode.Generation.PatchFormat.A4_LANDSCAPE`
- Added field `Aspose.BarCode.Generation.PatchFormat.US_Letter`
- Added field `Aspose.BarCode.Generation.PatchFormat.US_Letter_LANDSCAPE`
- Added method `Aspose.BarCode.Metered.GetConsumptionCredit`

For the detailed notes, please visit [Aspose.BarCode for .NET 20.4 Release Notes](https://docs.aspose.com/display/barcodenet/Aspose.BarCode+for+.NET+20.4+Release+Notes).

## Barcode Symbologies

**Numeric Only:** EAN13,  EAN8, UPCA, UPCE, ISBN, ISMN, ISSN, Interleaved2of5,  Standard2of5, MSI, Code11, Codabar, Postnet, Planet, EAN14(SCC14), SSCC18, ITF14, IATA2of5, DatabarOmniDirectional, DatabarStackedOmniDirectional, DatabarExpandedStacked,   DatabarStacked, DatabarLimited, DatabarTruncated
**Alpha-Numeric:** GS1Code128, Code128, Code39 Extended, Code39 Standard, Code93 Extended, Code93 Standard, Australia Post, Italian Post 25, Matrix2of5, DatabarExpanded. PatchCode
**2D Symbologies:** PDF417, DataMatrix, Aztec, QR, MicroQR, GS1DataMatrix, Code16K, CompactPDF417, Swiss QR (QR Bill)

## Barcode Generation & Recognition Formats

**Images:** JPEG, TIFF, PNG, BMP, GIF, EXIF

## Save BarCode Labels As

**Images:** EMF, SVG

## Platform Independence

Aspose.BarCode for .NET can easily be used in any .NET 32-bit or 64-bit application, including, WinForms, WPF, ASP.NET, and .NET core. In short, you can develop apps using Aspose.BarCode for .NET where the .NET framework is available.

## Getting Started with Aspose.BarCode for .NET

Are you ready to give Aspose.BarCode for .NET a try? Simply execute `Install-Package Aspose.BarCode` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.BarCode for .NET and want to upgrade the version, please execute `Update-Package Aspose.BarCode` to get the latest version.

## Generate a Barcode Label with Code128

Try the following snippet to see how Aspose.BarCode API performs in your environment or check the [GitHub Repository](https://github.com/aspose-barcode/Aspose.BarCode-for-.NET) for other common usage scenarios.
```csharp
// instantiate object and set different barcode properties
BarcodeGenerator  generator = new BarcodeGenerator (EncodeTypes.Code128, "1234567");
generator.Parameters.Barcode.XDimension.Millimeters = 1f;

// save the image to your system and set its image format to Jpeg
generator.Save(dir + "output.jpg", BarCodeImageFormat.Jpeg);
```

## Hide Barcode Text from the PNG Label via C# Code

Aspose.BarCode for .NET allows you to customize various properties of barcodes, such as, borders, color, type, bar height as well as barcode text. Following example shows, how simple it is to hide the barcode text using C#.

```csharp
string codeText = "This text is hidden.\n" + "This text is hidden.\n"; ;

// instantiate barcode object and set CodeText, Symbology , and  CodeLocation
BarcodeGenerator  generator = new BarcodeGenerator(EncodeTypes.DataMatrix, codeText);
generator.Parameters.Barcode.CodeTextParameters.Location = CodeLocation.None;
generator.Save(dir + "output.png", BarCodeImageFormat.Png);
```

[Product Page](https://products.aspose.com/barcode/net) | [Docs](https://docs.aspose.com/display/barcodenet/Home) | [Demos](https://products.aspose.app/barcode/family) | [API Reference](https://apireference.aspose.com/barcode/net) | [Examples](https://github.com/aspose-barcode/Aspose.BarCode-for-.NET) | [Blog](https://blog.aspose.com/category/barcode/) | [Free Support](https://forum.aspose.com/c/barcode) | [Temporary License](https://purchase.aspose.com/temporary-license)
