# .NET API to Watermark Documents

This .NET component offers [read & write watermark](https://products.groupdocs.com/watermark/net) support for the documents of [40+ file formats](https://docs.groupdocs.com/display/watermarknet/Supported+Document+Formats). Supports watermark search, customization & extraction as well.

## Document Watermark Processing Features

- Add text and image watermark to supported document formats.
- Search and remove text and image watermarks.
- Search watermarks in particular objects.
- Apply watermark to images inside a document.
- Work with existing watermark objects.
- Extract information of watermark objects in a document.
- Perform PDF document rasterization.
- Fetch document basic information.
- Search watermarks by text formatting (font, color etc.).
- Set background image for charts in Excel and PowerPoint documents.
- Work with PDF and email attachments.

## New Features & Enhancements in Version 20.7

- Support of Linux for GroupDocs.Watermark for .NET Core.
- Removal of Legacy namespace.

## Important Notice

- In this version we have removed the Legacy API of GroupDocs.Watermark. So from version 20.7 `GroupDocs.Watermark.Legacy` does not exist anymore.

For the detailed notes, please visit [GroupDocs.Watermark for .NET 20.7 Release Notes](https://docs.groupdocs.com/watermark/net/groupdocs-watermark-for-net-20-7-release-notes/).

## Read & Write Watermark Formats

**Microsoft Word:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, RTF
**Microsoft Excel:** XLSX, XLSM, XLTM, XLT, XLTX, XLS
**Microsoft PowerPoint:** PPTX, PPTM, PPSX, PPSM, POTX, POTM, PPT, PPS
**Microsoft Visio:** VSD, VDX, VSDX, VSTX, VSS, VSSX, VSDM, VSSM, VSTM, VTX, VSX
**OpenOffice:** ODT
**Email:** EML, EMLX, OFT, MSG
**Fixed Layout:** PDF
**Image:** BMP, GIF, JPG/JPEG/JPE, JP2, PNG, TIFF, WEBP

## Platform Independence

GroupDocs.Watermark for .NET does not require any external software or third party tool to be installed. GroupDocs.Watermark for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up)
**Development Environments:** Microsoft Visual Studio (2010 & up)
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET frameworks.

## Getting Started with GroupDocs.Watermark for .NET

Are you ready to give GroupDocs.Watermark for .NET a try? Simply execute `Install-Package GroupDocs.Watermark` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Watermark assembly in your project. If you already have GroupDocs.Watermark for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Watermark` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-watermark/GroupDocs.Watermark-for-.NET) for other common usage scenarios.

## Using C# to Add Watermark to All Images on a PDF Page

```csharp
PdfLoadOptions loadOptions = new PdfLoadOptions();
// Constants.InDocumentPdf is an absolute or relative path to your document. Ex: @"C:\Docs\document.pdf"
using (Watermarker watermarker = new Watermarker(Constants.InDocumentPdf, loadOptions))
{
    // initialize image or text watermark
    TextWatermark watermark = new TextWatermark("Protected image", new Font("Arial", 8));
    watermark.HorizontalAlignment = HorizontalAlignment.Center;
    watermark.VerticalAlignment = VerticalAlignment.Center;
    watermark.RotateAngle = 45;
    watermark.SizingType = SizingType.ScaleToParentDimensions;
    watermark.ScaleFactor = 1;

    PdfContent pdfContent = watermarker.GetContent<PdfContent>();

    // get all images from the first page
    WatermarkableImageCollection images = pdfContent.Pages[0].FindImages();

    // add watermark to all found images
    foreach (WatermarkableImage image in images)
    {
        image.Add(watermark);
    }

    watermarker.Save(Constants.OutDocumentPdf);
}
```

## Search Watermarks in PDF using Regular Expression via C# Code

```csharp
// Constants.InDocumentPdf is an absolute or relative path to your document. Ex: @"C:\Docs\document.pdf"
using (Watermarker watermarker = new Watermarker(Constants.InDocumentPdf))
{
    Regex regex = new Regex(@"^Â© \d{4}$");

    // search by regular expression
    TextSearchCriteria textSearchCriteria = new TextSearchCriteria(regex);

    // find possible watermarks using regular expression
    PossibleWatermarkCollection possibleWatermarks = watermarker.Search(textSearchCriteria);

    Console.WriteLine("Found {0} possible watermark(s).", possibleWatermarks.Count);
}
```

[Product Page](https://products.groupdocs.com/watermark/net) | [Documentation](https://docs.groupdocs.com/watermark/net/) | [Demo](https://products.groupdocs.app/watermark/family) | [API Reference](https://apireference.groupdocs.com/net/watermark) | [Examples](https://github.com/groupdocs-watermark/GroupDocs.Watermark-for-.NET) | [Blog](https://blog.groupdocs.com/category/watermark/) | [Free Support](https://forum.groupdocs.com/c/watermark) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
