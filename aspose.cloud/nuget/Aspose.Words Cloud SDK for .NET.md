This cloud SDK provides seamless integration of cloud document processing & manipulation features into your cloud-based C#, ASP.NET & other .NET apps.

Aspose.Words Cloud SDK for .NET is built on top of Aspose.Words REST API and is provided to you under an MIT license. Using Aspose.Words Cloud SDK for .NET, you can work with document comparison, headers, footers, page numbering, tables, sections, document comments, drawing objects, FormFields, fonts, hyperlinks, ranges, paragraphs, math objects, watermarks, track changes and document protection. Aspose.Words Cloud SDK for .NET also assists you in appending documents, splitting documents as well as converting document into other supported file formats.

## Document Processing Features

- Programmatically create new documents of various file formats.
- Fetch a web page via its URL and save it in Microsoft Word file format.
- Get document information, by default, in JSON/XML representation.
- Fetch statistical data of a document.
- Render complex elements (table, DrawingObject etc.) of the document in supported formats.
- Remove all macros contained in a specific document.
- Convert a document to desired file format along with detailed settings.
- Convert an encrypted PDF document into MS Word document format.
- So many more features.

## Read & Write Document Formats

**Microsoft Word:** DOC, DOCX, RTF, DOT, DOTX, DOTM, FlatOPC (XML)
**OpenOffice:** ODT, OTT
**WordprocessingML:** XML
**Web:** HTML, MHTML, HtmlFixed
**Text:** TXT
**Fixed Layout:** PDF

## Save Document As

**Fixed Layout:** PDF/A, XPS, OpenXPS, PS
**Images:** JPEG, PNG, BMP, SVG, TIFF, EMF
**Others:** PCL

## Platform Independence

Aspose.Words Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.Words Cloud SDK for .NET

You do not need to install anything to get started with Aspose.Words Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.Words-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.Words assembly in your project. If you already have Aspose.Words Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.Words-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-words-cloud/aspose-words-cloud-dotnet) for other common usage scenarios.

## Use C# to Create a New MS Word DOCX Cloud Document

The following C# code sample elaborates, how to programmatically create a new Microsoft Word DOCX document in the cloud:

```csharp
//Please get the AppKey and the AppSID from https://dashboard.aspose.cloud/

var fileName = "NewDocument.docx";
string folder = null; // File exists at the root of the storage

var request = new PutCreateDocumentRequest { FileName = fileName, Folder = folder };

var actual = wordsApi.PutCreateDocument(request);
```

## Convert DOCX Document to PDF via C# Code

The following code sample demonstrates, how to convert a DOCX cloud document from PDF using C# code:

```csharp
//Please get the AppKey and the AppSID from https://dashboard.aspose.cloud/

var fileName = "input.docx";
var format = "pdf";

var request = new PutConvertDocumentRequest(File.OpenRead(@"c:\Data\" + fileName), format);
var result = wordsApi.PutConvertDocument(request);
```

[Product Page](https://products.aspose.cloud/words/net) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [API Reference](https://apireference.aspose.cloud/words/) | [Code Samples](https://github.com/aspose-words-cloud/aspose-words-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)