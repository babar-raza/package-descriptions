# .NET REST API for Cloud Document Processing

This cloud SDK provides seamless integration of [cloud document processing & manipulation features](https://products.aspose.cloud/words/net) into your cloud-based C#, ASP.NET & other .NET apps.

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

## New Features & Enhancements in Version 20.8

- Added new API method `(PUT '/words/{name}/compatibility/optimize')` that allows to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.
- Added `ApplyBaseDocumentHeadersAndFootersToAppendingDocuments` option to `DocumentEntryList` for `AppendDocument` API.
- `WithoutNodePath` methods have been removed, pass `null` values instead.

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
**Others:** PCL, Markdown

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

[Product Page](https://products.aspose.cloud/words/net) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [Demo](https://products.aspose.app/words/family) | [API Reference](https://apireference.aspose.cloud/words/) | [Examples](https://github.com/aspose-words-cloud/aspose-words-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
