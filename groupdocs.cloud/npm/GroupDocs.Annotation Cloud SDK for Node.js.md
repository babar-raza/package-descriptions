Node.js Cloud SDK wraps GroupDocs.Annotation Cloud API so you could seamlessly integrate Document Annotation features into your own Node.js apps.

# Document Annotation in the Cloud

[GroupDocs.Annotation Cloud SDK for Node.js](https://products.groupdocs.cloud/annotation/nodejs) helps developers implement document annotation for over 35 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe, metafile, markup & image file formats, and add area, arrow, distance, point, polyline, text or watermark annotation. 

Check out the [API Reference](https://apireference.groupdocs.cloud/annotation/) to know all about the GroupDocs.Annotation REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## Addon Features

- Load protected documents.
- Add, remove or extract document annotation.
- Generate image representation from document pages.
- Inspect document information.
- Get & set various annotation settings.
- [Export annotation](https://wiki.groupdocs.cloud/annotationcloud/developer-guide/working-with-annotations/#HExportAnnotationandgetDocumentasStream) information to a document.
- [Render documents to PDF](https://wiki.groupdocs.cloud/annotationcloud/developer-guide/rendering-documents/).
- Integrated storage API.

## New Features in Version 19.5

- This is the first release of a completely new version of the API `GroupDocs.Annotation.Cloud v2.0`.
- `V2` provides much simpler and intuitive API comparing with `V1`.
- `V2` includes Storage and File API which enables users to manage storage and files.

For the detailed notes, please visit [GroupDocs.Annotation Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/annotationcloud/release-notes/2019/groupdocs-annotation-cloud-19-5-release-notes/).

## Supported Annotation Formats

GroupDocs.Annotation Cloud API [supports 35+ file formats](https://wiki.groupdocs.cloud/annotationcloud/getting-started/supported-document-formats/) that it can load & annotate.

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

## Getting Started with GroupDocs.Annotation Cloud SDK for Node.js

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-node). You can either directly use it in your project via source code or get NPM distribution via `npm install groupdocs-annotation-cloud`.

Execute following snippet to load supported formats.

```js
// load the module
var GroupDocs = require('groupdocs-annotation-cloud');

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct AnnotationApi
var infoApi = GroupDocs.InfoApi.fromKeys(appSid, appKey);

// retrieve supported file-formats
infoApi.getSupportedFileFormats()
    .then(function (response) {
        console.log("Supported file-formats:")
        response.formats.forEach(function (format) {
            console.log(format.fileFormat + " (" + format.extension + ")");
        });
    })
    .catch(function (error) {
        console.log("Error: " + error.message)
    });
```

Or compile and run same written in TypeScript:

```js
// load the module
import { InfoApi } from "groupdocs-annotation-cloud";

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
const appSid: string = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
const appKey: string = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct AnnotationApi
const infoApi: InfoApi = InfoApi.fromKeys(appSid, appKey);

// retrieve supported file-formats
infoApi.getSupportedFileFormats()
    .then((result) => {
        console.log("Supported file-formats:");
        result.formats.forEach((format) => {
            console.log(format.fileFormat + " (" + format.extension + ")");
        });
    })
    .catch((error) => {
        console.log("Error: " + error.message);
    });
```

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

## Licensing

GroupDocs.Annotation Cloud Node.js SDK licensed under [MIT License](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-node/blob/HEAD/LICENSE).

[Product Page](https://products.groupdocs.cloud/annotation/nodejs) | [Documentation](https://wiki.groupdocs.cloud/annotationcloud/) | [API Reference](https://apireference.groupdocs.cloud/annotation/) | [Examples](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/annotation/) | [Free Support](https://forum.groupdocs.cloud/c/annotation) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
