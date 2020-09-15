# .NET SDK for Document Processing in the Cloud

[Aspose.Words Cloud SDK for .NET](https://products.aspose.cloud/words/net) wraps Aspose.Words REST API to provide seamless integration of Word Processing features in your own .NET applications.

## Cloud Word Processor in a Nutshell

- Create documents from scratch via APIs, using [MailMerge](https://docs.aspose.cloud/display/wordscloud/Working+with+Mail+Merge) or importing web-pages.
- [Convert between 40+ diverse file formats](https://docs.aspose.cloud/display/wordscloud/Supported+File+Formats) including DOC, DOCX, ODT, OTT, OPC, HTML, PDF, XPS, WordML, PS, MD & more.
- Join, split, append, compare & classify documents with simple API calls.
- Access, edit or add Word document elements such as hyperlinks, comments, paragraphs, tables, footnotes, math & drawing objects, watermarks and so on.
- Insert, update, copy or apply styles to supported document elements.
- Render document pages, objects or whole documents in raster & vector image formats.
- [Add, update & remove FormFields in Word documents](https://docs.aspose.cloud/display/wordscloud/Working+with+FormFields).
- Encrypt or decrypt documents as well as load protected documents for all possible manipulation operations.
- Find text via regular expression & replace all occurrences of the captured string.

## Enhancements in Aspose.Words Cloud v20.8

- Added new API method `(PUT '/words/{name}/compatibility/optimize')` that allows to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.
- Added `ApplyBaseDocumentHeadersAndFootersToAppendingDocuments` option to `DocumentEntryList` for `AppendDocument` API.
- `WithoutNodePath` methods have been removed.
- Numerous `PDF` to `Word` conversion improvements.

Visit [Aspose.Words Cloud 20.8 Release Notes](https://docs.aspose.cloud/display/wordscloud/Aspose.Words+Cloud+20.8+Release+Notes) for detailed release notes.

## Get Started with Aspose.Words Cloud SDK for .NET

Create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information for authentication. 

### Install via Package Manager Console

Execute `Install-Package Aspose.Words-Cloud` from the Package Manager Console in Visual Studio to fetch the latest version of .NET SDK. If you just want to upgrade it, execute `Update-Package Aspose.Words-Cloud`.

### Install from Command Line

[Get & set up NuGet CLI](https://docs.microsoft.com/en-us/nuget/reference/nuget-exe-cli-reference) then execute `nuget install Aspose.Words-Cloud` from the command line.

## SDK Dependencies

- [.NET Framework 2.0 or later](https://dotnet.microsoft.com/download)
- [Json.NET](https://dotnet.microsoft.com/download)

## Convert DOCX to PDF in the Cloud

```csharp
var fileName = "template.docx";
var format = "pdf";

var request = new PutConvertDocumentRequest(File.OpenRead(@"c:\Data\" + fileName), format);
var result = wordsApi.PutConvertDocument(request);
```

[Product Page](https://products.aspose.cloud/words/net) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [Demo](https://products.aspose.app/words/family) | [API Reference](https://apireference.aspose.cloud/words/) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
