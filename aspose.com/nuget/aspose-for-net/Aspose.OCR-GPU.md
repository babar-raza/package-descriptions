# OCR Processing via GPU

It is an OCR API that enhances your .NET apps to perform the image recognition using `GPU` and `CUDA` technology.

## GPU OCR API Features

- Programmatically [detect, identify and read characters](https://docs.aspose.com/ocr/net/performing-ocr-on-an-image/) from images.
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

Are you ready to give Aspose.OCR for .NET a try? Simply execute `Install-Package Aspose.OCR-GPU` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.OCR for .NET and want to upgrade the version, please execute `Update-Package Aspose.OCR-GPU` to get the latest version.

Execute the following code snippet to see how Aspose.OCR API performs with your own samples or check the [GitHub Repository](https://github.com/aspose-ocr/Aspose.OCR-for-.NET) for other common usage scenarios.

## Perform OCR on PNG Image via C# Code

```csharp
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_OCR();

// Initialize an instance of AsposeOcr
AsposeOcr api = new AsposeOcr();

// Recognize image
string result = api.RecognizeImage(dataDir + "sample.png");

// Display the recognized text
Console.WriteLine(result);
```

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/ocr/net) | [Docs](https://docs.aspose.com/ocr/net/) | [Demos](https://products.aspose.app/ocr/family) | [API Reference](https://apireference.aspose.com/ocr/net) | [Examples](https://github.com/aspose-ocr/Aspose.OCR-for-.NET) | [Blog](https://blog.aspose.com/category/ocr/) | [Free Support](https://forum.aspose.com/c/ocr) | [Temporary License](https://purchase.aspose.com/temporary-license)
