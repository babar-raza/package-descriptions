# C++ API for XPS Page Manipulation

[Aspose.Page for C++](https://products.aspose.com/page/cpp) is an on premise C++ API that allows you to add XPS manipulation features to your own applications. The API also supports to convert XPS, EPS & PS documents to other formats.

## XPS Processing Features

- Create and [edit `XPS` documents](https://docs.aspose.com/display/pagecpp/Add+Text+in+XPS+Document).
- Add or remove [pages of `XPS` document](https://docs.aspose.com/display/pagecpp/Add+Pages+to+XPS+Document).
- Create vector graphics shapes (Path element) using a set of primitives (elliptical arcs, Bezier curve segments, and straight-line segments).
- Create text strings (Glyphs element).
- Group elements (Canvas element) to manipulate a group as a whole.
- [Supports brushes of various types](https://docs.aspose.com/display/pagecpp/Add+Grid+using+Visual+Brush), such as, solid color brush, image brush, visual brush, etc.
- Supports different color spaces including `sRGB`, `scRGB` and any space-based on `ICC` profile.
- Works for multiple documents inside an `XPS` document.
- Add default print tickets into new `XPS` document or preserve print tickets in opened `XPS`.
- Save `XPS` documents in various [supported file formats](https://docs.aspose.com/display/pagecpp/Supported+File+Formats).

## Enhancements in Version 20.3

For the detailed notes, please visit [Aspose.Page for CPP 20.3 Release Notes](https://docs.aspose.com/display/pagecpp/Aspose.Page+for+CPP+20.3+Release+Notes).

## Save XPS as

PDF, BMP, TIFF, JPEG, PNG

# Save EPS/PS as

PDF, BMP, TIFF, JPEG, PNG, EMF, WMF, GIF

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

[Product Page](https://products.aspose.com/page/cpp) | [Documentation](https://docs.aspose.com/display/pagecpp/Home) | [Live Demo](https://products.aspose.app/page/family) | [API Reference](https://apireference.aspose.com/cpp/page) | [Code Examples](https://github.com/aspose-page/Aspose.Page-for-C) | [Blog](https://blog.aspose.com/category/page/) | [Free Support](https://forum.aspose.com/c/page) |  [Temporary License](https://purchase.aspose.com/temporary-license)
