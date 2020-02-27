This REST API enables your Node.js apps to [perform document merging & joining](https://products.groupdocs.cloud/merger/nodejs) for 40+ file formats, while page manipulation for 35+ formats.

## Cloud Document Merger Features

- [Merge two of more documents](https://wiki.groupdocs.cloud/mergercloud/developer-guide/document-operations/join-multiple-documents/) into a single file.
- Merge specific pages from several different documents into a single file.
- Join page ranges from various documents into a single resultant file.
- [Split a source document](https://wiki.groupdocs.cloud/mergercloud/developer-guide/document-operations/split-document/) into many different files.
- Generate image representation of document pages as preview.
- Create document image preview of all pages, specific pages, or a page range.
- [Move, remove, rotate, swap, and extract](https://wiki.groupdocs.cloud/mergercloud/developer-guide/pages-operations/) document pages.
- Change portrait or landscape orientation of the document pages.
- Set, update or remove document password.
- Extract basic information about the document.

## Merge & Split File Formats

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

The following file formats are supported for trimming, moving, swapping pages or changing page orientation:
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

## Platform Independence

GroupDocs.Merger Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Installation

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information. The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

A package `groupdocs-merger-cloud` is available at [npmjs.com](https://www.npmjs.com/package/groupdocs-merger-cloud). You can install it with:

 `npm install groupdocs-merger-cloud`

## Getting Started

Please follow the [installation](https://www.npmjs.com/package/groupdocs-merger-cloud#installation) procedure and then run the following JavaScript code:

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

## Merge Multiple Documents using Node.js

```js
Configuration configuration = new Configuration(MyAppSid, MyAppKey);
DocumentApi apiInstance = new DocumentApi(configuration);

FileInfo fileInfo1 = new FileInfo();
fileInfo1.setFilePath("foldername/doc1.docx");
JoinItem item1 = new JoinItem();
item1.setFileInfo(fileInfo1);

FileInfo fileInfo2 = new FileInfo();
fileInfo2.setFilePath("foldername/doc2.docx");
JoinItem item2 = new JoinItem();
item2.setFileInfo(fileInfo2);

JoinOptions options = new JoinOptions();
options.setJoinItems(Arrays.asList(item1, item2));
options.setOutputPath("output/mergedDoc.docx");

JoinRequest request = new JoinRequest(options);
DocumentResult response = apiInstance.join(request);
```

## Licensing

GroupDocs.Merger Cloud Node.js SDK licensed under [MIT License](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-node/blob/HEAD/LICENSE).

[Product Page](https://products.groupdocs.cloud/merger/nodejs) | [Documentation](https://wiki.groupdocs.cloud/mergercloud/) | [API Reference](https://apireference.groupdocs.cloud/merger/) | [Code Samples](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/merger/) | [Free Support](https://forum.groupdocs.cloud/c/merger) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
