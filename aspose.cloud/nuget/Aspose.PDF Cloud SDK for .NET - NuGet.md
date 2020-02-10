This Cloud SDK allows you to easily build cloud-based PDF creator, editor & converter apps in C#, ASP.NET or other .NET languages for various cloud platforms.

Aspose.PDF Cloud SDK for .NET is available to you under an MIT license and is a wrapper around Aspose.PDF REST API. Access images embedded in the PDF documents for customization, work with; annotations, stamps, PDF form fields, watermarks, as well as the OCR layers within the PDF files.

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

## Read & Write PDF Formats

PDF, EPUB, HTML, TeX, SVG, XML, XPS, FDF, XFDF

## Save PDF As

XLS, XLSX, PPTX, DOC, DOCX, MobiXML, JPEG, EMF, PNG, BMP, GIF, TIFF, Text

## Read PDF Formats

MHT, PCL, PS, XSLFO, MD

## Platform Independence

Aspose.PDF Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

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

[Product Page](https://products.aspose.cloud/pdf/net) | [Documentation](https://docs.aspose.cloud/display/pdfcloud/Home) | [API Reference](https://apireference.aspose.cloud/pdf/) | [Code Samples](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/pdf/) | [Free Support](https://forum.aspose.cloud/c/pdf) | [Free Trial](https://dashboard.aspose.cloud/#/apps)