# Document Merger .NET Cloud REST API

This REST API enables your C#, ASP.NET, & other .NET apps to [perform document merging & joining](https://products.groupdocs.cloud/merger/net) for 40+ file formats, while page manipulation for 35+ formats.

## Cloud Document Merger Features

- Merge two of more documents into a single file.
- Merge specific pages from several different documents into a single file.
- Join page ranges from various documents into a single resultant file.
- Split a source document into many different files.
- Generate image representation of document pages as preview.
- Create document image preview of all pages, specific pages, or a page range.
- Move, remove, rotate, swap, and extract document pages.
- Change portrait or landscape orientation of the document pages.
- Set, update or remove document password.
- Extract basic information about the document.

## Merge & Split File Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX
**Microsoft Visio:** VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
**Microsoft OneNote:** ONE
**OpenOffice:** ODT, OTT, ODP, OTP, ODS
**Markup:** HTML, MHT
**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB, CSV, TSV, TXT

## Page Manipulation File Formats

The following file formats are supported for trimming, moving, swapping pages or changing page orientation:
**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX
**Microsoft Visio:** VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
**Microsoft OneNote:** ONE
**OpenOffice:** ODT, OTT, ODP, OTP, ODS
**Markup:** HTML, MHT
**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB

## Page Rotation File Formats

**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB

## Getting Started

You do not need to install anything to get started with GroupDocs.Merger Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Merger-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Merger assembly in your project. If you already have GroupDocs.Merger Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Merger-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-dotnet) for other common usage scenarios.

## Merge Multiple Documents using C# Code

```csharp
var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
var apiInstance = new DocumentApi(configuration);
var item1 = new JoinItem
{
    FileInfo = new FileInfo
    {
    FilePath = "WordProcessing/four-pages.docx"
    }
};

var item2 = new JoinItem
{
    FileInfo = new FileInfo
    {
        FilePath = "WordProcessing/one-page.docx"
    }
};

var options = new JoinOptions
{
    JoinItems = new List<JoinItem> { item1, item2 },
    OutputPath = "Output/joined.docx"
};

var request = new JoinRequest(options);
var response = apiInstance.Join(request);
Console.WriteLine("Output file path: " + response.Path);
```

## Use C# to Split a DOCX File into Several Multi-Page Documents

```csharp
var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
var apiInstance = new DocumentApi(configuration);

var fileInfo = new FileInfo
{
    FilePath = "WordProcessing/sample-10-pages.docx"
};
var options = new SplitOptions
{
    FileInfo = fileInfo,
    OutputPath = "Output/split-to-multipage-document",
    Pages = new List<int?> { 3, 6, 8 },
    Mode = SplitOptions.ModeEnum.Intervals
};
var request = new SplitRequest(options);
var response = apiInstance.Split(request);
foreach (var document in response.Documents)
{
    Console.WriteLine("Output file path: " + document.Path);
}
```

[Product Page](https://products.groupdocs.cloud/merger/net) | [Documentation](https://wiki.groupdocs.cloud/mergercloud/) | [API Reference](https://apireference.groupdocs.cloud/merger/) | [Code Samples](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/merger/) | [Free Support](https://forum.groupdocs.cloud/c/merger) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
