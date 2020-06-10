# .NET API for Document Conversion

This .NET API can seamlessly integrate and enables your C#, ASP.NET & other .NET apps to [convert document formats](https://products.groupdocs.com/conversion/net), without installing any 3rd party tools.

## Document Conversion Processing Features

- Provide a source format and fetch its supported conversion formats.
- Generate fixed positioned DOM elements or flow positioned DOM elements for HTML conversion.
- Apply a watermark to the converted document.
- Supports various types of watermarks.
- Supports conversion of N consecutive pages.
- Convert format of specific pages based on page number.
- Convert to HTML format with absolutely positioned HTML elements.
- Supports conversion with advanced configurable options.
- Cache conversion results to local drive or use extension point to customize it.
- Load document from Amazon S3, Azure Blob, FTP, or from local disk.
- Load document via stream or from a specific URL.
- Load password protected documents.
- Enable listening of conversion process stages.

## New Features & Enhancements in Version 20.6

- Implemented conversion from/to `FODP` format.
- Implemented conversion from/to `MD` format.
- Ability to convert `XML` files as data source.
- Improved document info for `PST`/`OST` documents.

For the detailed notes, please visit [GroupDocs.Conversion for .NET 20.6 Release Notes](https://docs.groupdocs.com/display/conversionnet/GroupDocs.Conversion+for+.NET+20.6+Release+Notes).

## Conversion File Formats

GroupDocs.Conversion allows you to convert any of the following type of file formats:
**Spreadsheet:** XLSX, XLSB, XLS2003, XLT, XLTX, XLTM, XLAM, XLS, XLSM, ODS, TSV, CSV
**Document:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT, ODT, OTT
**Presentation:** PPT, PPS, PPTX, PPSX, ODP, POT, POTX, POTM, PPTM, PPSM, FODP
**Image:** JPEG-LS, TIFF, TIF, JPEG, JPG, PNG, GIF, BMP, ICO, CMX, DIB, JPC
**Portable Document:** PDF, XPS, EPUB
**Web:** HTM, HTML, MHTML
**Adobe Photoshop:** PSD
**Microsoft Project:** MPT, MPP, MPX
**Email:** MSG, EML, EMLX
**Microsoft Visio:** VSD, VSDX, VSS, VST, VSX, VTX, VDW, VDX, SVG, VSDM, VSSM, VSTM
**AutoCAD:** DXF, DWG, DWF, STL, IFC, DWT
**Page Description:** EPS, PCL, PS, CGM
**Markup:** MD

to the following formats:
**Microsoft Excel:** XLS, XLSM, XLSB, CSV, XLS2003, TSV, XLTX, XLTM, XLAM
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft PowerPoint:** PPT, PPS, PPTX, PPSX, POT, POTX, POTM, PPTM, PPSM
**OpenDocument:** ODT, OTT, ODS, ODP, OTP, FODP
**Images:** TIFF, TIF, JPEG, JPG, PNG, GIF, BMP, ICO, EMF, WMF
**Fixed Layout:** PDF, XPS
**Web:** HTM, HTML, MHTML
**Markup:** MD

## Supported Platforms

GroupDocs.Conversion for .NET does not require any external software or third party tool to be installed. GroupDocs.Conversion for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure
**Mac OS:** Mac OS X
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET and Mono frameworks.

## Document Information Retrieval

**Word Processing:** word count, line count, page count, author, creation date.
**Spreadsheet:** worksheet count, author, creation date.
**Presentation:** slide count, author, creation date, presentation format.
**Email:** attachment count, is HTML body, is encrypted, is signed.
**Image:** image width, image height, image format.
**CAD Drawing:** collections of layout and layers.
**PDF Document:** page count, is landscaped, is encrypted, author, creation date.

## Getting Started with GroupDocs.Conversion for .NET

Are you ready to give GroupDocs.Conversion for .NET a try? Simply execute `Install-Package GroupDocs.Conversion` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Conversion assembly in your project. If you already have GroupDocs.Conversion for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Conversion` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-conversion/GroupDocs.Conversion-for-.NET) for other common usage scenarios.

## Convert Specific Pages of DOCX to PDF via C# Code

```csharp
using (Converter converter = new Converter("sample.docx"))
{
    PdfConvertOptions options = new PdfConvertOptions
    {
        Pages = new List<int>{ 1, 3 }
    };
    converter.Convert("converted.pdf", options);
}
```

## Use C# to Fetch all Possible Conversion Formats

```csharp
var allPossibleConversions = Converter.GetAllPossibleConversions();
foreach (var possibleConversions in allPossibleConversions)
{
    Console.WriteLine($"Source format: {possibleConversions.Source.Description}");
    foreach (var primary in possibleConversions.Primary)
    {
        Console.WriteLine($"\t...can be converted to {primary.Description}");
    }
    foreach (var secondary in possibleConversions.Secondary)
    {
        Console.WriteLine($"\t...can be converted to {secondary.Description}");
    }
}
```

[Product Page](https://products.groupdocs.com/conversion/net) | [Documentation](https://docs.groupdocs.com/display/conversionnet/Home) | [Demo](https://products.groupdocs.app/conversion/family) | [API Reference](https://apireference.groupdocs.com/net/conversion) | [Examples](https://github.com/groupdocs-conversion/GroupDocs.Conversion-for-.NET) | [Blog](https://blog.groupdocs.com/category/conversion/) | [Free Support](https://forum.groupdocs.com/c/conversion) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
