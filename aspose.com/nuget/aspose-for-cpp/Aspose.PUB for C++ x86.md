# Process PUB files via C++ API

[Aspose.PUB for C++](https://products.aspose.com/pub/cpp) is a simple API that allows to read & convert Microsoft Publisher® (PUB) files to PDF format programmatically in your C++ Apps. It also provides easy to understand interfaces to edit metadata of PUB files.

## PUB File Processing Features

- Read Microsoft Publisher [(PUB) files for conversion to PDF](https://docs.aspose.com/pub/cpp/pub-to-pdf/) format.
- [Read & Edit metadata of PUB files](https://docs.aspose.com/pub/cpp/programming-with-documents/) via API.

## New Features & Enhancements in Version 20.7

This month's release uses the latest version of the shared codeporting library. The `API` has also been updated to include the latest implementation of Aspose.PDF for C++ library, thus enhancing the overall functionality of the `API`.

## Read PUB Files

**Microsoft Publisher:** PUB

## Save PUB As

**Fixed Layout:** PDF

## Platform Independence

You can use Aspose.PUB for C++ to build any type of 32-bit and 64-bit C++ applications. You can use it on server and client-side by simply copying the assembly without worrying about other services or modules.

## Getting Started with Aspose.PUB for C++

Are you ready to give Aspose.PUB for C++ a try? Simply execute `Install-Package Aspose.PUB.Cpp.x86` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.PUB for C++ and want to upgrade the version, please execute `Update-Package Aspose.PUB.Cpp.x86` to get the latest version.

## Convert a Microsoft Publisher File to PDF using C# Code

You can execute below code snippet to see how Aspose.PDF API performs in your own development environment or check the [GitHub Repository](https://github.com/aspose-pub/Aspose.PUB-for-C) for other common usage scenarios.

```c++
// Initialize license object
auto license = System::MakeObject<Aspose::Pub::License>();
// Set license
license->SetLicense(dataDir() + u"License\\Aspose.PUB.C++.lic");

System::String filePub = dataDir() + u"1.pub";
System::String filePdf = dataDir() + u"1.pdf";

System::Console::WriteLine(u"Convert starting...");

System::SharedPtr<IPubParser> parser = PubFactory::CreateParser(filePub);
System::SharedPtr<Document> document = parser->Parse();
PubFactory::CreatePdfConverter()->ConvertToPdf(document, filePdf);

System::Console::WriteLine(u"Convert done.");
```

## Limitations

At the moment API lacks the support to convert images of PUB file to PDF file. So such images wont show up in the resultant output PDF file. This feature is in our plan to be released in some future release.

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/pub/cpp) | [Docs](https://docs.aspose.com/pub/cpp/) | [API Reference](https://apireference.aspose.com/pub/cpp) | [Examples](https://github.com/aspose-pub/Aspose.PUB-for-C) | [Blog](https://blog.aspose.com/category/pub/) | [Free Support](https://forum.aspose.com/c/pub) | [Temporary License](https://purchase.aspose.com/temporary-license)
