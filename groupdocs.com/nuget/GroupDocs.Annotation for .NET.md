# .NET API for Document Annotation

Its an on-premise API that seamlessly [integrates document annotation features](https://products.groupdocs.com/annotation/net) into your .NET applications. Apply graphic, text and watermark annotations.

## Document Annotation Processing Features

- Import document annotations.
- Support for adding, removing or replying to annotation comments.
- Export annotated document back to its original format.
- Render document pages as images.
- Generate document thumbnails or document image preview.
- Support for default cache (local disk) or custom cache (Amazon S3,Dropbox etc.).
- [Get list](https://docs.groupdocs.com/display/annotationnet/Get+supported+file+formats) of [supported file formats](https://docs.groupdocs.com/display/annotationnet/Supported+Document+Formats).
- Fetch document information, such as, page count & file size.
- [Extract annotations from a document](https://docs.groupdocs.com/display/annotationnet/Extract+annotations+from+document) and serialize to XML format.
- Remove previously added annotations from a document.
- Update specific annotation properties (size, color etc.).

## New Features in Version 20.4

- Managing different versions of annotated file (supported formats: Words, PDF, Slides, SpreadSheets).

## Enhancements in Version 20.4

- Added to new API getting pages image size.
- Added advanced rendering options for show\hide replies.

For the detailed list, please visit [GroupDocs.Annotation for .NET 20.4 Release Notes](https://docs.groupdocs.com/display/annotationnet/GroupDocs.Annotation+for+.NET+20.4+Release+Notes).

## Microsoft Office Annotation Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX
**Microsoft PowerPoint:** PPT, PPTX, PPSX, PPS
**Microsoft Visio:** VSD, VSDX, VSS, VST

## Other Annotation Formats

**Portable:** PDF (PDF/A-1a, PDF/A-1b, PDF/A-2a)
**OpenDocument:** ODT, ODS, ODP
**Images:** TIF, TIFF, JPG, JPEG, PNG, BMP
**AutoCAD:** DWG, DXF
**Email:** EML
**Web:** HTML
**Others:** DCM

## Supported Graphic Annotation Types

**Area:** marks an area with a rectangle
**Arrow:** draws an arrow on a document
**Distance:** measures a distance between objects in a document
**Ellipse:** draws elliptic annotation in a document
**Point:** sticks comments to any point in a document
**Polyline:** draws shapes and freehand lines
**Resource Redaction:** fills black rectangle with fixed position
**TextField:** adds rectangle with a text inside

## Supported Text Annotation Types

**Highlight:** highlights and comments selected text
**Link:** adds a hyperlink to the document
**Replacement:** replaces original text with user’s text
**Strikeout:** marks text with a strikethrough styling
**Text Redaction:** fills part of text with black rectangle
**Underline:** marks text with an underline styling

## Supported Watermark Annotation Types

**Diagonal:** adds diagonal text watermark
**Horizontal:** adds horizontal text watermark

## Supported Platforms

GroupDocs.Annotation for .NET supported platforms are listed below:
**.NET Standard 2.0:** Any type of .NET Standard 2.0 application is supported (since Q4 2019).
**.NET Framework:** Any type of .NET Framework version 2.0 (or later) application is supported - ASP.NET, Web Services, WinForms, WPF and others. Full support for 32-bit and 64-bit.
**Windows Azure:** GroupDocs.Annotation for .NET runs on Windows Azure.
**Mono:** You can use GroupDocs.Annotation for .NET to build applications with Mono.

## Getting Started with GroupDocs.Annotation for .Net

Are you ready to give GroupDocs.Annotation for .NET a try? Simply execute `Install-Package GroupDocs.Annotation` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Annotation assembly in your project. If you already have GroupDocs.Annotation for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Annotation` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-annotation/GroupDocs.Annotation-for-.NET) for other common usage scenarios.

## Use C# Code to Save Annotation-only Pages of PDF File

```csharp
// for this example input file ("input.pdf") must have at least 10 pages
using (Annotator annotator = new Annotator(“input.pdf”))
{
    AreaAnnotation area = new AreaAnnotation()
    {
        Box = new Rectangle(100, 100, 100, 100),
        BackgroundColor = 65535,
        PageNumber = 1
    };
    EllipseAnnotation ellipse = new EllipseAnnotation()
    {
        Box = new Rectangle(100, 100, 100, 100),
        BackgroundColor = 123456,
        PageNumber = 9
    };
    annotator.Add(new List<AnnotationBase>() { area, ellipse });
    annotator.Save(“result.pdf” new SaveOptions { OnlyAnnotatedPages = true});
}
```

[Product Page](https://products.groupdocs.com/annotation/net) | [Documentation](https://docs.groupdocs.com/display/annotationnet/Home) | [API Reference](https://apireference.groupdocs.com/net/annotation) | [Code Samples](https://github.com/groupdocs-annotation/GroupDocs.Annotation-for-.NET) | [Blog](https://blog.groupdocs.com/category/annotation/) | [Free Support](https://forum.groupdocs.com/c/annotation) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
