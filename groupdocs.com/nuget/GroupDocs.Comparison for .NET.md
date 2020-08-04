# .NET Document Comparison API

On-premise library to [compare documents](https://products.groupdocs.com/comparison/net) in applications based on .NET platform. Retrieve list of changes in desired format with line-by-line comparison of content, paragraphs, characters, styles, shapes and position.

## Document Comparison Features

- [Compare and detect differences](https://docs.groupdocs.com/comparison/net/compare-documents/) among similar documents.
- Support for [55+ popular document formats](https://docs.groupdocs.com/comparison/net/supported-document-formats/) from various categories.
- Visual separation of detected changes with the ability to [accept or reject modifications](https://docs.groupdocs.com/comparison/net/accept-or-reject-detected-changes/).
- [Generate document preview](https://docs.groupdocs.com/comparison/net/generate-document-pages-preview/).
- Compare paragraph, word as well as the characters.
- Identify content styling and formatting changes.
- Set metadata from the source, target files or keep it user-defined.
- Make the resultant document password protected.

## New Features & Enhancements in Version 20.7

- Refactor `GetDocumentInfo` Method for Cells.
- Improved comparison of `DocumentTags` Word.
- Improved *sheet rendering* for Cells.
- Added ability to *merge* source code file.

For the detailed notes, please visit [GroupDocs.Comparison for .NET 20.7 Release Notes](https://docs.groupdocs.com/comparison/net/groupdocs-comparison-for-net-20-7-release-notes/).

## Supported Microsoft Office Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTX\
**Microsoft Excel:** XLS, XLT, XLSX, XLTM, XLSB, XLSM, XLSX\
**Microsoft PowerPoint:** POT, POTX, PPS, PPSX, PPTX, PPT\
**Microsoft OneNote:** ONE\
**Microsoft Visio:** VSDX, VSD, VSS, VST, VDX

## Other Supported Formats

**OpenDocument:** ODT, ODP, OTP, ODS, OTT\
**Portable:** PDF\
**AutoCAD:** DWG, DXF\
**Email:** EML, EMLX, MSG\
**Images:** BMP, GIF, JPG, JPEG, PNG, DICOM\
**Web:** HTM, HTML, MHT, MHTML\
**Text:** TXT, CSV\
**eBook:** MOBI, DJVU

## Develop & Deploy GroupDocs.Comparison Anywhere

**Microsoft Windows:** Windows Azure, Microsoft Windows Desktop (x86, x64), Microsoft Windows Server (x86, x64)\
**macOS:** Mac OS X\
**Linux:** Ubuntu, OpenSUSE, CentOS, and others\
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later\
**Supported Frameworks:** .NET Standard 2.0, .NET Framework 2.0 or higher, .NET Core 2.0 or higher, Mono Framework 1.2 or higher

## Getting Started with GroupDocs.Comparison for .NET

Are you ready to give GroupDocs.Comparison for .NET a try? Simply execute `Install-Package GroupDocs.Comparison` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Comparison assembly in your project. If you already have GroupDocs.Comparison for .NET and want to upgrade it, please execute `Update-Package GroupDocs.Comparison` to get the latest version.

## Compare Password Protected Files

```csharp
using (Comparer comparer = new Comparer("source.docx", new LoadOptions() { Password = "1234" }))
{
	comparer.Add("target1.docx", new LoadOptions() { Password = "5678" });
    comparer.Add("target2.docx", new LoadOptions() { Password = "5678" });
    comparer.Add("target3.docx", new LoadOptions() { Password = "5678" });
    comparer.Compare("result.docx");
}
```

[Product Page](https://products.groupdocs.com/comparison/net) | [Documentation](https://docs.groupdocs.com/comparison/net/) | [Demo](https://products.groupdocs.app/comparison/family) | [API Reference](https://docs.groupdocs.com/display/comparisonnet/home) | [Examples](https://docs.groupdocs.com/comparison/net) | [Blog](https://blog.groupdocs.com/category/comparison/) | [Free Support](https://blog.groupdocs.com/category/comparison/) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
