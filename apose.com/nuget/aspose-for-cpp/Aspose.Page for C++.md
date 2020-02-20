Aspose.Page for C++ is an on premise C++ API that allows you to add XPS manipulation features to your own applications. The API also supports to convert XPS, EPS & PS documents to other formats.

Developers can perform various operations on XPS documents, such as, add text, images, pages, gradient, grid using visual brush, transparency object and set opacity mask. It allows to create, edit and convert the file pages as well as the ability to manipulate documents and elements, create vector graphics, group shapes and specifying colors in different color spaces including sRGB, scRGB, and any space based on ICC profile.

## XPS, EPS & PS Processing Features

- Create & modify XPS documents via API.
- Add or delete pages of XPS documents.
- Create vector graphic shapes (Path element) and text strings (Glyphs element).
- Group various elements as well as modify the appearance of text strings and graphics.
- Support for visual brush, image brush, solid color brush and more.
- Work with multiple documents within an XPS document.
- Preserve print tickets and  add default print tickets to new XPS documents.
- Perform cross-package operations such as, inserting a page from another document.
- Conversion of XPS, PS & EPS documents to other popular formats.
- Supports PostScript language levels 1-3 with an exception of font types: Type2 (CFF), Type14 (Chameleon), Types 9, 10, 11, 32 (CID-Keyed).

## Read & Write XPS Format

**Fixed Layout:** XPS

## Save XPS, PS & EPS Documents As

**Fixed Layout:** PDF
**Images:** PNG, JPEG, TIFF, BMP

## Save PS & EPS Documents As

**Metafiles:** EMF, WMF
**Animation:** GIF

## Platform Independence

Aspose.Page for C++ is a native library. It supports 32 as well as 64-bit operating systems (Microsoft Windows desktop (XP, Vista, 7, 8, 10) and server operating systems (2003, 2008, 2012)). Aspose.Page for C++ is designed to perform equally well, both on server and client-side. It is a native assembly that can be deployed by simply copying it.

## Getting Started with Aspose.Page for C++

Are you ready to give Aspose.Page for C++ a try? Simply execute `Install-Package Aspose.Page.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Page for C++ and want to upgrade the version, please execute `Update-Package Aspose.Page.Cpp` to get the latest version.

## Insert Pages in XPS Files using C++

```cpp
// Create new XPS file
auto doc = System::MakeObject<XpsDocument>(dataDir() + u"Sample1.xps");
// Add empty page at end
doc->AddPage();
// Insert an empty page at beginning of pages list
doc->InsertPage(1, true);
// Save resultant XPS document
doc->Save(outDir() + u"AddPages_out.xps");
```

[Product Page](https://products.aspose.com/page/cpp) | [Documentation](https://docs.aspose.com/display/pagecpp/Home) | [API Reference](https://apireference.aspose.com/cpp/page) | [Code Examples](https://github.com/aspose-page/Aspose.Page-for-C) | [Blog](https://blog.aspose.com/category/page/) | [Free Support](https://forum.aspose.com/c/page) |  [Temporary License](https://purchase.aspose.com/temporary-license)
