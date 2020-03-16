Node.js Cloud SDK wraps GroupDocs.Merger Cloud API so you could seamlessly integrate Document Joining features into your own Node.js apps.

# Document Merging in the Cloud

[GroupDocs.Merger Cloud SDK for Node.js](https://products.groupdocs.cloud/merger/nodejs) helps developers implement document merging for over 35 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe & markup file formats, and merge documents.

Check out the [API Reference](https://apireference.groupdocs.cloud/merger/) to know all about the GroupDocs.Merger REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## Utility Features

- Load password protected documents.
- [Integrated storage API](https://wiki.groupdocs.cloud/editorcloud/developer-guide/storage-operations/) for unified access to files & folders.
- Extract basic information about the document.
- Set, update or remove document password.
- Change portrait or landscape orientation of the document pages.
- [Merge two of more documents](https://wiki.groupdocs.cloud/mergercloud/developer-guide/document-operations/join-multiple-documents/) into a single file.
- Merge specific pages from several different documents into a single file.
- Join page ranges from various documents into a single resultant file.
- [Split a source document](https://wiki.groupdocs.cloud/mergercloud/developer-guide/document-operations/split-document/) into many different files.
- Generate image representation of document pages as preview.
- Create document image preview of all pages, specific pages, or a page range.
- [Move, remove, rotate, swap, and extract](https://wiki.groupdocs.cloud/mergercloud/developer-guide/pages-operations/) document pages.

## Merge & Split File Formats

GroupDocs.Merger Cloud API [supports 35+ file formats](https://wiki.groupdocs.cloud/mergercloud/getting-started/supported-document-formats/) that it can load & perform merge or split operations.

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX
**Microsoft Visio:** VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
**Microsoft OneNote:** ONE
**OpenOffice:** ODT, OTT, ODP, OTP, ODS
**Markup:** HTML, MHT
**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB, CSV, TSV, TXT

## Page Manipulation File Formats

The following file formats are supported for trimming, moving, swapping pages or changing page orientation.

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX
**Microsoft Visio:** VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
**Microsoft OneNote:** ONE
**OpenOffice:** ODT, OTT, ODP, OTP, ODS
**Markup:** HTML, MHT
**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB

## Page Rotation File Formats

**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB

## Getting Started with GroupDocs.Merger Cloud SDK for Node.js

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-node). You can either directly use it in your project via source code or get NPM distribution via `npm install groupdocs-merger-cloud`.

Execute following snippet to load supported formats.

```js
// load the module
var GroupDocs = require('groupdocs-merger-cloud');

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct MergerApi
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
import { InfoApi } from "groupdocs-merger-cloud";

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
const appSid: string = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
const appKey: string = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct MergerApi
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

## Merge Multiple Documents in the Cloud using Node.js

```js
global.appSid = "XXXX-XXXX-XXXX-XXXX"; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
global.appKey = "XXXXXXXXXXXXXXXX"; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
global.documentApi = merger_cloud.DocumentApi.fromKeys(appSid, appKey);

let item1 = new merger_cloud.JoinItem();
item1.fileInfo = new merger_cloud.FileInfo();
item1.fileInfo.filePath = "WordProcessing/four-pages.docx";

let item2 = new merger_cloud.JoinItem();
item2.fileInfo = new merger_cloud.FileInfo();
item2.fileInfo.filePath = "WordProcessing/one-page.docx";

let options = new merger_cloud.JoinOptions();
options.joinItems = [item1, item2];
options.outputPath = "Output/joined.docx";

let result = await documentApi.join(new merger_cloud.JoinRequest(options));
```

## Licensing

GroupDocs.Merger Cloud Node.js SDK licensed under [MIT License](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-node/blob/HEAD/LICENSE).

[Product Page](https://products.groupdocs.cloud/merger/nodejs) | [Documentation](https://wiki.groupdocs.cloud/mergercloud/) | [API Reference](https://apireference.groupdocs.cloud/merger/) | [Code Samples](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/merger/) | [Free Support](https://forum.groupdocs.cloud/c/merger) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
