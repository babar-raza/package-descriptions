# HTML Rendering & Conversion Swift Cloud REST API

This cloud SDK assists to develop cloud-based [HTML page rendering, processing, translation & conversion](https://products.aspose.cloud/html/swift) apps in Swift language via REST API.

## HTML Processing Features

- Fetch HTML page along with its resources as a ZIP archive by providing page URL.
- Based on page URL, retrieve all images of an HTML page as a ZIP package.
- Load data from local file to populate HTML document template.
- Use request body to populate HTML document template.
- Convert HTML page to numerous other file formats.

## New Features in Version 20.5

- Added `Configuration.AddDefaultHeader`. It provides ability to specify custom headers which will be added to each `HTTP` request beneath API calls.

For the detailed notes, please visit [Release Notes - 2020](https://docs.aspose.cloud/display/htmlcloud/Release+Notes+-+2020).

## Read & Write HTML Formats

HTML, XHTML, zipped HTML, zipped XHTML, MHTML, HTML containing SVG markup, Markdown, JSON

## Save HTML As

**Fixed Layout:** PDF, XPS
**Images:** TIFF, JPEG, PNG, BMP, GIF
**Other:** TXT, ZIP (images)

## Read HTML Formats

**eBook:** EPUB
**Other:** XML, SVG

## Requirements

- mac OS X 10.12.6
- XCode 9.2
- Swift 4.0 and later
- Alamofire 4.7.3 and later

## Prerequisites

To use Aspose HTML for Cloud SDK you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Getting Started

Firstly create configuration, then use `HtmlAPI` or `StorageAPI`.

### Example

```swift
ClientAPI.setConfig(
  basePath: "https://api.aspose.cloud/v3.0",
  authPath: "https://api.aspose.cloud/connect/token",
  apiKey: "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  appSID: "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
  debugging: true
)
```

## `oauth`

- Type: OAuth2
- Flow: application
- Authorization URL: "https://api.aspose.cloud/connect/token"
- Scopes: N/A

## Source Code

The complete source code is available at the [GitHub repository](https://github.com/aspose-html-cloud/aspose-html-cloud-swift).

## Tests

[Tests](https://github.com/aspose-html-cloud/aspose-html-cloud-swift/blob/master/Tests/AsposeHtmlTests) contain various examples of using the Aspose.HTML and Aspose.Storage SDK.

[Product Page](https://products.aspose.cloud/html/swift) | [Documentation](https://docs.aspose.cloud/display/htmlcloud/Home) | [Demo](https://products.aspose.app/html/family) | [API Reference](https://apireference.aspose.cloud/html/) | [Examples](https://github.com/aspose-html-cloud/aspose-html-cloud-swift) | [Blog](https://blog.aspose.cloud/category/html/) | [Free Support](https://forum.aspose.cloud/c/html) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
