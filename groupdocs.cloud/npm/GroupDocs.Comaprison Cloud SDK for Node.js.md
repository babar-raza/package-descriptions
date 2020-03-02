This cloud REST API enhances your Node.js cloud apps to [compare two documents](https://products.groupdocs.cloud/comparison/nodejs), fetch, accept or reject the changes. Supports 90+ file formats.

## Cloud Document Comparison Features

- Compare two documents and fetch changes.
- [Fetch document changes](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-document-changes/) based on change category, such as, numeric only.
- Accept or reject the changes that come up after document comparison.
- [Get the image stream of resultant document](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-stream-of-images-of-result-document-changes/) via JsonRequest object.
- Save the resultant document to streams as set of images.
- Get the resultant document path.
- Add summary page to resultant document after comparison.
- Show deleted components in the resultant document.
- Detect style changes.
- Get or set password of the resultant document.

## Supported Document Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX, XLTM, XLTX, ODS, OTS, CSV, TSV
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POTM, POTX, ODP, OTP
**Microsoft Visio:** VDW, VDX, VSD, VSDML, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Microsoft Project:** MPP, MPT
**Microsoft OneNote:** ONE
**Email:** EML, EMLX, MSG, OST, PST
**Adobe Photoshop:** PSD
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**eBook:** EPUB, MOBI
**Image:** BMP, CGM, DCM, DJVU, DNG, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PNG, SVG, TIF, TIFF, WEBP
**Markup:** HTML, MHT, MHTML, XML
**Portable:** PDF, TEX, XPS
**Metafile:** EMF, WMF
**Other:** PCL, PS

## Platform Independence

GroupDocs.Comparison Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Installation

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

A package `groupdocs-comparison-cloud` is available at [npmjs.com](https://www.npmjs.com/package/groupdocs-comparison-cloud). You can install it with:

`npm install groupdocs-comparison-cloud`

## Getting Started

Please follow the [installation](https://www.npmjs.com/package/groupdocs-comparison-cloud#installation) procedure and then run the following JavaScript code:

```js
// load the module
var GroupDocs = require('groupdocs-comparison-cloud');

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct ComparisonApi
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
import { InfoApi } from "groupdocs-comparison-cloud";

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
const appSid: string = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
const appKey: string = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct ComparisonApi
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

## Compare Documents using Node.js

```js
public async comparisons(requestObj: model.ComparisonsRequest): Promise<model.Link> {
    if (requestObj === null || requestObj === undefined) {
        throw new Error('Required parameter "requestObj" was null or undefined when calling comparisons.');
    }

    const localVarPath = this.configuration.getServerUrl() + "/comparison/comparisons";
    const queryParameters: any = {};

    // verify required parameter 'requestObj.comparisonOptions' is not null or undefined
    if (requestObj.comparisonOptions === null || requestObj.comparisonOptions === undefined) {
        throw new Error('Required parameter "requestObj.comparisonOptions" was null or undefined when calling comparisons.');
    }

    const requestOptions: request.Options = {
        method: "POST",
        qs: queryParameters,
        uri: localVarPath,
        json: true,
        body: Serializer.serialize(requestObj.comparisonOptions, requestObj.comparisonOptions.constructor.name === "Object" ? "Options" : requestObj.comparisonOptions.constructor.name),
    };

    const response = await invokeApiMethod(requestOptions, this.configuration);
    const result =  Serializer.deserialize(response.body, "Link");
    return Promise.resolve(result);
}
```

## Licensing

GroupDocs.Comparison Cloud Node.js SDK licensed under [MIT License](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-node/blob/HEAD/LICENSE).

[Product Page](https://products.groupdocs.cloud/comparison/nodejs) | [Documentation](https://wiki.groupdocs.cloud/comparisoncloud/) | [API Reference](https://apireference.groupdocs.cloud/comparison/) | [Code Samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/comparison/) | [Free Support](https://forum.groupdocs.cloud/c/comparison) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
