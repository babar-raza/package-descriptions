# C++ API for Word Document Processing

A standalone C++ class library to load, save, format & convert Microsoft Word® documents without Office Automation.

[Aspose.Words for C++](https://products.aspose.com/words/cpp) is a powerful on premise API that can be used for a great range of document processing tasks such as; working with [documents](https://docs.aspose.com/display/wordscpp/Working+with+Document), [sections](https://docs.aspose.com/display/wordscpp/Working+with+Sections), [tables](https://docs.aspose.com/display/wordscpp/Working+with+Tables), [bookmarks](https://docs.aspose.com/display/wordscpp/Working+with+Bookmarks), [fields](https://docs.aspose.com/display/wordscpp/Working+with+Fields), [form fields](https://docs.aspose.com/display/wordscpp/Working+with+Form+Fields), [DocumentBuilder](https://docs.aspose.com/display/wordscpp/Use+DocumentBuilder+to+Insert+Document+Elements), [ranges](https://docs.aspose.com/display/wordscpp/Working+with+Ranges), [comments](https://docs.aspose.com/display/wordscpp/Working+with+Comments), [content control SDT](https://docs.aspose.com/display/wordscpp/Working+with+Content+Control+SDT), [images](https://docs.aspose.com/display/wordscpp/Working+with+Images), [styles](https://docs.aspose.com/display/wordscpp/Working+with+Styles), [charts](https://docs.aspose.com/display/wordscpp/Working+with+Charts), [watermarks](https://docs.aspose.com/display/wordscpp/Working+with+Watermark), lists, [shapes](https://docs.aspose.com/display/wordscpp/Working+with+Shapes), [mail merge](https://docs.aspose.com/display/wordscpp/How+to+Use+Advanced+Mail+Merge+Features), rendering, printing and much more.

## Word File Processing Features

- Call the Document constructor without parameters to [programmatically create a new blank document](https://docs.aspose.com/display/wordscpp/Creating+or+Loading+a+Document#CreatingorLoadingaDocument-CreatingaNewDocument).
- Detect the file format and [check file format compatibility](https://docs.aspose.com/display/wordscpp/Creating+or+Loading+a+Document#CreatingorLoadingaDocument-HowtoDetecttheFileFormatandCheckFormatCompatibility).
- [Convert Word Documents](https://docs.aspose.com/display/wordscpp/Converting+a+Document) to other supported formats.
- [Serialize a document object](https://docs.aspose.com/display/wordscpp/Converting+a+Document#ConvertingaDocument-ConvertaDocumenttoByteArray) to fetch a byte array and vice versa.
- Supports [conversion compliance to various PDF standards](https://docs.aspose.com/display/wordscpp/Converting+a+Document#ConvertingaDocument-ConvertusingPdfCompliance).
- [Export fonts to HTML](https://docs.aspose.com/display/wordscpp/Converting+a+Document#ConvertingaDocument-ExportFontstoHTMLinBase64Encoding) in `Base64` encoding.
- [Save any password encrypted word document](https://docs.aspose.com/display/wordscpp/Working+With+OOXML#WorkingWithOOXML-EncryptDocumentwithPassword).
- [Specify the OOXML specification](https://docs.aspose.com/display/wordscpp/Working+With+OOXML#WorkingWithOOXML-SettingtheComplianceLevel).
- [Apply password to encrypted documents](https://docs.aspose.com/display/wordscpp/Working+with+SaveOptions#WorkingwithSaveOptions-EncryptDocumentWithPassword) and ignore `RoutingSlip` data while saving.
- [Compress all the metafiles](https://docs.aspose.com/display/wordscpp/Working+with+SaveOptions#WorkingwithSaveOptions-CompressMetafiles), be it small or large.
- Enable bi-directional marks to add support for right to left languages.
- Access the VBA Project to extend the functionality.
- Read, write or modify [VBA Macros](https://docs.aspose.com/display/wordscpp/Working+with+VBA+Macros).
- [Clone VBA Project](https://docs.aspose.com/display/wordscpp/Working+with+VBA+Macros#WorkingwithVBAMacros-CloneVBAProject) or VBA Module.
- So many more [features](https://docs.aspose.com/display/wordscpp/Developer+Guide).

## New Features in Version 20.5

- Ability to show/hide Grammatical and Spelling errors.
- New helper class to work with watermark inside document is introduced.
- Added feature to set the compression level for `OOXML` documents.

## Limitations and API Differences in Version 20.5

Aspose.Words for C++ has some differences as compared to its equivalent .NET version of the API. This section contains information about all such functionality that is not available in the current release. The missing features will be added in future releases.

- Metered license.
- Multipage TIFF format.
- *LINQ* and Reporting features.
- *OpenGL* 3D Shapes rendering.
- Advanced typography based on the *HarfBuzz* shaper.
- Loading PDF documents.
- Limited support for database features - C++ doesn't have a common API for DB like .Net System.Data.
- Only supports Microsoft Visual C++ version 2017 or higher and only for the x64 platform.

For the detailed notes, please visit [Aspose.Words for CPP 20.5 Release Notes](https://docs.aspose.com/display/wordscpp/Aspose.Words+for+CPP+20.5+Release+Notes).

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

### Create DOCX with HelloWorld Text via C++

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
doc->Save(u"output.docx");
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

[Product Page](https://products.aspose.com/words/cpp) | [Documentation](https://docs.aspose.com/display/wordscpp/Home) | [Demo](https://products.aspose.app/words/family) | [API Reference](https://apireference.aspose.com/cpp/words) | [Examples](https://github.com/aspose-words/Aspose.Words-for-C) | [Blog](https://blog.aspose.com/category/words/) | [Free Support](https://forum.aspose.com/c/words) |  [Temporary License](https://purchase.aspose.com/temporary-license)
