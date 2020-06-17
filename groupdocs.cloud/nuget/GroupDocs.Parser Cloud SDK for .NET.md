# Document Parser .NET Cloud REST API

This [document parser & data extraction REST API](https://products.groupdocs.cloud/parser/net) can be used to enhance your C#, ASP.NET, & other .NET cloud-based applications to perform parsing operations.

## Cloud Document Parser Features

- Create easy to define templates with data field and table definitions.
- Parse documents with pre-defined templates.
- Extract data from invoices or from other sort of documents.
- Supports extracting text and images.
- Extract data from regular documents as well as from email or archive containers.
- Obtain data from PDF portfolios.
- Fetch text fields, numbers and tables from common documents.
- Save your templates in the storage and parse your documents with them.
- Ability to extract HTML or Markdown (MD) text for a quick preview.
- Fetch specific pages of plain as well as formatted text.
- Extract formatted (bold, italic, hyperlink etc.) text in the MD format.
- Support for extracting text in HTML formatting (paragraph, hyperlinks, lists etc.).
- Retrieve all images from a document and save them.
- Obtain basic information about documents, archives, emails, and attachments etc.
- Extract data from a document contained inside a ZIP archive, email or PDF portfolio.

## New Features & Enhancements in Version 20.6

- Added `Node.js`, `PHP`, `Python`, and `Ruby` SDK for GroupDocs.Parser Cloud.
- Implemented extraction of encoding.
- Implemented additional image information extraction.

For the detailed notes, pelase visit [GroupDocs.Parser for Cloud 20.6 Release Notes](https://wiki.groupdocs.cloud/parsercloud/release-notes/release-notes-2020/groupdocs-parser-for-cloud-20-6-release-notes).

## Parse Document By Template Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF

## Extract Text Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Emails:** EML, EMLX, MSG
**Notes:** ONE

## Extract Document Info Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Emails:** PST, OST, EML, EMLX, MSG
**Notes:** ONE
**Archives:** ZIP

## Extract Images Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Emails:** EML, EMLX, MSG
**Archives:** ZIP

## Extract Container Items Info Supported Formats

**Portable:** PDF
**Emails:** PST, OST, EML, EMLX, MSG
**Archives:** ZIP

## Getting Started

You do not need to install anything to get started with GroupDocs.Parser Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Parser-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Parser assembly in your project. If you already have GroupDocs.Parser Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Parser-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-dotnet) for other common usage scenarios.

## Extract Text From The Whole Document

```csharp
string MyAppKey = "";
string MyAppSid = "";
  
var configuration = new Configuration(MyAppSid, MyAppKey);
  
var apiInstance = new ParseApi(configuration);
var fileInfo = new FileInfo
{
    FilePath = "words/one-page.docx"
};

var options = new TextOptions
{
    FileInfo = fileInfo
};

var request = new TextRequest(options);
var response = apiInstance.Text(request);
```

## Parse by Template of a DOCX Inside a ZIP Container

```csharp
string MyAppKey = "";
string MyAppSid = "";
  
var configuration = new Configuration(MyAppSid, MyAppKey);
  
var apiInstance = new ParseApi(configuration);
var fileInfo = new FileInfo

{
    FilePath = "containers/archive/sample.zip",
};

var templatePath = "templates/document-template.json";
var options = new ParseOptions

{
    FileInfo = fileInfo,
    TemplatePath = templatePath,
    ContainerItemInfo = new ContainerItemInfo
    {
        RelativePath = "companies.docx"
    }
};

var request = new ParseRequest(options);
var response = apiInstance.Parse(request);
```

[Product Page](https://products.groupdocs.cloud/parser/net) | [Documentation](https://wiki.groupdocs.cloud/parsercloud/) | [Demo](https://products.groupdocs.app/parser/family) | [API Reference](https://apireference.groupdocs.cloud/parser/) | [Examples](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/parser/) | [Free Support](https://forum.groupdocs.cloud/c/parser) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
