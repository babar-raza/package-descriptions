# .NET Cloud REST API to Watermark Documents

Use this REST API to enable your cloud-based C#, ASP.NET, & other .NET apps to [search, edit, remove & add watermarks](https://products.groupdocs.cloud/watermark/net) to documents of 40+ different file formats.

## Cloud Document Watermarking Features

- Add text or image watermarks to documents of supported formats.
- Create watermarks for specific pages only.
- Specify physical attributes of the watermark, e.g., size, font, color etc.
- Search for the collection of image or text-based watermarks inside a document.
- Edit properties of the existing editable watermarks.
- Remove watermarks from specific pages or remove specific watermarks from the document.

## New features in Version 19.12

- This is the first release of a completely new version of the GroupDocs.Watermark.Cloud API.

For the detailed notes, please visit [GroupDocs.Watermark Cloud 19.12 Release Notes](https://wiki.groupdocs.cloud/watermarkcloud/release-notes/release-notes-2019/groupdocs-watermark-cloud-19-12/).

## Supported File Formats

The following file formats support the adding, removing, searching, and replacing watermark:
**Microsoft Word:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, RTF
**Microsoft Excel:** XLSX, XLSM, XLTM, XLT, XLTX, XLS
**Microsoft PowerPoint:** PPTX, PPTM, PPSX, PPSM, POTX, POTM, PPT, PPS
**Microsoft Visio:** VSD, VDX, VSDX, VSTX, VSS, VSSX, VSDM, VSSM, VSTM, VTX, VSX
**OpenOffice:** ODT
**Image:** BMP, GIF, JPG, JPEG, JPE, JP2, PNG, TIFF, WEBP
**Portable:** PDF

## Getting Started

You do not need to install anything to get started with GroupDocs.Watermark Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Watermark-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Watermark assembly in your project. If you already have GroupDocs.Watermark Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Watermark-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-watermark-cloud/groupdocs-watermark-cloud-dotnet) for other common usage scenarios.

## Get Watermark Supported File Formats

```csharp
string MyAppKey = "";
string MyAppSid = "";

var configuration = new Configuration(MyAppSid, MyAppKey);
var apiInstance = new InfoApi(configuration);
  
var response = apiInstance.GetSupportedFileFormats();
```

## Using C# to Add Image Watermark to DOCX file

```csharp
string MyAppKey = "";
string MyAppSid = "";

var configuration = new Configuration(MyAppSid, MyAppKey);
var apiInstance = new ParseApi(configuration);
var fileInfo = new FileInfo
{
    FilePath = "documents/input.docx",
};
var options = new WatermarkOptions()
{
    FileInfo = fileInfo,
    WatermarkDetails = new List<WatermarkDetails>
    {
        new WatermarkDetails
        {
            ImageWatermarkOptions = new ImageWatermarkOptions()
            {
                Image = new FileInfo { FilePath = "watermark_images/sample_watermark.png" }
            }
        }
    },
    ProtectLevel = WatermarkOptions.ProtectLevelEnum.DocumentAndImages
};
var request = new AddRequest(options);
var response = apiInstance.Add(request);
```

[Product Page](https://products.groupdocs.cloud/watermark/net) | [Documentation](https://wiki.groupdocs.cloud/watermarkcloud/) | [Demo](https://products.groupdocs.app/watermark/family) | [API Reference](https://apireference.groupdocs.cloud/watermark/) | [Examples](https://github.com/groupdocs-watermark-cloud/groupdocs-watermark-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/watermark/) | [Free Support](https://forum.groupdocs.cloud/c/watermark) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
