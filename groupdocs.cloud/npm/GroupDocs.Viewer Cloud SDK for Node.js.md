Node.js Cloud SDK wraps GroupDocs.Viewer Cloud API so you could seamlessly integrate Document Viewing features into your own Node.js apps.

# View Documents in the Cloud

[GroupDocs.Viewer Cloud SDK for Node.js](https://products.groupdocs.cloud/viewer/nodejs) helps developers implement document merging for over 85+ file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Visio®, Project®, Adobe, markup & image file formats to view as HTML, PDF or images. 

Check out the [API Reference](https://apireference.groupdocs.cloud/viewer/) to know all about the GroupDocs.Viewer REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## Addon Document Viewing Features

- [Render documents pages](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/rendering-document-pages/) as images.
- Fetch the list of all installed fonts or delete the fonts cache.
- Download HTML page resources, e.g., images, CSS, fonts etc.
- Render document as PDF, HTML or image representation and download as ZIP.
- Fetch document information via various methods.
- Obtain list of links to document pages as HTML.
- Rotate and reorder document pages.
- Specify image quality while rendering PDF as HTML.
- Decrease the resultant file size by excluding fonts.
- Render specific sections of worksheets defined as "Print Area".
- Choose to include or exclude hidden content.
- Save result in [minified HTML and SVG](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/minification-of-html-and-svg/).
- Render documents [responsive HTML](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/rendering-document-to-responsive-html/).
- Render email messages & Outlook data files.
- Integrated storage API.

## New Features in Version 19.5.0

- Improve Cloud products API Reference grouping.

For the detailed notes, please visit [GroupDocs.Viewer Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/viewercloud/release-notes/2019/groupdocs-viewer-cloud-19-5-release-notes/).

## Supported File Formats

GroupDocs.Viewer Cloud API [supports 85+ file formats](https://wiki.groupdocs.cloud/viewercloud/getting-started/supported-document-formats/) that it can load & render.

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

## Getting Started with GroupDocs.Viewer Cloud SDK for Node.js

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node). You can either directly use it in your project via source code or get NPM distribution via `npm install groupdocs-viewer-cloud`.

Execute following snippet to load supported document formats.

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
