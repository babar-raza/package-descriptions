# Document Annotation .NET Cloud REST API

This REST API enhances your C#, ASP.NET & other .NET cloud apps to [import, export & process text & figure annotations](https://products.groupdocs.cloud/annotation/net) within documents for 35+ file formats.

## Cloud Document Annotation Features

- Fetch document description with meta data and coordinates of text on pages.
- Fetch annotation data from files of supported formats.
- Import annotation information from documents.
- Export annotation information to a document and fetch it as a stream.
- Remove document annotations.
- Get image representation of the document pages.
- Render documents to PDF format with storage URL or stream output.
- Add or remove document or image annotations of various types.

## New Features in Version 19.5

- This is the first release of a completely new version of the API `GroupDocs.Annotation.Cloud v2.0`.
- `V2` provides much simpler and intuitive API comparing with `V1`.
- `V2` includes Storage and File API which enables users to manage storage and files.

For the detailed notes, please visit [GroupDocs.Annotation Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/annotationcloud/release-notes/2019/groupdocs-annotation-cloud-19-5-release-notes/).

## Supported Annotation Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF, TXT
**Microsoft Excel:** XLS, XLSX, XLSB, XLSX
**Microsoft PowerPoint:** PPT, PPTX, PPSX
**Microsoft Visio:** VSD, VDX, VSS, VSDM
**OpenOffice:** OTT, ODT, ODP, OTP
**Image:** JPEG, TIFF, BMP, GIF, DJVU
**Metafile:** EMF, WMF
**Email:** EML, EMLX, MSG
**Portable:** PDF
**Medical Imagery:** DICOM
**Markup:** HTML, MHTML
**AutoCAD:** CAD

## Supported Text Annotation Types

**Text annotation** – add comments to selected text.
**Text replacement** – highlight which text should be replaced with what.
**Text redaction** – hide confidential text.
**Strikeout/underline** – highlight text with strikethroughs/underlines.
**Typewriter** – add sticky notes with rich text.

## Supported Figure Annotation Types

**Area annotation** – add notes to an area highlighted with a rectangle.
**Point annotation** – add notes to any point in the document.
**Area redaction** – hide confidential parts of an image or text.
**Polyline** – draw freehand lines and shapes.
**Pointer/arrow** – drop arrows pointing to an object.
**Watermark** – create text-based watermark overlays.
**Distance** – measure the distance between any objects in a document.

## Platform Independence

GroupDocs.Annotation Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with GroupDocs.Annotation Cloud SDK for .NET. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Annotation-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Annotation assembly in your project. If you already have GroupDocs.Annotation Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Annotation-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-dotnet) for other common usage scenarios.

## Use C# to Export Annotations and get Document as Stream

```csharp
var configuration = new Configuration
{
    AppSid = Sid,
    AppKey = Key
};

var apiInstance = new AnnotationApi(configuration);

List<AnnotationInfo> annotations = new List<AnnotationInfo>();
AnnotationInfo annotation = new AnnotationInfo
{
    AnnotationPosition = new Point(852, 154.31),
    Replies = new[]
    {
        new AnnotationReplyInfo {Message = "reply text", RepliedOn = DateTime.Now, UserName = "Admin"},
        new AnnotationReplyInfo
        {
            Message = "reply2 text",
            RepliedOn = DateTime.Now,
            UserName = "Commentator"
        }
    },
    Box = new Rectangle((float)173.29, (float)154.31, (float)142.5, 9),
    PageNumber = 0,
    SvgPath =
        "[{\"x\":173.2986,\"y\":687.5769},{\"x\":315.7985,\"y\":687.5769},{\"x\":173.2986,\"y\":678.5769},{\"x\":315.7985,\"y\":678.5769}]",
    Type = AnnotationType.Text,
    CreatorName = "Anonym A."
};
annotations.Add(annotation);
PutExportRequest request = new PutExportRequest()
{
    Name ="Annotated.pdf",
    Folder=null,
    Password=null,
    Body=annotations,
};
// Insert/Export annotations to document.
var response = apiInstance.PutExport(request);
Debug.Print("Document Processsed and stream length: " + response.Length);
```

[Product Page](https://products.groupdocs.cloud/annotation/net) | [Documentation](https://wiki.groupdocs.cloud/annotationcloud/) | [API Reference](https://apireference.groupdocs.cloud/annotation/) | [Code Samples](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/annotation/) | [Free Support](https://forum.groupdocs.cloud/c/annotation) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
