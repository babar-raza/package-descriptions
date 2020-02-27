This REST API enhances your Node.js based cloud apps to [render 85+ types of file formats](https://products.groupdocs.cloud/viewer/nodejs) to image, PDF or HTML formats from within your apps.

## Cloud Document Viewer Features

- Support for [rendering](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/rendering-document-pages/) lots of document and image file formats.
- Fetch the list of all installed fonts or delete the fonts cache.
- Download HTML page resources, e.g., images, CSS, fonts etc.
- Render a document to PDF for HTML or image representation and download it.
- Fetch document information via various methods.
- Obtain list of links to document pages as HTML or images.
- Fetch and download ZIP archive of document pages as HTML or images.
- Rotate and reorder document pages.
- Specify image quality while rendering PDF as HTML.
- Decrease the resultant file size by excluding fonts when rendering as HTML.
- Render specific sections of worksheets defined as "print area" as HTML.
- Choose to include or exclude hidden content in Excel documents.
- Make the output content in [HTML and SVG minified](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/minification-of-html-and-svg/).
- Render a document to [responsive HTML](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/rendering-document-to-responsive-html/).
- Render email messages & render Outlook data files as HTML.
- Get list of all email attachments in its HTML or image representation.
- Download resources of a specific email attachment page for HTML representation.

## Supported File Formats

**Word Processing:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Spreadsheet:** XLS, XLSB, XLSM, XLSX, ODS, OTS, CSV, TSV
**Presentation:** PPT, PPTM, PPTX, PPS, PPSM, PPSX, POTX, POTM, ODP, OTP
**Project Management:** MPP, MPT
**Email:** EML, EMLX, MSG, OST, PST
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**Markup:** HTML, MHTML
**Diagram:** VDW, VDX, VSD, VSDM, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Note:** ONE
**Portable:** PDF, TEX, XPS
**Image:** BMP, CGM, DCM, DJVU, DNG, EMF, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PCL, PNG, PS, PSD, SVG, TIF, TIFF, WEBP, WMF
**eBook:** EPUB, MOBI

## Platform Independence

GroupDocs.Viewer Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Installation

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

A package `groupdocs-viewer-cloud` is available at [npmjs.com](https://www.npmjs.com/package/groupdocs-viewer-cloud). You can install it with:

`npm install groupdocs-viewer-cloud`

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

## Getting Started

Please follow the [installation](https://www.npmjs.com/package/groupdocs-viewer-cloud#installation) procedure and then run the following JavaScript code:

```js
// load the module
var GroupDocs = require('groupdocs-viewer-cloud');

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct ViewerApi
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
import { InfoApi } from "groupdocs-viewer-cloud";

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
const appSid: string = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
const appKey: string = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct ViewerApi
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

## Render Document Pages using Node.js

```js
public async createView(requestObj: model.CreateViewRequest): Promise<model.ViewResult> {
        if (requestObj === null || requestObj === undefined) {
            throw new Error('Required parameter "requestObj" was null or undefined when calling createView.');
        }

        const localVarPath = this.configuration.getServerUrl() + "/viewer/view";
        const queryParameters: any = {};

        // verify required parameter 'requestObj.viewOptions' is not null or undefined
        if (requestObj.viewOptions === null || requestObj.viewOptions === undefined) {
            throw new Error('Required parameter "requestObj.viewOptions" was null or undefined when calling createView.');
        }

        const requestOptions: request.Options = {
            method: "POST",
            qs: queryParameters,
            uri: localVarPath,
            json: true,
            body: Serializer.serialize(requestObj.viewOptions, requestObj.viewOptions.constructor.name === "Object" ? "ViewOptions" : requestObj.viewOptions.constructor.name),
        };

        const response = await invokeApiMethod(requestOptions, this.configuration);
        const result =  Serializer.deserialize(response.body, "ViewResult");
        return Promise.resolve(result);
    }
```

## Licensing

GroupDocs.Viewer Cloud Node.js SDK licensed under [MIT License](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node/blob/HEAD/LICENSE).

[Product Page](https://products.groupdocs.cloud/viewer/nodejs) | [Documentation](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node) | [API Reference](https://apireference.groupdocs.cloud/viewer/) | [Code Samples](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/viewer/) | [Free Support](https://forum.groupdocs.cloud/c/viewer) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
