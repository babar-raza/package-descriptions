This Cloud SDK allows you to easily build cloud-based PDF creator, editor & converter apps in Node.js language for various cloud platforms.

Aspose.PDF Cloud SDK for Node.js is available to you under an MIT license and is a wrapper around Aspose.PDF REST API. Access images embedded in the PDF documents for customization, work with; annotations, stamps, PDF form fields, watermarks, as well as the OCR layers within the PDF files.

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

## Read & Write PDF Formats

PDF, EPUB, HTML, TeX, SVG, XML, XPS, FDF, XFDF

## Save PDF As

XLS, XLSX, PPTX, DOC, DOCX, MobiXML, JPEG, EMF, PNG, BMP, GIF, TIFF, Text

## Read PDF Formats

MHT, PCL, PS, XSLFO, MD

## Platform Independence

Aspose.PDF Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.PDF Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-node.js). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.PDF for Cloud via NPM, please execute from the command line, `npm install aspose-pdf-cloud-node --save`.

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