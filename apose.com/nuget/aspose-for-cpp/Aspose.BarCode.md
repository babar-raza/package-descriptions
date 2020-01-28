Aspose.BarCode for C++ class library enables the developers to perform barcode generation, recognition and manipulation operation from within their own C++ applications.

You can modify and customize barcode properties, such as, font, foreground color, background color, alignment, barcode location, and barcode caption. Aspose.BarCode for C++ supports most of the popular barcode symbologies, including but not limited to, EAN13, EAN8, Code11, Codabar, Databar, Code128, GS1Code128, PDF417, QR, Micro QR etc. It supports both encoding and decoding of the supported symbologies.

## Barcode Generation Features
- Write 1D & 2D barcode types of 50+ symbologies.
- Customize barcode text, style & formatting.
- Support of X-dimension & Y-dimension for 2D barcodes.
- Support of wide to narrow ratio for selective symbologies.
- Exceptional optimization of Code128 encoding.
- Save barcode labels as images of popular formats including PNG, JPG, BMP and more.
- Encode non-english characters in 2D types.

## Barcode Scanning Features
- Read 1D & 2D barcode types of 50+ symbologies.
- Recognize codes from stream or image file.
- Scan a specific area of image to detect barcode.
- Get region information for the barcodes recognized in the image.
- Decode non-English characters in 2D types.

## Barcode Imaging Features
- Customize the barcode image's borders, border color, style, margins, width and so on.
- Customize barcode image's color, back color and bar color.
- Rotate barcode images to any angle.
- Generate high-quality barcode images with custom resolution.
- Support for anti-Aliasing.
- Specify size in inches and millimetres.
- Create barcode images in any desired image format like BMP, JPEG, GIF, PNG, TIFF.
- Create device resolution dependent images.

## Supported Barcode Symbologies
**Numeric Only:** EAN13,  EAN8, UPCA, UPCE, ISBN, ISMN, ISSN, Interleaved2of5,  Standard2of5, MSI, Code11, Codabar, Postnet, Planet, EAN14(SCC14), SSCC18, ITF14, IATA2of5, DatabarOmniDirectional, DatabarStackedOmniDirectional, DatabarExpandedStacked,   DatabarStacked, DatabarLimited, DatabarTruncated
**Alpha-Numeric:** GS1Code128, Code128, Code39 Extended, Code39 Standard, Code93 Extended, Code93 Standard, Australia Post, Italian Post 25, Matrix2of5, DatabarExpanded. PatchCode
**2D Symbologies:** PDF417, DataMatrix, Aztec, QR, MicroQR, GS1DataMatrix, Code16K, CompactPDF417, Swiss QR (QR Bill)

## Read & Write Barcode Labels
**Images:** JPEG, TIFF, PNG, BMP, GIF, EXIF

## Save Barcode Labels As
**Images:** EMF, SVG

## Generate Code128 Barcode in PNG Format
You can execute below code snippet to see how Aspose.BarCode API works in your development environment. You may also check the [GitHub Repository](https://github.com/aspose-barcode/Aspose.Barcode-for-C) for other common usage scenarios.

```c++
// instantiate barcode object and set CodeText & Barcode Symbology
System::SharedPtr<BarcodeGenerator> generator = System::MakeObject<BarcodeGenerator>(EncodeTypes::Code128, u"1234");
generator->Save(dir + u"output.png");
```

## Hide Barcode Label Text using C++
Aspose.BarCode for C++ allows you to customize various properties of barcodes, such as, borders, color, type, bar height as well as barcode text. Following example shows, how simple it is to hide the barcode text using C++:

```c++
System::String codeText = System::String(u"The quick brown fox jumps over the lazy dog\n") + u"The quick brown fox jumps over the lazy dog\n";

// instantiate barcode object and set CodeText, Symbology , and  CodeLocation
System::SharedPtr<BarcodeGenerator> generator = [&] { auto tmp_0 = System::MakeObject<BarcodeGenerator>(EncodeTypes::DataMatrix, codeText); 

tmp_0->get_Parameters()->get_Barcode()->get_CodeTextParameters()->set_Location(CodeLocation::None); return tmp_0; }();
generator->Save(dir + u"output.png", BarCodeImageFormat::Png);
```
[Product Page](https://products.aspose.com/barcode/cpp) | [Documentation](https://docs.aspose.com/display/barcodecpp/Home) | [API Reference](https://apireference.aspose.com/cpp/barcode) | [Code Examples](https://github.com/aspose-barcode/Aspose.Barcode-for-C) | [Blog](https://blog.aspose.com/category/barcode/) | [Free Support](https://forum.aspose.com/c/barcode) | [Temporary License](https://purchase.aspose.com/temporary-license)