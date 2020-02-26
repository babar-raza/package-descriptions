This REST API enhances your Node.js cloud apps to import, export & process text & figure annotations within documents for 35+ file formats.

## Cloud Document Annotation Features

- Fetch document description with meta data and coordinates of text on pages.
- Fetch annotation data from files of supported formats.
- Import annotation information from documents.
- [Export annotation](https://wiki.groupdocs.cloud/annotationcloud/developer-guide/working-with-annotations/#HExportAnnotationandgetDocumentasStream) information to a document and fetch it as a stream.
- Remove document annotations.
- Get image representation of the document pages.
- [Render documents to PDF](https://wiki.groupdocs.cloud/annotationcloud/developer-guide/rendering-documents/) format with storage URL or stream output.
- Add or remove document or image annotations of various types.

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

You do not need to install anything to get started with GroupDocs.Annotation Cloud SDK for Node.js. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install GroupDocs.Annotation for Cloud via NPM, please execute from the command line, `npm install groupdocs-annotation-cloud`.

## Add Text Annotation using Node.js

```js
"use strict";
class Annotation_Node_Add_Area_Annotation {
    static Run() {

        let a1 = new groupdocs_annotation_cloud_1.AnnotationInfo();
        a1.annotationPosition = new groupdocs_annotation_cloud_1.Point();
        a1.annotationPosition.x = 852;
        a1.annotationPosition.y = 59.388262910798119;
        a1.box = new groupdocs_annotation_cloud_1.Rectangle();
        a1.box.x = 375.89276123046875;
        a1.box.y = 59.388263702392578;
        a1.box.width = 88.7330551147461;
        a1.box.height = 37.7290153503418;
        a1.pageNumber = 2;
        a1.penColor = 1201033;
        a1.penStyle = 0;
        a1.penWidth = 1;
        a1.type = groupdocs_annotation_cloud_1.AnnotationInfo.TypeEnum.Area;
        a1.text = "This is area annotation";
        a1.creatorName = "Anonym A.";

        var request = new groupdocs_annotation_cloud_1.PostAnnotationsRequest("Annotationdocs\\ten-pages.pdf", [a1]);
        annotateApi.postAnnotations(request)
        .then(function (response) {
            console.log("Expected response type is void: Area Annotation added.");
        })
        .catch(function (error) {
            console.log("Error: " + error.message);
        });
    }
}
module.exports = Annotation_Node_Add_Area_Annotation;
```

[Product Page](https://products.groupdocs.cloud/annotation/nodejs) | [Documentation](https://wiki.groupdocs.cloud/annotationcloud/) | [API Reference](https://apireference.groupdocs.cloud/annotation/) | [Code Samples](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/annotation/) | [Free Support](https://forum.groupdocs.cloud/c/annotation) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
