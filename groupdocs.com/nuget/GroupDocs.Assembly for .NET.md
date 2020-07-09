# .NET Document Automation & Reporting API

An on-premise [Document Automation Engine](https://products.groupdocs.com/assembly/net) that accepts a template document and some data to assemble documents as per syntax defined by the template. Data can be fetched from various sources including CSV, XML, OData, JSON, .NET Objects & more.

## Report Generation via .NET

- Wide range of supported [document formats](https://docs.groupdocs.com/display/assemblynet/Supported+Document+Formats).
- Capable to manipulate data using formulae & [sequential data](https://docs.groupdocs.com/display/assemblynet/Template+Syntax+-+Part+2+of+2#TemplateSyntax-Part2of2-OutputtingSequentialData) operations.
- Supports upper, lower, capital, first-cap formatting.
- Apply Ordinal, Cardinal, Alphabetic & Numeric formatting in template syntax.
- Dynamically insert document content & hyperlinks in reports.
- Apply attributes to email message body and dynamically add email attachments.
- [Generate barcode labels](https://docs.groupdocs.com/display/assemblynet/Working+with+Barcode+Image+Generation) in reports.
- Dynamically set background color of HTML documents.
- Apply formatting to numeric, text, image, date-time & chart elements in template.
- Apply conditional formatting on text elements.
- LINQ-based template syntax.
- Supports NEXT field analogue of Microsoft Word.
- Update fields during Word document assembly.
- Apply & calculate formula during Excel file assembly.
- Automatically remove empty paragraphs.
- Generate various report types, such as, charts, lists, tables etc.
- Load templates from HTML as well as save assembled documents to HTML with resources.

## Read & Write Microsoft Office Formats

**Microsoft Word:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, RTF\
**Microsoft Excel:** XLSX, XLSM, XLTX, XLTM, XLSB, XLS, XLT\
**Microsoft PowerPoint:** PPTX, PPTM, PPSX, PPSM, POT, POTX, POTM, PPT, PPS

## Other Supported Formats

**OpenOffice:** ODS, ODT, OTT, OTP, ODP, OXPS\
**Email:** EML, MSG, EMLX\
**Fixed Layout:** PDF, XPS\
**Web:** HTML, MHTML\
**Images:** TIFF, SVG\
**Other:** XML, XAML, TXT, EPUB, PS, PCL, MD

## Platform Independence

GroupDocs.Assembly  for .NET can be used to build applications for Windows, Mac OS X as well as for Linux. Developers may code in PHP, VBScript, Delphi & C++ programming languages while using GroupDocs.Assembly for .BET via COM Interop.

## Getting Started with GroupDocs.Assembly for .NET

Are you ready to give GroupDocs.Assembly for .NET a try? Simply execute `Install-Package GroupDocs.Assembly` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Assembly assembly in your project. If you already have GroupDocs.Assembly for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Assembly` to get the latest version.

## Generate DOCX from Markdown (MD) Template via C# Code

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

## Use Excel File as a Data Source to Assemble a Document

```csharp
string strDocumentTemplate = "Word Templates/Using Spreadsheet as Table of Data.docx";
string strDocumentReport = "Word Reports/Using Spreadsheet as Table of Data_Output.docx";
// Assemble a document using the external document table as a data source.
DocumentAssembler assembler = new DocumentAssembler();
assembler.AssembleDocument(CommonUtilities.GetSourceDocument(strDocumentTemplate),
                           CommonUtilities.SetDestinationDocument(strDocumentReport),
                           new DataSourceInfo(DataLayer.ExcelData(), "contracts"));
```

[Product Page](https://products.groupdocs.com/assembly/net) | [Documentation](https://docs.groupdocs.com/display/assemblynet/Home) | [Demo](https://products.groupdocs.app/assembly/family) | [API Reference](https://apireference.groupdocs.com/net/assembly) | [Examples](https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-.NET) | [Blog](https://blog.groupdocs.com/category/assembly/) | [Free Support](https://forum.groupdocs.com/c/assembly) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
