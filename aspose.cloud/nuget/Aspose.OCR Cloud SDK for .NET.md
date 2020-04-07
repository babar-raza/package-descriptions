# .NET Cloud REST API for OCR

This cloud SDK helps you [perform optical character recognition (OCR)](https://products.aspose.cloud/ocr/net) on various image formats using C#, ASP.NET or other .NET supported languages, in the cloud.

## OCR Processing Features

- Recognize and extract text from images via OCR.
- Specify area of the image from which you want to extract text.
- Perform OCR to recognize text from whole or partial image.
- Fetch character and font information from raster images.
- Return the response in the JSON or XML format.
- Supports English, French & Spanish text recognition.

## Save OCR As

TXT, PDF, HOCR

## Read OCR Formats

BMP, JPG, GIF, PNG, TIFF

## Getting Started with Aspose.OCR Cloud SDK for .NET

You do not need to install anything to get started with Aspose.OCR Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.OCR-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.OCR assembly in your project. If you already have Aspose.OCR Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.OCR-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-ocr-cloud/aspose-ocr-cloud-dotnet) for other common usage scenarios.

## Access a PNG Image from URL & Extract its Text using C# via REST API

The following code sample elaborates, how to access a web hosted PNG image via URL, perform OCR on it and extract its text using C#via REST API:

```csharp
string imgUri = @"http://typecast.com/images/uploads/fluid-type-single-column.png";

OcrApi api = new OcrApi(conf);
var request = new PostOcrFromUrlOrContentRequest(null, imgUri);
OCRResponse response = api.PostOcrFromUrlOrContent(request);

return response.Text;
```

[Product Page](https://products.aspose.cloud/ocr/net) | [Documentation](https://docs.aspose.cloud/display/ocrcloud/Home) | [Live Demo](https://products.aspose.app/ocr/family) | [API Reference](https://apireference.aspose.cloud/ocr/) | [Code Samples](https://github.com/aspose-ocr-cloud/aspose-ocr-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/ocr/) | [Free Support](https://forum.aspose.cloud/c/ocr) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
