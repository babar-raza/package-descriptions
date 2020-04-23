Node.js Cloud SDK wraps GroupDocs.Conversion Cloud API so you could seamlessly integrate Document Conversion features into your own Node.js apps.

# Document Conversion in the Cloud

[GroupDocs.Conversion Cloud SDK for Node.js](https://products.groupdocs.cloud/conversion/nodejs) helps developers implement document conversion for over 50 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe, CAD, markup & image file formats, and export to various other formats. 

Check out the [API Reference](https://apireference.groupdocs.cloud/conversion/) to know all about the GroupDocs.Conversion REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try it from Swagger UI.

## Conversion Utility Features

- Load password protected documents.
- Protect destination document (if supported).
- Convert specific document pages.
- Convert N consecutive pages.
- Add watermark to destination document.
- Get document metadata.
- Get possible conversion options for any input document.
- Use PDF as an intermediary format while converting.
- Integrated storage API.

## Document Specific REST Models

- Convert specific cell range, skip empty rows & columns or substitute font during Excel document conversion.
- Display or hide email headers like "from", "to", "cc" & "bcc".
- Adjust resolution, contrast, brightness or gamma for image conversion. Also rotate, flip or convert to grayscale.
- Set page's DPI & zoom level while converting Word documents.
- Render specific CAD layouts.

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

GroupDocs.Conversion Cloud SDK for Node.js allows you to convert any of the following type of file formats:
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

## Getting Started with GroupDocs.Conversion Cloud SDK for Node.js

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-node). You can either directly use it in your project via source code or get NPM distribution `npm install groupdocs-conversion-cloud`.


Execute following snippet to load all supported conversion formats.

```js
// load the module
var GroupDocs = require('groupdocs-conversion-cloud');

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct Api
var api = GroupDocs.InfoApi.fromKeys(appSid, appKey);
var request = new GroupDocs.GetSupportedConversionTypesRequest();
// retrieve supported conversion types
api.getSupportedConversionTypes(request)
    .then(function (response) {
        console.log("Supported file-formats:")
        response.forEach(function (format) {
            console.log(format.sourceFormat + ": [" + format.targetFormats.join(", ") + "]");
        });
    })
    .catch(function (error) {
        console.log("Error: " + error.message)
    });
```

Or compile and run same written in TypeScript:

```js
// load the module
import { INfoApi, GetSupportedConversionTypesRequest } from "groupdocs-conversion-cloud";

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
const appSid: string = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
const appKey: string = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct Api
const api: InfoApi = InfoApi.fromKeys(appSid, appKey);

const request: GetSupportedConversionTypesRequest = new GetSupportedConversionTypesRequest();

// retrieve supported file-formats
api.getSupportedConversionTypes(request)
    .then((result) => {
        console.log("Supported file-formats:");
        result.forEach((format) => {
            console.log(format.sourceFormat + ": [" + format.targetFormats.join(", ") + "]");
        });
    })
    .catch((error) => {
        console.log("Error: " + error.message);
    });
```

## Use Node.js to Convert PDF Document to DOCX Format

```js
"use strict";
class Conversion_Node_Convert_To_Words {
    static Run() {

        var settings = new groupdocs_conversion_cloud_1.ConvertSettings();
        settings.storageName = myStorage;
        settings.filePath = "converted/topdf/password-protected.pdf";
        settings.format = "docx";

        var loadOptions = new groupdocs_conversion_cloud_1.PdfLoadOptions();
        loadOptions.password = "password";
        loadOptions.hidePdfAnnotations = true;
        loadOptions.removeEmbeddedFiles = false;
        loadOptions.flattenAllFields = true;

        settings.loadOptions = loadOptions;

        var convertOptions = new groupdocs_conversion_cloud_1.DocxConvertOptions();
        convertOptions.fromPage = 1;
        convertOptions.pagesCount = 1;

        settings.convertOptions = convertOptions;
        settings.outputPath = "converted/todocx";

        var request = new groupdocs_conversion_cloud_1.ConvertDocumentRequest(settings);
        convertApi.convertDocument(request)
        .then(function (response) {
            console.log("Document converted successfully: " + response[0].url);
        })

        .catch(function (error) {
            console.log("Error: " + error.message);
        });
    }
}
module.exports = Conversion_Node_Convert_To_Words;
```

## Licensing

GroupDocs.Conversion Cloud SDK for Node.js licensed under [MIT License](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-node/blob/HEAD/LICENSE).

[Product Page](https://products.groupdocs.cloud/conversion/nodejs) | [Documentation](https://wiki.groupdocs.cloud/conversioncloud/) | [Demo](https://products.groupdocs.app/conversion/family) | [API Reference](https://apireference.groupdocs.cloud/conversion/) | [Examples](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/conversion/) | [Free Support](https://blog.groupdocs.cloud/category/conversion/) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
