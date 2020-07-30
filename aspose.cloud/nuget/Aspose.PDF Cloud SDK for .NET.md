# .NET REST API to Process PDF in Cloud

This Cloud SDK allows you to [easily build cloud-based PDF creator](https://products.aspose.cloud/pdf/net), editor & converter apps in C#, ASP.NET or other .NET languages for various cloud platforms.

## PDF Processing Features

- Add PDF document's header & footer in text or image format.
- Add tables & stamps (text or image) to PDF documents.
- Append multiple PDF documents to an existing file.
- Work with PDF attachments, annotations, & form fields.
- Apply encryption or decryption to PDF documents & set password.
- Delete all stamps & tables from a page or entire PDF document.
- Delete a specific stamp or table from the PDF document by its ID.
- Replace a single or multiple instances of a text on a PDF page or from entire document.
- Extensive support for converting PDF documents to various other file formats.
- Extract various elements of PDF file & make PDF document optimized.

## New Features & Enhancements in Version 20.7

- Added Support for `PDF_A_3A` Format.
- Added Support of `MaxResolution` option in `OptimizeOption`.
- Added Support of `ImageCompressionOptions` in `OptimizeOptions`.
- Implemented Info action.

For the detailed notes, please visit [Aspose.PDF Cloud 20.7 Release Notes](https://docs.aspose.cloud/display/pdfcloud/Aspose.PDF+Cloud+20.7+Release+Notes).

## Read & Write PDF Formats

PDF, EPUB, HTML, TeX, SVG, XML, XPS, FDF, XFDF

## Save PDF As

XLS, XLSX, PPTX, DOC, DOCX, MobiXML, JPEG, EMF, PNG, BMP, GIF, TIFF, Text

## Read PDF Formats

MHT, PCL, PS, XSLFO, MD

## Getting Started with Aspose.PDF Cloud SDK for .NET

You do not need to install anything to get started with Aspose.PDF Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.PDF-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.PDF assembly in your project. If you already have Aspose.PDF Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.PDF-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-dotnet) for other common usage scenarios.

## Convert PDF File to DOC Format via C# Code

The following code sample demonstrates how to convert a PDF file to DOC format using C# code via REST API:

```csharp
string name = "Input_Document.pdf";
using (Stream stream = System.IO.File.OpenRead(Path.Combine("", name)))
    {
        string resFileName = "Output_Document.doc";

        var response = api.PutPdfInRequestToDoc(Path.Combine(FolderName, resFileName), file: stream);
        Console.WriteLine(response);
    }
```

## Use C# Code to Optimize PDF Document

The following C# code elaborates how to optimize various factors, such as, image compression & image quality, of a PDF document via REST API:

```csharp
const string name = "Input_Document.pdf";
UploadFile(name, name);

var options = new OptimizeOptions(
    AllowReusePageContent: false,
    CompressImages: true,
    ImageQuality: 100,
    RemoveUnusedObjects: true,
    RemoveUnusedStreams: true,
    UnembedFonts: true);
var response = api.PostOptimizeDocument(name, options, folder: FolderName);
Console.WriteLine(response);
```

[Product Page](https://products.aspose.cloud/pdf/net) | [Documentation](https://docs.aspose.cloud/display/pdfcloud/Home) | [Demo](https://products.aspose.app/pdf/family) | [API Reference](https://apireference.aspose.cloud/pdf/) | [Examples](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/pdf/) | [Free Support](https://forum.aspose.cloud/c/pdf) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
