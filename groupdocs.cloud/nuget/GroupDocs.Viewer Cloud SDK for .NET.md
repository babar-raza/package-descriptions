# .NET Cloud REST API for Document Rendering

This REST API enhances your C#, ASP.NET, & other .NET based cloud apps to [render](https://products.groupdocs.cloud/viewer/net) 85+ types of file formats to image, PDF or HTML formats from within your apps.

## Cloud Document Viewer Features

- Support for rendering lots of document and image file formats.
- Fetch the list of all installed fonts or delete the fonts cache.
- Download HTML page resources, e.g., images, CSS, fonts etc.
- Render a document to PDF for HTML or image representation and download it.
- Fetch document information via various methods.
- Obtain list of links to document pages as HTML or images.
- Fetch and download ZIP archive of document pages as HTML or images.
- Rotate and reorder document pages.
- Specify image quality while rendering PDF as HTML.
- Decrease the resultant file size by excluding fonts when rendering as HTML.
- Render specific sections of worksheets defined as "print area" as HTML.
- Choose to include or exclude hidden content in Excel documents.
- Make the output content in HTML and SVG minified.
- Render a document to responsive HTML.
- Render email messages & render Outlook data files as HTML.
- Get list of all email attachments in its HTML or image representation.
- Download resources of a specific email attachment page for HTML representation.

## Enhancements in Version 19.5

- Improved Cloud products API Reference grouping.

For the detailed notes, please visit [GroupDocs.Viewer Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/viewercloud/release-notes/2019/groupdocs-viewer-cloud-19-5-release-notes/).

## Supported File Formats

**Word Processing:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Spreadsheet:** XLS, XLSB, XLSM, XLSX, ODS, OTS, CSV, TSV
**Presentation:** PPT, PPTM, PPTX, PPS, PPSM, PPSX, POTX, POTM, ODP, OTP
**Project Management:** MPP, MPT
**Email:** EML, EMLX, MSG, OST, PST
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**Markup:** HTML, MHTML
**Diagram:** VDW, VDX, VSD, VSDM, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Note:** ONE
**Portable:** PDF, TEX, XPS
**Image:** BMP, CGM, DCM, DJVU, DNG, EMF, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PCL, PNG, PS, PSD, SVG, TIF, TIFF, WEBP, WMF
**eBook:** EPUB, MOBI

## Getting Started

You do not need to install anything to get started with GroupDocs.Viewer Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Viewer-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Viewer assembly in your project. If you already have GroupDocs.Viewer Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Viewer-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet) for other common usage scenarios.

## Render DOCX Page as Responsive HTML

```csharp
var configuration = new Configuration
{
    AppSid = Sid,
    AppKey = Key
};

var apiInstance = new ViewerApi(configuration);

var request = new HtmlGetPageRequest
{
    FileName = "input.docx",
    EnableResponsiveRendering = true,
    PageNumber = 1,
    EmbedResources = true,
    Folder = null,
    Storage = null,
};

var response = apiInstance.HtmlGetPage(request);

Debug.Print("Result as IO Stream :" + response.Length.ToString());
```

## Use C# to Render Outlook Data Files as HTML

```csharp
var configuration = new Configuration("XXXX-XXXX-XXX", "XXXXXXXXXXX");

var apiInstance = new ViewerApi(configuration);

var file = "data.pst";
var htmlOptions = new HtmlOptions
{
    EmbedResources = true,
    OutlookOptions = new OutlookOptions
    {
        MaxItemsInFolder = 5
    }
};

var request = new HtmlCreatePagesCacheFromContentRequest
{
    HtmlOptions = this.SerializeObject(htmlOptions),
    File = this.GetTestFileStream(file),
    FileName = null,
    FontsFolder = null,
    Folder = FromContentFolder,
    Storage = null,
};

var response = apiInstance.HtmlCreatePagesCacheFromContent(request);

Console.Write("File name:" + response.FileName);
Console.Write("PageCount: " + response.Pages.Count);
```

[Product Page](https://products.groupdocs.cloud/viewer/net) | [Documentation](https://wiki.groupdocs.cloud/viewercloud/) | [Live Demo](https://products.groupdocs.app/viewer/family) | [API Reference](https://apireference.groupdocs.cloud/viewer/) | [Code Samples](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/viewer/) | [Free Support](https://forum.groupdocs.cloud/c/viewer) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
