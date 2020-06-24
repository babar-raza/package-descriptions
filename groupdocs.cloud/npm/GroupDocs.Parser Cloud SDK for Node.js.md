# Document Parser Node.js Cloud REST API

This [document parser & data extraction REST API](https://products.groupdocs.cloud/parser/nodejs) can be used to enhance your Node.js cloud-based applications to perform parsing operations.

## Cloud Document Parser Features

- Create easy to define templates with data field and table definitions.
- Parse documents with pre-defined templates.
- Extract data from invoices or from other sort of documents.
- Supports extracting text and images.
- Extract data from regular documents as well as from email or archive containers.
- Obtain data from PDF portfolios.
- Fetch text fields, numbers and tables from common documents.
- Save your templates in the storage and parse your documents with them.
- Ability to extract HTML or Markdown (MD) text for a quick preview.
- Fetch specific pages of plain as well as formatted text.
- Extract formatted (bold, italic, hyperlink etc.) text in the MD format.
- Support for extracting text in HTML formatting (paragraph, hyperlinks, lists etc.).
- Retrieve all images from a document and save them.
- Obtain basic information about documents, archives, emails, and attachments etc.
- Extract data from a document contained inside a ZIP archive, email or PDF portfolio.

## New Features & Enhancements in Version 20.6

- Added `Node.js`, `PHP`, `Python`, and `Ruby` SDK for GroupDocs.Parser Cloud.
- Implemented extraction of encoding.
- Implemented additional image information extraction.

For the detailed notes, pelase visit [GroupDocs.Parser for Cloud 20.6 Release Notes](https://wiki.groupdocs.cloud/parsercloud/release-notes/release-notes-2020/groupdocs-parser-for-cloud-20-6-release-notes).

## Parse Document By Template Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF

## Extract Text Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Emails:** EML, EMLX, MSG
**Notes:** ONE

## Extract Document Info Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Emails:** PST, OST, EML, EMLX, MSG
**Notes:** ONE
**Archives:** ZIP

## Extract Images Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Emails:** EML, EMLX, MSG
**Archives:** ZIP

## Extract Container Items Info Supported Formats

**Portable:** PDF
**Emails:** PST, OST, EML, EMLX, MSG
**Archives:** ZIP

## Getting Started

You do not need to install anything to get started with GroupDocs.Parser Cloud SDK for Node.js. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Please check the [GitHub Repository](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-node-samples) for other common usage scenarios.

## Installation

A package `groupdocs-parser-cloud` is available at [npmjs.com](https://www.npmjs.com/package/groupdocs-parser-cloud). You can install it with:

```shell
npm install groupdocs-parser-cloud
```

Please follow the installation procedure and then run the following JavaScript code:

```js
// load the module
var GroupDocs = require('groupdocs-parser-cloud');

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct InfoApi
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

```ts
// load the module
import { InfoApi } from "groupdocs-parser-cloud";

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
const appSid: string = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
const appKey: string = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct InfoApi
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

## Prerequisites

- Node.js with `NPM` installed
- Get your `AppSID` and `AppKey` at [https://dashboard.groupdocs.cloud](https://dashboard.groupdocs.cloud) (free registration is required).

## How to Run the Examples

Follow the given steps to proceed run:

- Extract the downloaded project.
- Edit `RunExamples.js` and put `appSid` and `appKey`, obtained from [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud).
- Go to "Examples" directory of the project.
- Execute `npm install` command.
- Execute `npm update` command.
- Run examples using `npm run-script start` command.

For more details, visit [Getting Started](https://docs.groupdocs.cloud/display/parsercloud/Getting+Started).

[Product Page](https://products.groupdocs.cloud/parser/nodejs) | [Documentation](https://wiki.groupdocs.cloud/parsercloud/) | [Demo](https://products.groupdocs.app/parser/family) | [API Reference](https://apireference.groupdocs.cloud/parser/) | [Examples](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-node-samples) | [Blog](https://blog.groupdocs.cloud/category/parser/) | [Free Support](https://forum.groupdocs.cloud/c/parser) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
