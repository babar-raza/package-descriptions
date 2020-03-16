Node.js Cloud SDK wraps GroupDocs.Editor Cloud API so you could seamlessly integrate Document Editing features into your own Node.js apps.

# Document Editing in the Cloud

[GroupDocs.Comparison Cloud SDK for Node.js](https://products.groupdocs.cloud/editor/nodejs) helps developers implement document comparison for over 40 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice & markup file formats, and edit documents using front-end WYSIWYG editor. 

Check out the [API Reference](https://apireference.groupdocs.cloud/editor/) to know all about the GroupDocs.Editor REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## Addon Features

- Load password protected documents.
- [Integrated storage API](https://wiki.groupdocs.cloud/editorcloud/developer-guide/storage-operations/) for unified access to files & folders.
- Extract basic information about the document.
- Support for highlighting and formatting options.

## Document Specific REST Models

- [Edit word processing documents](https://wiki.groupdocs.cloud/editorcloud/developer-guide/document-edit-operations/working-with-wordprocessing-documents/) in flow or paged mode.
- Extract font information for a consistent look and feel of the edited documents.
- Editing multi-tabbed spreadsheets with the ability to specify the index of the worksheet.
- [Edit DSV files](https://wiki.groupdocs.cloud/editorcloud/developer-guide/document-edit-operations/working-with-dsv-documents/).
- Specify the separator for the CSV and TSV files with flexible conversion options for dates and numbers.
- Optimize memory usage for large files.
- Fix incorrect document structure of the XML files.
- Recognize email addresses and URIs in the XML files.
- Enable pagination and protection while saving Word documents.

## Supported File Formats for Editing

GroupDocs.Editor Cloud API [supports 40+ file formats](https://wiki.groupdocs.cloud/editorcloud/getting-started/supported-document-formats/) that it can load & edit.

**Word Processing:** DOC, DOCX, DOCM, DOT, DOTM, DOTX, FlatOPC, ODT, OTT, RTF, WordML
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLTX, XLTM, XLSB, XLAM, SXC, SpreadsheetML, ODS, FODS, DIF, DSV, CSV, TSV
**Presentation:** PPT (95), PPT (97-2003), PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, POTM, ODP, OTP
**Markup:** HTML, XML
**Other:** TXT

## Getting Started with GroupDocs.Editor Cloud SDK for Node.js

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-node). You can either directly use it in your project via source code or get NPM distribution via `npm install groupdocs-editor-cloud`.

Execute following snippet to load supported formats.

```js
// load the module
var GroupDocs = require('groupdocs-editor-cloud');

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct EditorApi
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
import { InfoApi } from "groupdocs-editor-cloud";

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
const appSid: string = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
const appKey: string = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct EditorApi
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

## Edit Spreadsheets in the Cloud using Node.js

```js
global.editor_cloud = require("groupdocs-editor-cloud");

global.appSid = "XXXX-XXXX-XXXX-XXXX"; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
global.appKey = "XXXXXXXXXXXXXXXX"; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
global.editApi = editor_cloud.EditApi.fromKeys(appSid, appKey);
global.fileApi = editor_cloud.FileApi.fromKeys(appSid, appKey);
// The document already uploaded into the storage.
// Load it into editable state      
let fileInfo = new editor_cloud.FileInfo();
fileInfo.filePath = "Spreadsheet/four-sheets.xlsx";
let loadOptions = new editor_cloud.SpreadsheetLoadOptions();
loadOptions.fileInfo = fileInfo;
loadOptions.outputPath = "output";
loadOptions.worksheetIndex = 0;
let loadResult = await editApi.load(new editor_cloud.LoadRequest(loadOptions));

// Download html document
let buf = await fileApi.downloadFile(new editor_cloud.DownloadFileRequest(loadResult.htmlPath));
let htmlString = buf.toString("utf-8");

// Edit something...
htmlString = htmlString.replace("This is sample sheet", "This is sample sheep");

// Upload html back to storage
await fileApi.uploadFile(new editor_cloud.UploadFileRequest(loadResult.htmlPath, new Buffer(htmlString, "utf-8")));

// Save html back to docx
let saveOptions = new editor_cloud.SpreadsheetSaveOptions();
saveOptions.fileInfo = fileInfo;
saveOptions.outputPath = "output/edited.xlsx";
saveOptions.htmlPath = loadResult.htmlPath;
saveOptions.resourcesPath = loadResult.resourcesPath;
let saveResult = await editApi.save(new editor_cloud.SaveRequest(saveOptions));

// Done.
console.log("Document edited: " + saveResult.path);
```

## Licensing

GroupDocs.Editor Cloud Node.js SDK licensed under [MIT License](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-node/blob/HEAD/LICENSE).

[Product Page](https://products.groupdocs.cloud/editor/nodejs) | [Documentation](https://wiki.groupdocs.cloud/editorcloud/) | [API Reference](https://apireference.groupdocs.cloud/editor/) | [Code Samples](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/editor/) | [Free Support](https://forum.groupdocs.cloud/c/editor) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
