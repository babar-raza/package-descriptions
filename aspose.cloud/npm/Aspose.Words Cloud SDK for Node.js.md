This cloud SDK provides seamless integration of cloud document processing & manipulation features into your cloud-based Node.js apps.

Aspose.Words Cloud SDK for Node.js is built on top of Aspose.Words REST API and is provided to you under an MIT license. Using Aspose.Words Cloud SDK for Node.js, you can work with document comparison, headers, footers, page numbering, tables, sections, document comments, drawing objects, FormFields, fonts, hyperlinks, ranges, paragraphs, math objects, watermarks, track changes and document protection. Aspose.Words Cloud SDK for Node.js also assists you in appending documents, splitting documents as well as converting document into other supported file formats.

## Document Processing Features

- Programmatically create new documents of various file formats.
- Fetch a web page via its URL and save it in Microsoft Word file format.
- Get document information, by default, in JSON/XML representation.
- Fetch statistical data of a document.
- Render complex elements (table, DrawingObject etc.) of the document in supported formats.
- Remove all macros contained in a specific document.
- Convert a document to desired file format along with detailed settings.
- Convert an encrypted PDF document into MS Word document format.
- So many more features.

## Read & Write Document Formats

**Microsoft Word:** DOC, DOCX, RTF, DOT, DOTX, DOTM, FlatOPC (XML)
**OpenOffice:** ODT, OTT
**WordprocessingML:** XML
**Web:** HTML, MHTML, HtmlFixed
**Text:** TXT
**Fixed Layout:** PDF

## Save Document As

**Fixed Layout:** PDF/A, XPS, OpenXPS, PS
**Images:** JPEG, PNG, BMP, SVG, TIFF, EMF
**Others:** PCL

## Platform Independence

Aspose.Words Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.Words Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-words-cloud/aspose-words-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.Words for Cloud via NPM, please execute from the command line, `npm install aspose-words-cloud-node --save`.

## Use Node.js REST API to Convert Word Documents

```js
const {WordsApi, PutConvertDocumentRequest } = require("asposewordscloud");

var AppSid = "" // Get App Key and App SID from https://dashboard.aspose.cloud/
var AppKey = "" // Get App Key and App SID from https://dashboard.aspose.cloud/
var BaseUrl = "https://api.aspose.cloud"
var debugMode = false
var version = "v1.1"

wordsApi = new WordsApi(AppSid, AppKey, BaseUrl, debugMode, version);

var fs = require('fs');
var StorageApi = require("asposestoragecloud")
var config = {'appSid':AppSid, 'apiKey':AppKey};
var storageApi = new StorageApi(config);

var fileName = "test_multi_pages.docx";
var dataPath = '../../TestData/Common/';

var request = new PutConvertDocumentRequest({
                    format: "pdf",
                    document: fs.readFileSync(dataPath + fileName),
                });

wordsApi.putConvertDocument(request).then((result) => {
	console.log('API Response:', result.body.byteLength);
}).catch(function(err) {
    // Deal with an error
    console.log('Error:', err);
});
```

[Product Page](https://products.aspose.cloud/words/nodejs) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [API Reference](https://apireference.aspose.cloud/words/) | [Code Samples](https://github.com/aspose-words-cloud/aspose-words-cloud-node) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)