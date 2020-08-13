# C++ API to Process & Manipulate PDF Files

[Aspose.PDF for C++](https://products.aspose.com/pdf/cpp) is a native C++ library that allows to create, process, manipulate and convert PDF documents without installing Adobe Acrobat®.

## `Aspose::Pdf` (DOM) Processing Features

- [Set how PDF pages display](https://docs.aspose.com/pdf/cpp/formatting-pdf-document/) in the application.
- Embed the font information into PDF file.
- Set zoom factor of PDF file.
- Set a particular page to be displayed when the PDF document is opened.
- [Convert PDF documents](https://docs.aspose.com/pdf/cpp/convert-pdf-files/) to other [supported file formats](https://docs.aspose.com/pdf/cpp/supported-file-formats/).
- Work with all the [attachments of the PDF](https://docs.aspose.com/pdf/cpp/working-with-attachments/) file.
- [Add images to PDF](https://docs.aspose.com/pdf/cpp/working-with-images/) document.
- [Change password of a PDF](https://docs.aspose.com/pdf/cpp/change-passwords-and-decrypt-pdf-document/) file.
- Decrypt a PDF document.
- [Search a particular phrase](https://docs.aspose.com/pdf/cpp/search-and-get-text-from-pages-of-a-pdf-document/) and change its style in PDF file.

## `Aspose::Pdf::Facades` Processing Features

- Add, update, delete, import, export and extract [annotations of a PDF document](https://docs.aspose.com/pdf/cpp/add-delete-and-get-annotation-facades/).
- [Add bookmarks and child bookmarks to PDF](https://docs.aspose.com/pdf/cpp/add-and-delete-bookmarks/) files.
- [Configure various access privileges for the PDF](https://docs.aspose.com/pdf/cpp/encrypt-decrypt-and-set-privileges-on-pdf-documents/) document.
- [Extract text from all pages of a PDF](https://docs.aspose.com/pdf/cpp/extract-text-from-pdf-facades/) file.

## New Features & Enhancements in Version 20.7

- `C++`-styled iteration has been added over the library containers. `begin/end/cbegin/cend/rbegin/rend` methods are now present where possible.
- Translation of `System::String` class to and from various `STL` string types have been improved. Respective constructors and conversion operators were added (yet explicit, to avoid undesired invocations of suboptimal operations). Also, the `String` class is now working fine with `STL` streams.
- Various other enhancements of the API in terms of performance and memory-related issues.

## Read & Write PDF & Other Formats

**Fixed Layout:** PDF, PDF/A

## Save PDF Documents As

**Microsoft Word:** DOC, DOCX
**Images:** JPEG, PNG, BMP, SVG
**Other:** TeX.

## Getting Started with Aspose.PDF for C++

Are you ready to give Aspose.PDF for C++ a try? Simply execute `Install-Package Aspose.PDF.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.PDF for C++ and want to upgrade the version, please execute `Update-Package Aspose.PDF.Cpp` to get the latest version.

## Extract Text from a PDF Document with C++

Try the below code snippet to see how Aspose.PDF for C++ performs in your environment or check the [GitHub Repository](https://github.com/aspose-pdf/Aspose.Pdf-for-C) for other common usage scenarios.

```c++
auto extractor = MakeObject<Facades::PdfExtractor>();
extractor->BindPdf(u"template.pdf");
extractor->ExtractText();

auto memStream = MakeObject<IO::MemoryStream>();
extractor->GetText(memStream);
auto unicode = System::Text::Encoding::get_Unicode();

String allText = unicode->GetString(memStream->ToArray());
Console::WriteLine(allText);
```

## Convert PDF to DOC Format

One of the most popular feature of Aspose.PDF for C++ is to convert PDF documents to other formats without needing to understand the underlying structure of the resultant format. Give the following snippet a try with your own sample:

```c++
auto doc = MakeObject<Document>(u"template.pdf");
doc->Save(u"output.doc", MakeObject<DocSaveOptions>());
```

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/pdf/cpp) | [Docs](https://docs.aspose.com/pdf/cpp/) | [Demos](https://products.aspose.app/pdf/family) | [API Reference](https://apireference.aspose.com/pdf/cpp) | [Examples](https://github.com/aspose-pdf/Aspose.Pdf-for-C) | [Blog](https://blog.aspose.com/category/pdf/) | [Free Support](https://forum.aspose.com/c/pdf) | [Temporary License](https://purchase.aspose.com/temporary-license)
