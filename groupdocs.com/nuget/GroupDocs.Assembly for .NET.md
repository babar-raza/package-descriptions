# .NET API for Document Assembly

An on-premise [API to generate documents of various formats](https://products.groupdocs.com/assembly/net) based on user-defined templates as well as from other data sources, such as, XML, OData, JSON etc.

## Document Assembly Processing Features

- Support for [multiple data formats](https://docs.groupdocs.com/display/assemblynet/Supported+Document+Formats).
- Perform [sequential data](https://docs.groupdocs.com/display/assemblynet/Template+Syntax+-+Part+2+of+2#TemplateSyntax-Part2of2-OutputtingSequentialData) operations.
- Supports upper, lower, capital, first-cap formatting to template syntax strings.
- Apply ordinal, cardinal, alphabetic, numeric formatting in template syntax.
- Use custom variables in the template documents.
- Support for text comments within template syntax tags.
- Dynamically insert document content & hyperlinks in reports.
- Apply attributes to email message body.
- Dynamically apply email attachments.
- [Generate barcode](https://docs.groupdocs.com/display/assemblynet/Working+with+Barcode+Image+Generation) in reports.
- Dynamically set background color of HTML documents.
- Supports formatting of numeric, text, image, date-time, chart elements in template.
- Apply conditional formatting on template text elements.
- Linq-based template syntax.
- Use explicit specifications or file extensions to change format of assembled file.
- Supports next field analogue of Microsoft Word.
- Update fields during word processing document assembly.
- Support for applying formula during spreadsheet file assembly.
- Automatically remove empty paragraphs.
- Generate various report types, such as, charts, lists, tables etc.
- Instead of exception throwing, support for inline template syntax errors in generated docs.
- Load template documents from HTML with resources.
- Save assembled documents to HTML with resources.

## New Features in Version 20.1.0

- Support for dynamic insertion of bookmarks for the following:
  - Word Processing documents.
  - Emails with HTML and RTF bodies.
- Support for dynamic naming of cell ranges for Spreadsheets.

For a detailed list, please visit [GroupDocs.Assembly for .NET 20.1 Release Notes](https://docs.groupdocs.com/display/assemblynet/GroupDocs.Assembly+for+.NET+20.1+Release+Notes).

## Read & Write Microsoft Office Formats

**Microsoft Word:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, RTF
**Microsoft Excel:** XLSX, XLSM, XLTX, XLTM, XLSB, XLS, XLT
**Microsoft PowerPoint:** PPTX, PPTM, PPSX, PPSM, POTX, POTM, PPT, PPS

## Read & Write Other Formats

**OpenOffice:** ODS, ODT, OTT, ODP, OXPS
**Email:** EML, MSG, EMLX
**Fixed Layout:** PDF, XPS
**Web:** HTML, MHTML
**Images:** TIFF, SVG
**Other:** XML, XAML, TXT, EPUB, PS, PCL, MD

## Platform Independence

GroupDocs.Assembly  for .Net can be used to build applications for Windows, Mac OS X x64 as well as for Linux x64. Developers may also code in PHP, VBScript, Delphi & C++ programming languages while using GroupDocs.Assembly for .Net via COM Interop.

## Getting Started with GroupDocs.Assembly for .NET

Are you ready to give GroupDocs.Assembly for .NET a try? Simply execute `Install-Package GroupDocs.Assembly` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Assembly assembly in your project. If you already have GroupDocs.Assembly for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Assembly` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-.NET) for other common usage scenarios.

## Generate a DOCX File from Markdown (MD) template via C# Code

```csharp
//Setting up source document template
const String strDocumentTemplate = "Markdown Templates/ReadMe.md";
//Setting up destination Markdown reports
const String strDocumentReport = "Word Reports/ReadMe Out.docx";
//Setting up description variable
const string description = "GroupDocs.Assembly for .NET is a class library that enables you to generate documents in popular " +
    "office and email file formats based upon template documents and data obtained from various sources " +
    "including databases, XML, JSON, OData, objects of custom .NET types, external documents, and more.";

DocumentAssembler assembler = new DocumentAssembler();
//Assemble Document
assembler.AssembleDocument(
CommonUtilities.GetSourceDocument(strDocumentTemplate),
CommonUtilities.SetDestinationDocument(strDocumentReport),
new DataSourceInfo("GroupDocs.Assembly for .NET", "product"),
new DataSourceInfo(description, "description"));
}
```

## Use Spreadsheet as a Data Source to Assemble a Document

```csharp
string strDocumentTemplate = "Word Templates/Using Spreadsheet as Table of Data.docx";
string strDocumentReport = "Word Reports/Using Spreadsheet as Table of Data_Output.docx";
// Assemble a document using the external document table as a data source.
DocumentAssembler assembler = new DocumentAssembler();
assembler.AssembleDocument(CommonUtilities.GetSourceDocument(strDocumentTemplate),
                           CommonUtilities.SetDestinationDocument(strDocumentReport),
                           new DataSourceInfo(DataLayer.ExcelData(), "contracts"));
```

[Product Page](https://products.groupdocs.com/assembly/net) | [Documentation](https://docs.groupdocs.com/display/assemblynet/Home) | [API Reference](https://apireference.groupdocs.com/net/assembly) | [Code Samples](https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-.NET) | [Blog](https://blog.groupdocs.com/category/assembly/) | [Free Support](https://forum.groupdocs.com/c/assembly) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
