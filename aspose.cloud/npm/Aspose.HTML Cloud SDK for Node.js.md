Node.js Cloud SDK wraps Aspose.HTML REST API so you could seamlessly integrate markup-based file creation, manipulation & conversion features into your own Node.js applications.

# Process HTML, SVG, MD & EPUB Files in the Cloud

[Aspose.HTML Cloud SDK for Node.js](https://products.aspose.cloud/html/nodejs) offers its consumers to load markup of HTML, MHTML, XHTML, EPUB, XML & SVG formats from file, cloud storage or URL. The loaded document can be traversed or inspected via CSS selector & XPath query or can be converted to images, PDF, XPS as well as other supported markup formats. The HTML REST API also allows to extract images from the HTML and populate HTML template with data from JSON or XML. Checkout the [API Reference]([https://apireference.aspose.cloud/html/](https://apireference.aspose.cloud/html/)) & [Developer's Guide]([https://docs.aspose.cloud/display/htmlcloud/Developer+Guide](https://docs.aspose.cloud/display/htmlcloud/Developer+Guide)) for all possible functions.

## HTML Processing Features

- Fetch HTML page along with its resources as a ZIP archive by providing page URL.
- Retrieve only the images on an HTML page as a ZIP package.
- Load data from local file to populate HTML document template.
- Use request body to populate HTML document template.
- Convert HTML page to numerous other file formats.
- Validate HTML for SEO & structure errors.

## New Features in Version 19.11.0

- Added following SEO analysis points in the current version:
  - detection of broken links.
  - validation of e-mail addresses.
  - checking of `IMG` tags for the absence of `ALT` attribute.
  - checking for duplicated `H1` elements.

For the detailed notes, please visit [Aspose.HTML Cloud 19.11 Release Notes](https://docs.aspose.cloud/display/htmlcloud/Aspose.HTML+Cloud+19.11+Release+Notes).

## Read & Write Formats

HTML, XHTML, zipped HTML, zipped XHTML, MHTML, Markdown, JSON

## Save HTML As

**Fixed Layout:** PDF, XPS
**Images:** TIFF, JPEG, PNG, BMP, GIF
**Other:** TXT, ZIP (images)

## Read HTML Formats

**eBook:** EPUB
**Other:** XML, SVG

## Getting Started with Aspose.HTML Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install @asposecloud/aspose-email-cloud --save` from the command line to install Aspose.HTML Cloud SDK for Node.js via NPM.

The complete source code is available at [GitHub Repository](https://github.com/aspose-html-cloud/aspose-html-cloud-nodejs).

## Fetch & Convert HTML to Image using Node.js

```js
this.GetConvertDocumentToImageByUrl = function (sourceUrl, outFormat, opts, callback) 
{
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
