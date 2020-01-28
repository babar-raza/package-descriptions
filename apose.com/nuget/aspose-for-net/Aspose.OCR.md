It is a standalone OCR API that enhances your .NET apps to perform the OCR operation on JPEG, PNG, GIF, BMP & TIFF images for extraction of English, French, Spanish & Portuguese content.

Aspose.OCR for .NET not only provides the Optical Character Recognition engine but more. You can also apply Blur, Gaussian Blur, and Median filter to reduce noise before document recognition and can set the OcrEngine to ignore non-textual blocks, maintain correct text order during document text recognition & automatically correct spellings of the document text.

## Image OCR API Features
- Programmatically detect, identify and read characters from images.
- Support English, French, Spanish and Portuguese text.
- Detect and read popular font faces such as Arial, Times New Roman, Courier New, Tahoma, Calibri & Verdana.
- Supports regular, bold and italic font styles.
- Scan whole image or only a specific portion of the image.
- Scan rotated images.
- Application of various noise removal filters to assist image recognition.

## Read Image Formats for OCR
**Raster Formats:** JPEG, PNG, GIF, BMP, TIFF

## Platform Independence
You can use Aspose.OCR for .NET to develop applications in any development environment that targets the .NET Framework 2.0 and higher. This includes support for Mono and Client Profiles. 

## Getting Started with Aspose.OCR for .NET
Are you ready to give Aspose.OCR for .NET a try? Simply execute `Install-Package Aspose.OCR` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.OCR for .NET and want to upgrade the version, please execute `Update-Package Aspose.OCR` to get the latest version.

Execute the following code snippet to see how Aspose.OCR API performs with your own samples or check the [GitHub Repository](https://github.com/aspose-ocr/Aspose.OCR-for-.NET) for other common usage scenarios. 

## Perform simple OCR on a BMP image for text extraction using C#.
```csharp
// initialize an instance of OcrEngine
OcrEngine ocrEngine = new OcrEngine();
// set the Image property by loading the image from file path location or an instance of MemoryStream 
ocrEngine.Image = ImageStream.FromFile(dataDir + "template.bmp");
// process the image
ocrEngine.Process();
// display the recognized text
Console.WriteLine(ocrEngine.Text);
```

## Load a Remote Image for OCR Operation
Aspose.OCR for .NET enables your .NET applications to perform OCR in various scenarios such as accessing a remote JPG image via URL.
```csharp
// initialize an instance of OcrEngine
OcrEngine ocrEngine = new OcrEngine();
// set the Image property by loading the image from remote location
ocrEngine.Image = ImageStream.FromUrl("https://blog.aspose.com/wp-content/uploads/sites/2/2019/03/SampleTextOnline.jpg");
// run recognition process
ocrEngine.Process();
// display the recognized text
Console.WriteLine(ocrEngine.Text);
```

[Product Page](https://products.aspose.com/ocr/net) | [Documentation](https://docs.aspose.com/display/ocrnet/Home) | [API Reference](https://apireference.aspose.com/net/ocr) | [Code Examples](https://github.com/aspose-ocr/Aspose.OCR-for-.NET) | [Blog](https://blog.aspose.com/category/ocr/) | [Free Support](https://forum.aspose.com/c/ocr) |  [Temporary License](https://purchase.aspose.com/temporary-license)