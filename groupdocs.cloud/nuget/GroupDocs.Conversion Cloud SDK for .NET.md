# .NET Cloud REST API for Document Conversion

This REST API allows your C#, ASP.NET & other .NET cloud-based apps to [convert documents](https://products.groupdocs.cloud/conversion/net) of 50+ file formats from within your apps without any 3rd party tool.

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

## New Features in Version 20.2

- **New Source Formats:** DIB, XLT, POT, XLAM, MPX, JPC, DWT, JPEG-LS.
- **New Target Formats:** WMF, EMF, XLAM.
- Supports encoding for source `CSV` and `TXT` documents.
- Supports `TimeZoneOffset` and `ConvertAttachments` for source Email documents.

## Enhancements in Version 20.2

- Improved quality of Diagram to Word document conversion.
- Converting multi-page `TIFF` to `PDF`.
- Improvement in `MPP` to `XLS` conversion.

For the detailed notes, please visit, [GroupDocs.Conversion Cloud 20.2 Release Notes](https://wiki.groupdocs.cloud/conversioncloud/release-notes/2020/groupdocs-conversion-cloud-20-2-release-notes/).

## Conversion File Formats

GroupDocs.Conversion Cloud SDK for .NET allows you to convert any of the following type of file formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLT, XLS2003, XLSB, XLSM, XLAM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX, POT
**Microsoft Visio:** VDW, VDX, VSD, VSDX, VSS, VST, VSX, VTX
**Microsoft Project:** MPP, MPT, MPX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**AutoCAD:** DWG, DWT, DXF
**Image:** BMP, GIF, ICO, JPEG, JPEG-LS, JPG, JPC, PNG, SVG, TIF, TIFF, DIB
**Email:** EML, EMLX, MSG
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML, MHT

to the following formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLS2003, XLSB, XLSM, XLAM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**Image:** BMP, GIF, ICO, JPEG, JPG, PNG, TIF, TIFF
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML
**Metafile:** WMF, EMF

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

[Product Page](https://products.groupdocs.cloud/conversion/net) | [Documentation](https://wiki.groupdocs.cloud/conversioncloud/) | [Live Demo](https://products.groupdocs.app/conversion/family) | [API Reference](https://apireference.groupdocs.cloud/conversion/) | [Examples](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/conversion/) | [Free Support](https://forum.groupdocs.cloud/c/conversion) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
