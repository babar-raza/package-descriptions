This REST API allows your C#, ASP.NET & other .NET cloud-based apps to convert documents of 50+ file formats from within your apps without any 3rd party tool.

## Cloud Document Conversion Features

- Specify document conversion settings.
- Specify page width & height while converting CAD diagrams.
- Choose specific CAD diagram layouts to be converted.
- Substitute specific fonts during cells document conversion.
- Convert specific cell range while converting to non-cell formats.
- Skip empty rows and columns when converting cells documents.
- Display or hide email header, "from", "to", "cc" & "bcc".
- Substitute specific fonts when converted some supported formats.
- Start converting from specified page number.
- Convert a specific number of pages from the specified page.
- Use PDF as an intermediary format while converting.
- Apply watermark during conversion process.

## Conversion File Formats

GroupDocs.Conversion Cloud SDK for .NET allows you to convert any of the following type of file formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLS2003, XLSB, XLSM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX
**Microsoft Visio:** VDW, VDX, VSD, VSDX, VSS, VST, VSX, VTX
**Microsoft Project:** MPP, MPT
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**AutoCAD:** DWG, DXF
**Image:** BMP, GIF, ICO, JPEG, JPG, PNG, SVG, TIF, TIFF
**Email:** EML, EMLX, MSG
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML, MHT

to the following formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLS2003, XLSB, XLSM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**Image:** BMP, GIF, ICO, JPEG, JPG, PNG, TIF, TIFF
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML

## Platform Independence

GroupDocs.Conversion Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with GroupDocs.Conversion Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Conversion-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Conversion assembly in your project. If you already have GroupDocs.Conversion Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Conversion-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-dotnet) for other common usage scenarios.

## Convert a DOCX file to the specified format via C# Code

```csharp
var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);

var apiInstance = new ConvertApi(configuration);

// convert settings
var settings = new ConvertSettings
{
    StorageName = Common.MyStorage,
    FilePath = "conversions/sample.docx",
    Format = convertToFormat,
    ConvertOptions = convertOptions,
    OutputPath = "converted/" + convertToFormat
};

// convert to specified format
List<StoredConvertedResult> response = apiInstance.ConvertDocument(new ConvertDocumentRequest(settings));
Console.WriteLine("Document converted successfully: " + response[0].Url);
```

[Product Page](https://products.groupdocs.cloud/conversion/net) | [Documentation](https://wiki.groupdocs.cloud/conversioncloud/) | [API Reference](https://apireference.groupdocs.cloud/conversion/) | [Code Samples](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/conversion/) | [Free Support](https://forum.groupdocs.cloud/c/conversion) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)