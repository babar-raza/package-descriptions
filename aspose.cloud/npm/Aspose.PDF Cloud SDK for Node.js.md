Node.js Cloud SDK wraps Aspose.PDF REST API so you could seamlessly integrate PDF document generation, manipulation, conversion & inspection features into your own Node.js applications.

# PDF Document Processing in the Cloud

[Aspose.PDF Cloud SDK for Node.js](https://products.aspose.cloud/pdf/nodejs) enhances your Node.js code to generate new PDF documents & pages, delete pages from existing PDF files as well as manage PDF bookmarks, annotations, signatures, stamps, watermarks, attachments, header, footer, hyperlinks, form fields, text items and images via simple Node.js REST API calls. Please feel free to explore the [Developer's Guide](https://docs.aspose.cloud/display/pdfcloud/Developer+Guide) for all possible usage scenarios. 

## PDF Processing Features

- Add PDF document's header & footer in text or image format.
- Add tables & stamps (text or image) to PDF documents.
- Append multiple PDF documents to an existing file.
- Work with PDF attachments, annotations, & form fields.
- Apply encryption or decryption to PDF documents & set password.
- Delete all stamps & tables from a page or entire PDF document.
- Delete a specific stamp or table from the PDF document by its ID.
- Replace a single or multiple instances of a text on a PDF page or from entire document.
- Extensive support for converting PDF documents to various other file formats.
- Extract various elements of PDF file & make PDF document optimized.

## New features in Version 20.2.0

- Implemented a method to convert `PDFA` to `PDF` and upload the resulting file to storage.
- Implemented a method to convert `PDFA` to `PDF` and return resulting file in response.

For the detailed notes, please visit [Aspose.PDF Cloud 20.2 Release Notes](https://docs.aspose.cloud/display/pdfcloud/Aspose.PDF+Cloud+20.2+Release+Notes).

## Read & Write Formats

PDF, EPUB, HTML, TeX, SVG, XML, XPS, FDF, XFDF

## Save PDF As

XLS, XLSX, PPTX, DOC, DOCX, MobiXML, JPEG, EMF, PNG, BMP, GIF, TIFF, Text

## Read Formats

MHT, PCL, PS, XSLFO, MD

## Getting Started with Aspose.PDF Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install aspose-pdf-cloud-node --save` from the command line to install Aspose.PDF Cloud SDK for Node.js via NPM.

The complete source code is available at [GitHub Repository](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-node.js).

## Get Page Annotation from PDF via Node.js

```js
const { PdfApi } = require("asposepdfcloud");
 
let pdfApi = new PdfApi(AppSid, AppKey);
 
let pageNumber = 1;
let pdfDocName = "example.pdf";
let remoteFolder = "folderName"; 
 
pdfApi.getPageAnnotations(pdfDocName, pageNumber, null, remoteFolder)
.then((result) => {
console.log(result.response);
console.log(result.body);
});
```

## Use Node.js to Split a PDF Document via REST API

```js
const { PdfApi } = require("asposepdfcloud");

pdfApi = new PdfApi("XXXX", "XXXXXXX")

console.log('running example');
pdfApi.postSplitDocument("4pages.pdf", null, null, null, null, null)
    .then((result) => {
        console.log(result.response);
    });
```

[Product Page](https://products.aspose.cloud/pdf/nodejs) | [Documentation](https://docs.aspose.cloud/display/pdfcloud/Home) | [API Reference](https://apireference.aspose.cloud/pdf/) | [Code Samples](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-node.js) | [Blog](https://blog.aspose.cloud/category/pdf/) | [Free Support](https://forum.aspose.cloud/c/pdf) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
