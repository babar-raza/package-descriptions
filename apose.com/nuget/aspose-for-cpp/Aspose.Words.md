A standalone C++ class library to load, save, format & convert Microsoft Word® documents without Office Automation.

Aspose.Words for C++ is a powerful on premise API that can be used for a great range of document processing tasks such as; working with paragraphs, text, images, text boxes, shapes, tables, rows, cells, fields, form fields, hyperlinks, bookmarks, document sections, headers, footers, footnotes, end-notes, and comments.

## Word File Processing Features
- Copy & move elements from one document to another.
- Join or split documents.
- Get and set document properties.
- Find and replace text.
- Accept all revisions of a document.
- Powerful layout engine.
- Render documents to PDF & image formats.
- Insert HTML into documents.
- Insert SVG images into documents.
- Insert online video.
- Create DML charts.
- Work with Table of Contents (TOC) & page layout.
- Compare two Microsoft Word documents.
- Read & write support for VBA Macros.
- Save document to Printer Command Language (PCL) format.
- Preserve OLE objects and ActiveX controls in the document.
- Work with Web Extension Elements.
- Create or modify a Microsoft Word mail merge data source for a document.
- Preserve mail merge settings & data sources.


## Read & Write Word Processing Files
**Microsoft Word:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, RTF, FlatOPC, FlatOpcMacroEnabled, FlatOpcTemplate, FlatOpcTemplateMacroEnabled
**WordprocessingML:** WordML
**Web:** HTML, MHTML
**OpenOffice:** ODT
**Other:** TXT, MOBI

## Save Word Documents As
**Fixed Layout:** PDF, XPS, OpenXPS
**Graphics:** SVG, EMF
**Web:** HtmlFixed
**Other:** PS, PCL, XamlFlow, XamlFixed, EPUB

## Getting Started with Aspose.Words for C++
Are you ready to give Aspose.Words for C++ a try? Simply execute `Install-Package Aspose.Words.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Words for C++ and want to upgrade the version, please execute `Update-Package Aspose.Words.Cpp` to get the latest version.

## Create DOCX with HelloWorld Text via C++
Try executing the following snippet to see how Aspose.Words for C++ performs in your own environment or check the [GitHub Repository](https://github.com/aspose-words/Aspose.Words-for-C) for other common usage scenarios. 

```c++
// create a blank document.
System::SharedPtr<Document> doc = System::MakeObject<Document>();
// the DocumentBuilder class provides members to easily add content to a document.
System::SharedPtr<DocumentBuilder> builder = System::MakeObject<DocumentBuilder>(doc);
// write a new paragraph in the document with the text "Hello World!"
builder->Writeln(u"Hello World!");
// save the document. 
// the format to save as is inferred from the extension of the file name.
System::String outputPath = dir + u"output.docx";
doc->Save(outputPath);
```

### Convert DOC to EPUB Format
Aspose.Words for C++ allows you to convert Microsoft Word® formats into bytes, EPUB, HTML and other file formats. Following code sample displays how to convert a DOC file into an EPUB format using C++:

```c++
// load the document from disk.
System::SharedPtr<Document> doc = System::MakeObject<Document>(u"template.doc");
// Save the document in EPUB format.
doc->Save(u"output.epub"); 
```

## Limitations
- No support for encrypted documents.
- No support for downloading remote resources from the Internet.
- Limited and unstable support for rendering features.
- No support for reporting features.

[Product Page](https://products.aspose.com/words/cpp) | [Documentation](https://docs.aspose.com/display/wordscpp/Home) | [API Reference](https://apireference.aspose.com/cpp/words) | [Code Examples](https://github.com/aspose-words/Aspose.Words-for-C) | [Blog](https://blog.aspose.com/category/words/) | [Free Support](https://forum.aspose.com/c/words) |  [Temporary License](https://purchase.aspose.com/temporary-license)