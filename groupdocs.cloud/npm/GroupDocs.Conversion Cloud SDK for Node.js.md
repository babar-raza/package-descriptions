This REST API allows your [Node.js cloud-based apps to convert documents](https://products.groupdocs.cloud/conversion/nodejs) of 50+ file formats from within your apps without any 3rd party tool.

## Cloud Document Conversion Features

- Specify document conversion settings.
- Specify page width & height while converting CAD diagrams.
- Choose [specific CAD diagram layouts to be converted](https://wiki.groupdocs.cloud/conversioncloud/getting-started/features-overview/).
- Substitute specific fonts during cells document conversion.
- Convert specific cell range while converting to non-cell formats.
- Skip empty rows and columns when converting cells documents.
- Display or hide email header, "from", "to", "cc" & "bcc".
- Substitute specific fonts when converted some supported formats.
- Start converting from specified page number.
- [Convert a specific number of pages](https://wiki.groupdocs.cloud/conversioncloud/developer-guide/common-conversion-options/convert-n-consecutive-pages/) from the specified page.
- Use PDF as an intermediary format while converting.
- Apply watermark during conversion process.

## Conversion File Formats

GroupDocs.Conversion Cloud SDK for Node.js allows you to convert any of the following type of file formats:
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

You do not need to install anything to get started with GroupDocs.Conversion Cloud SDK for Node.js. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

## Installation

A package groupdocs-conversion-cloud is available at [npmjs.com](https://www.npmjs.com/package/groupdocs-conversion-cloud). You can install it with:
`npm install groupdocs-conversion-cloud`

Please follow the [installation](https://www.npmjs.com/package/groupdocs-conversion-cloud#installation) procedure and then run the following JavaScript code:

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

[Product Page](https://products.groupdocs.cloud/conversion/nodejs) | [Documentation](https://wiki.groupdocs.cloud/conversioncloud/) | [API Reference](https://apireference.groupdocs.cloud/conversion/) | [Code Samples](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/conversion/) | [Free Support](https://blog.groupdocs.cloud/category/conversion/) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
