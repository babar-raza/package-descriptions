Node.js Cloud SDK wraps Aspose.Words REST API so you could seamlessly integrate Microsoft Word® document generation, manipulation, conversion & inspection features into your own Node.js applications.

# Word Document Processing in the Cloud

[Aspose.Words Cloud SDK for Node.js](https://products.aspose.cloud/slides/nodejs) allows to work with document headers, footers, page numbering, tables, sections, document comments, drawing objects, FormFields, fonts, hyperlinks, ranges, paragraphs, math objects, watermarks, track changes and document protection. It also assists in appending documents, splitting documents as well as converting document to other supported file formats. 

Feel free to explore the [Developer's Guide](https://docs.aspose.cloud/display/wordscloud/Developer+Guide) & [API Reference](https://apireference.aspose.cloud/words/) to know all about Aspose.Words Cloud API. 

## Document Processing Features

- Convert between various document-related formats, including Word to PDF & vice versa.
- Mail merge and report generation in the Cloud.
- Split & merge Word documents.
- Access Word document metadata.
- Find and replace text.
- Add & remove watermarks and protection.
- Read & write access to Document Object Model.

## New Features & Enhancements in Version 20.6

### Words Cloud changes

- Added new `OoxmlSaveOption` CompressionLevel.
- Added group of methods without nodePath property:
  - `DeleteAllParagraphTabStops`
  - `DeleteParagraphListFormat`
  - `DeleteParagraphTabStop`
  - `GetParagraphTabStops`
  - `InsertOrUpdateParagraphTabStop`
  - `InsertParagraph`
  - `UpdateParagraphFormat`
  - `UpdateParagraphListFormat`

### PDF to Word conversion improvements

- Implemented clipping path detection for `W` and `W*` operators.
- Added support for `PDF` files with early `EOFs`.
- Slightly improved speed of `PDF` recognition workflow.
- Corrected space detection between links on the same row.
- Fixed a rare concurrency error in font loading code.

For the detiled notes, please visit [Aspose.Words Cloud 20.6 Release Notes](https://docs.aspose.cloud/display/wordscloud/Aspose.Words+Cloud+20.6+Release+Notes).

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

## Getting Started with Aspose.Words Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install asposewordscloud --save` from the command line to install Aspose.Words Cloud SDK for Node.js via NPM.

The complete source code is available at [GitHub Repository](https://github.com/aspose-words-cloud/aspose-words-cloud-node).

### SDK Dependencies

- [@types/request](https://www.npmjs.com/package/@types/request) (version 2.48.3+)
- [lodash](https://www.npmjs.com/package/lodash) (version 4.17.15+)
- [lodash.template](https://www.npmjs.com/package/lodash.template) (version 4.5.0+)
- [request](https://www.npmjs.com/package/request) (version 2.88.0+)
- [request-debug](https://www.npmjs.com/package/request-debug) (version 0.2.0+)

## Convert DOC to PDF via Node.js

```js
const { WordsApi, PostDocumentSaveAsRequest, SaveOptionsData } = require("asposewordscloud");
 
wordsApi = new WordsApi(AppSid, AppKey);
 
var request = new PostDocumentSaveAsRequest({
    name: "fileStoredInCloud.doc",
    saveOptionsData: new SaveOptionsData(
        {
            saveFormat: "pdf",
            fileName: "destination.pdf"
        })
});
 
wordsApi.postDocumentSaveAs(request)
    .then((result) => {
        // Deal with a result
        console.log(result.response.statusCode);
        console.log(result.body);
    })
    .catch(function(err) {
        console.log(err.reponse.statusCode);
        console.log(err.body);
    });
```

[Product Page](https://products.aspose.cloud/words/nodejs) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [Demo](https://products.aspose.app/words/family) | [API Reference](https://apireference.aspose.cloud/words/) | [Examples](https://github.com/aspose-words-cloud/aspose-words-cloud-node) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
