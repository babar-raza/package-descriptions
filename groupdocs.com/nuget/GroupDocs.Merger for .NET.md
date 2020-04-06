# Document Merger .NET API

This .NET on-premise API lets your apps [perform merging, trimming, reordering, swapping](https://products.groupdocs.com/merger/net) and lots of other operations on document pages of [various file formats](https://docs.groupdocs.com/display/mergernet/Supported+Document+Types).

## Document Merger Processing Features

- Merge two or more documents into a single file.
- Join specific or group of pages from various files into one document.
- Split a document into several resultant documents.
- Split document by providing specific page numbers.
- Split document to several multiple page files by providing various page intervals.
- Specify exact line numbers to create its separate one-liner file.
- Change page position within a document.
- Remove single or multiple pages from document.
- Remove several pages from a document based on page number.
- Rotate page to an angle of 90, 180 or 270 degrees.
- Swap position of two pages within a document.
- Extract specific page or a range of pages from the document.
- Change page orientation (portrait, landscape) of specific or all pages within a document.
- Set, update or remove document password.
- Obtain basic meta information about the document.
- Generate image representation of the document pages.
- Ability to log document manipulation process information.
- Load document from local disk, stream or from URL.

## New Features in Version 20.2

- Added support for the MHTML file format.

For the detailed list, please visit [GroupDocs.Merger for .NET 20.2 Release Notes](https://docs.groupdocs.com/display/mergernet/GroupDocs.Merger+for+.NET+20.2+Release+Notes).

## Join & Split File Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM, XLAM
**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX
**Microsoft Visio:** VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
**Microsoft OneNote:** ONE
**OpenOffice:** ODT, OTT, ODP, OTP, ODS
**Web:** HTML, MHT
**Portable:** PDF, XPS
**Text:** TXT
**Other:** TEX, EPUB, CSV, TSV

## Rotate Pages File Formats

**Portable:** PDF, XPS
**Other:** TEX, EPUB

## Other Supported File Formats

GroupDocs.Merger for .NET supports the following file formats to trim page, move/remove page, swap page and change page orientation operations:
**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM, XLAM
**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX
**Microsoft Visio:** VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
**Microsoft OneNote:** ONE
**OpenOffice:** ODT, OTT, ODP, OTP, ODS
**Web:** HTML, MHT, MHTML
**Portable:** PDF, XPS
**Text:** TXT
**Other:** TEX, EPUB

## Platform Independence

GroupDocs.Merger for .NET does not require any external software or third party tool to be installed. GroupDocs.Merger for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure
**Mac OS:** Mac OS X
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET and Mono frameworks.

## Getting Started with GroupDocs.Merger for .NET

Are you ready to give GroupDocs.Merger for .NET a try? Simply execute `Install-Package GroupDocs.Merger` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Merger assembly in your project. If you already have GroupDocs.Merger for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Merger` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-merger/GroupDocs.Merger-for-.NET) for other common usage scenarios.

## Use C# to Join Specific Pages from Various Documents

```csharp
string filePath = @"c:\sample.docx";
string filePath2 = @"c:\sample2.docx";
string filePathOut = @"c:\output\result.docx";

JoinOptions joinOptions = new JoinOptions(1, 4, RangeMode.OddPages);

using (Merger merger = new Merger(filePath, loadOptions))
{
    merger.Join(filePath2, joinOptions);
    merger.Save(filePathOut);
}
```

## Swap Page Position within a Document via C# Code

```csharp
string filePath = @"c:\sample.pptx";
string filePathOut = @"c:\output\result.pptx";

int pageNumber1 = 3;
int pageNumber2 = 6;
SwapOptions swapOptions = new SwapOptions(pageNumber2, pageNumber1);

using (Merger merger = new Merger(filePath))
{
    merger.SwapPages(swapOptions);
    merger.Save(filePathOut);
}
```

[Product Page](https://products.groupdocs.com/merger/net) | [Documentation](https://docs.groupdocs.com/display/mergernet/Home) | [API Reference](https://apireference.groupdocs.com/net/merger) | [Code Samples](https://github.com/groupdocs-merger/GroupDocs.Merger-for-.NET) | [Blog](https://blog.groupdocs.com/category/merger/) | [Free Support](https://forum.groupdocs.com/c/merger) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
