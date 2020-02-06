Aspose.Words for .NET is a Word Document Processing API that allows the developers to work with Microsoft Word® documents without needing Office Automation.

It is a powerful on-premise class library that can be used for numerous document processing tasks, enabling the developers to enhance their own applications with feature such as, document generation, modification, conversion, rendering and printing without relying on Microsoft Word or automation.

## Word API Features

- Comprehensive document import and export with 35+ supported file formats.
- High fidelity rendering of document pages - exactly like Microsoft Word would have rendered.
- Rich object model that allows to generate, combine, modify, parse or otherwise examine loaded documents.
- Programmatic access to formatting properties of all document elements.
- .NET printing infrastructure to print documents on physical and virtual printers.
- Generate reports with Mail Merge that allows populating documents with data from various sources.
- LINQ Reporting Engine to fetch data from databases, XML, JSON, OData, external documents and more.

## Read & Write Document Formats

**Microsoft Word:** DOC, DOCX, RTF, DOT, DOTX, DOTM, DOCM FlatOPC, FlatOpcMacroEnabled, FlatOpcTemplate, FlatOpcTemplateMacroEnabled
**OpenOffice:** ODT, OTT
**WordprocessingML:** WordML
**Web:** HTML, MHTML
**Fixed Layout:** PDF
**Text:** TXT

## Save Word Files As

**Fixed Layout:** XPS, OpenXPS, PostScript (PS)
**Images:** TIFF, JPEG, PNG, BMP, SVG, EMF, GIF
**Web:** HtmlFixed
**Others:** PCL, EPUB, XamlFixed, XamlFlow, XamlFlowPack

## Platform Independence

Aspose.Words for .NET API can be used to develop applications for a vast range of operating systems (Windows, Linux & Mac OS) and platforms. You can build both 32-bit and 64-bit applications including ASP.NET, WCF & WinForms. Aspose.Words for .NET can also be used via COM Interop from ASP, PHP, Perl and Python. 

You can also build applications with Mono as well as on Windows Azure, Microsoft SharePoint, Microsoft Silverlight, Xamarin.Android, Xamarin.iOS & Xamarin.Mac.

## Getting Started with Aspose.Words for .NET

Are you ready to give Aspose.Words for .NET a try? Simply execute `Install-Package Aspose.Words` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Words for .NET and want to upgrade the version, please execute `Update-Package Aspose.Words` to get the latest version.

## Using C# to Create a DOC File from Scratch

You can execute this snippet in your environment to see how Aspose.Words performs or check the [GitHub Repository](https://github.com/aspose-words/Aspose.Words-for-.NET) for other common usage scenarios.

```csharp
// create a blank document
Document doc = new Document();
// the DocumentBuilder class provides members to easily add content to a document
DocumentBuilder builder = new DocumentBuilder(doc);
// write a new paragraph in the document with the text "Hello World!"
builder.Writeln("Hello World!");
// save the document in DOCX format. 
// the format to save as is inferred from the extension of the file name.
doc.Save(dir + "output.docx");
```

## Using C# to Export DOC to EPUB Format

Aspose.Words for .NET allows you to convert Microsoft Word® formats into bytes, HTML, EPUB, MHTML and other file formats. Following snippet demonstrates the conversion of a DOC file to an EPUB file:

```csharp
// load the document from disc
Document doc = new Document(dir + "template.doc");
// save the document in EPUB format
doc.Save(dir + "output.epub");
```

## Using C# to Import PDF and Save as a DOCX File

```csharp
// Load the PDF document from directory
Document doc = new Document(dir + "input.pdf");
 
// Save the document in DOCX format
doc.Save(dir + "output.docx");
```

[Product Page](https://products.aspose.com/words/net) | [Documentation](https://docs.aspose.com/display/wordsnet/Home) | [API Reference](https://apireference.aspose.com/net/words) | [Code Examples](https://github.com/aspose-words/Aspose.Words-for-.NET) | [Blog](https://blog.aspose.com/category/words/) | [Free Support](https://forum.aspose.com/c/words) | [Temporary License](https://purchase.aspose.com/temporary-license)