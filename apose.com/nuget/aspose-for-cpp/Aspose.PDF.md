Aspose.PDF for C++ is a native C++ library that allows to create, process, manipulate and convert PDF documents without installing Adobe Acrobat®.

## PDF Processing Features
- Generate PDF documents via API, XML or templates.
- Create PDF forms and manage form fields.
- Add, remove & replace text & images on any PDF page.
- Set PDF page margins, zoom factor, transition type & other attributes.
- Custom font handling for PDF documents.
- Manage attachments, watermarks, bookmarks, annotation & metadata.
- Split, merge, insert or extract PDF pages.
- Convert PDF pages or whole documents to images.
- Set security constraints on PDF files.

## Read & Write PDF & Other Formats
**Fixed Layout:** PDF, PDF/A

## Save PDF Documents As
**Microsoft Word:** DOC, DOCX
**Images:** JPEG, PNG, BMP, SVG

## Getting Started with Aspose.PDF for C++
Are you ready to give Aspose.PDF for C++ a try? Simply execute `Install-Package Aspose.PDF.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.PDF for C++ and want to upgrade the version, please execute `Update-Package Aspose.PDF.Cpp` to get the latest version.

Try the below code snippet to see how Aspose.PDF for C++ performs in your environment or check the [GitHub Repository](https://github.com/aspose-pdf/Aspose.Pdf-for-C) for other common usage scenarios. 

### Extract Text from a PDF Document with C++
```c++
auto extractor = MakeObject<Facades::PdfExtractor>();	
extractor->BindPdf(u"..\\Data\\Text\\input.pdf");
extractor->ExtractText();
	
auto memStream = MakeObject<IO::MemoryStream>();
extractor->GetText(memStream);
auto unicode = System::Text::Encoding::get_Unicode();

String allText = unicode->GetString(memStream->ToArray());	
Console::WriteLine(allText);
```

### Convert PDF to DOC Format
One of the most popular feature of Aspose.PDF for C++ is to convert PDF documents to other formats without needing to understand the underlying structure of the resultant format. Give the following snippet a try with your own samples.
```c++
auto doc = MakeObject<Document>(u"template.pdf");
doc->Save(u"output.doc", MakeObject<DocSaveOptions>());
```
[Product Page](https://products.aspose.com/pdf/cpp) | [Documentation](https://docs.aspose.com/display/pdfcpp/Home) | [API Reference](https://apireference.aspose.com/cpp/pdf) | [Code Examples](https://github.com/aspose-pdf/Aspose.Pdf-for-C) | [Blog](https://blog.aspose.com/category/pdf/) | [Free Support](https://forum.aspose.com/c/pdf) |  [Temporary License](https://purchase.aspose.com/temporary-license)