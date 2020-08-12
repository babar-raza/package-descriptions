[Aspose.Words for .NET](https://products.aspose.com/words/net) is a powerful on-premise class library that can be used for numerous document processing tasks. It enables developers to enhance their own applications with features such as generating, modifying, converting, rendering, and printing documents, without relying on third-party applications, for example, Microsoft Word, or automation.

## Word API Features

The following are some popular features of Aspose.Words for .NET:

- Aspose.Words can be used to develop applications for a vast range of operating systems such as Windows or Linux & Mac OS and [platforms](https://docs.aspose.com/words/net/feature-overview/#supported-platforms) such as [Windows Azure](https://docs.aspose.com/words/net/windows-azure-platform/), Xamarin.Android, or Xamarin.iOS & Xamarin.Mac.
- Comprehensive [document import and export](https://docs.aspose.com/words/net/loading-saving-and-converting/) with [35+ supported file formats](https://docs.aspose.com/words/net/supported-document-formats/). This allows users to [convert documents](https://docs.aspose.com/words/net/converting-a-document/) from [one popular format](https://apireference.aspose.com/words/net/aspose.words/loadformat) to [another](https://apireference.aspose.com/words/net/aspose.words/saveformat), for example, from DOCX into PDF or Markdown, or from PDF into various Word formats.
- Programmatic access to the formatting properties of all document elements. For example, using Aspose.Words users can [split a document](https://docs.aspose.com/words/net/split-a-document/) into parts or [compare two documents](https://docs.aspose.com/words/net/split-a-document/).
- [High fidelity rendering](https://docs.aspose.com/words/net/rendering/) of document pages. For example, if it is needed to render a document as in Microsoft Word, Aspose.Words will successfully cope with this task.
- Ability to [print a document](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) programmatically using Aspose.Words and the XpsPrint API or via dialog boxes.
- [Generate reports with Mail Merge](https://docs.aspose.com/words/net/mail-merge-and-reporting/), which allows filling in merge templates with data from various sources to create merged documents.
- LINQ Reporting Engine to fetch data from databases, XML, JSON, OData, external documents, and much more.

## New Features & Enhancements in Version 20.8

- Implemented Markdown *Inline Images* feature.
- Added new font substitution rule for font name processing.
- Added flag indicating whether images must be skipped while loading PDF documents.
- Implemented support for `SVG` images embedded using data URLs upon HTML import.

For the detailed notes, please visit [Aspose.Words for .NET 20.8 Release Notes](https://docs.aspose.com/words/net/aspose-words-for-net-20-8-release-notes/).

## Read & Write Document Formats

Aspose.Words for .NET supports the following formats,

- DOC, DOCX, RTF, DOT, DOTX,
- ODT, OTT,
- PDF, XPS,
- HTML, MHTML, Markdown,
- JPEG, TIFF, PNG,
- and others.

For a complete list of formats supported by Aspose.Words, see the [Supported Document Formats](https://docs.aspose.com/words/net/supported-document-formats/) page.

## Platform Independence

Aspose.Words for .NET API can be used to develop applications for a vast range of operating systems, such as Windows, Linux and Mac OS, and platforms. You can build both 32-bit and 64-bit applications, including ASP.NET, WCF, and WinForms. Aspose.Words for .NET can also be used via COM Interop from ASP, PHP, Perl, and Python.

You can also build applications with Mono, as well as on Windows Azure, Microsoft SharePoint, Microsoft Silverlight, Xamarin.Android, Xamarin.iOS, and Xamarin.Mac.

## Getting Started with Aspose.Words for .NET

Ready to give Aspose.Words for .NET a try?

Simply run ```Install-Package Aspose.Words``` from Package Manager Console in Visual Studio to fetch the NuGet package.
If you already have Aspose.Words for .NET and want to upgrade the version, please run ```Update-Package Aspose.Words``` to get the latest version.

You can run the following snippets in your environment to see how Aspose.Words works, or check out the [GitHub Repository](https://github.com/aspose-words/Aspose.Words-for-.NET) for other common use cases.

## Using C# to Create a DOCX File from Scratch

Aspose.Words for .NET allows you to create a new blank document and add content to this document.

```c#
// Create a blank document.
Document doc = new Document();

// Use a document builder to add content to the document.
DocumentBuilder builder = new DocumentBuilder(doc);
// Write a new paragraph in the document with the text "Hello World!".
builder.Writeln("Hello World!");

// Save the document in DOCX format. Save format is automatically determined from the file extension.
doc.Save(dir + "output.docx");
```

## Using C# to Convert a Word Document to HTML

Aspose.Words for .NET also allows you to convert Microsoft Word formats to PDF, XPS, Markdown, HTML, JPEG, TIFF, and other file formats. Following snippet demonstrates the conversion from DOCX to HTML:

```c#
// Load the document from disc.
Document doc = new Document(dir + "TestDocument.docx");

// Save the document to DPF format.
doc.Save(dir + "output.html");
```

## Using C# to Import PDF and Save as a DOCX File

In addition, you can import a PDF document into your .NET application and export it as a DOCX format file without the need to install the Microsoft Word:

```c#
// Load the PDF document from disc.
Document doc = new Document(dir + "TestDocument.pdf");

// Save the document to DOCX format.
doc.Save(dir + "output.docx");
```

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/words/net) | [Docs](https://docs.aspose.com/words/net/) | [Demos](https://products.aspose.app/words/family) | [API Reference](https://apireference.aspose.com/words/net) | [Examples](https://github.com/aspose-words/Aspose.Words-for-.NET) | [Blog](https://blog.aspose.com/category/words/) | [Free Support](https://forum.aspose.com/c/words) | [Temporary License](https://purchase.aspose.com/temporary-license)
