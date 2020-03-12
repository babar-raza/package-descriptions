Node.js Cloud SDK wraps GroupDocs.Comparison Cloud API so you could seamlessly integrate Document Comparison features into your own Node.js apps.

# Document Comparison in the Cloud

[GroupDocs.Comparison Cloud SDK for Node.js](https://products.groupdocs.cloud/comparison/nodejs) helps developers implement document comparison for over 90 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe, CAD, markup & image file formats, and compare 2 similar documents to retrieve differences as a file or array of images. 

Check out the [API Reference](https://apireference.groupdocs.cloud/comparison/) to know all about the GroupDocs.Comparison REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

# Addon Features

- Load password protected documents.
- [Fetch document changes](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-document-changes/) based on category, such as, change in numeric values only.
- Accept or reject retrieved changes.
- [Get the image stream of resultant document](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-stream-of-images-of-result-document-changes/).
- Detect changes in text style.
- Add summary page to resultant document after comparison.
- Show deleted components in the resultant document.

## Compare Document Formats

GroupDocs.Comparison Cloud API [supports 90+ file formats](https://wiki.groupdocs.cloud/comparisoncloud/getting-started/supported-document-formats/) that it can load & compare.

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

## Getting Started with GroupDocs.Comparison Cloud SDK for Node.js

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-Comparison-cloud/groupdocs-Comparison-cloud-node). You can either directly use it in your project via source code or get NPM distribution via `npm install groupdocs-comparison-cloud`.

Execute following snippet to load supported formats.

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

Or compile and run the same written in TypeScript:

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

## Compare Documents in the Cloud using Node.js 

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
