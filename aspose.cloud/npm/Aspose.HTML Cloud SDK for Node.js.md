This cloud SDK assists to develop cloud-based HTML page rendering, processing, translation & conversion apps in Node.js language via REST API.

Aspose.HTML Cloud SDK for Node.js lets you access your desired HTML document from the cloud storage, or fetch the HTML page with all its linked resources as a ZIP archive via page URL.

## HTML Processing Features

- Fetch HTML page along with its resources as a ZIP archive by providing page URL.
- Based on page URL, retrieve all images of an HTML page as a ZIP package.
- Load data from local file to populate HTML document template.
- Use request body to populate HTML document template.
- Convert HTML page to numerous other file formats.

## Read & Write HTML Formats

HTML, XHTML, zipped HTML, zipped XHTML, MHTML, HTML containing SVG markup, Markdown, JSON

## Save HTML As

**Fixed Layout:** PDF, XPS
**Images:** TIFF, JPEG, PNG, BMP, GIF
**Other:** TXT, ZIP (images)

## Read HTML Formats
**eBook:** EPUB
**Other:** XML, SVG

## Platform Independence

Aspose.HTML Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.HTML Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-html-cloud/aspose-html-cloud-nodejs). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.HTML for Cloud via NPM, please execute from the command line, `npm install aspose-html-cloud-node --save`.

## Fetch HTML Page via URL & Convert to Image using Node.js

```js
this.GetConvertDocumentToImageByUrl = function (sourceUrl, outFormat, opts, callback) {
            opts = opts || {};
            var postBody = null;
            // verify the required parameter 'sourceUrl' is set
            if (sourceUrl === undefined || sourceUrl === null) {
                throw new Error("Missing the required parameter 'sourceUrl' when calling GetConvertDocumentToImageByUrl");
            }
            // verify the required parameter 'outFormat' is set
            if (outFormat === undefined || outFormat === null) {
                throw new Error("Missing the required parameter 'outFormat' when calling GetConvertDocumentToImageByUrl");
            }
            var pathParams = {
                'outFormat': outFormat
            };
            var queryParams = {
                'sourceUrl': sourceUrl,
                'width': opts['width'],
                'height': opts['height'],
                'leftMargin': opts['leftMargin'],
                'rightMargin': opts['rightMargin'],
                'topMargin': opts['topMargin'],
                'bottomMargin': opts['bottomMargin'],
                'resolution': opts['resolution'],
                'folder': opts['folder'],
                'storage': opts['storage'],
            };
            var headerParams = {};
            var formParams = {};
            var contentTypes = ['application/json'];
            var accepts = ['multipart/form-data'];
            var returnType = 'Blob';

            return this.apiClient.callApi(
                '/html/convert/image/{outFormat}', 'GET',
                pathParams, queryParams, headerParams, formParams, postBody,
                contentTypes, accepts, returnType, callback
            );
        };
```

[Product Page](https://products.aspose.cloud/html/nodejs) | [Documentation](https://docs.aspose.cloud/display/htmlcloud/Home) | [API Reference](https://apireference.aspose.cloud/html/) | [Code Samples](https://github.com/aspose-html-cloud/aspose-html-cloud-nodejs) | [Blog](https://blog.aspose.cloud/category/html/) | [Free Support](https://forum.aspose.cloud/c/html) | [Free Trial](https://dashboard.aspose.cloud/#/apps)