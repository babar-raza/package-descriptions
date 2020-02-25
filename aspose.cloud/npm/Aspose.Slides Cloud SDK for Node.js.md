This REST API enables your Node.js cloud-based apps to process & manipulate PPT, PPTX, ODP, OTP presentations in the cloud.

Aspose.Slides Cloud SDK for Node.js is a wrapper around Aspose.Slides REST API and is offered under an MIT license. Enhance your Node.js programs to create presentations in the cloud, pick and merge specific slides, split presentations, extract images from presentation in any of the supported file formats, extract & download slide notes, clone master slide information, and so much more.

## Presentation Processing Features

- Fetch presentation images in any of the supported file formats.
- Copy layout side or clone master slide from the source presentation.
- Process slides shapes, slides notes, placeholders, colors & font theme info.
- Programmatically create presentation from HTML & export it to various formats.
- Merge multiple presentations or split single presentation into multiple ones.
- Extract and replace text from specific slide or entire presentation.

## Read & Write Presentation Formats

**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX, PPTM, PPSM, POTX, POTM
**OpenOffice:** ODP, OTP

## Save Presentation As

**Fixed Layout:** PDF, PDF/A, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Web:** HTML
**Other:** SWF (export whole presentations)

## Platform Independence

Aspose.Slides Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.Slides Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-slides-cloud/aspose-slides-cloud-nodejs). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.Slides for Cloud via NPM, please execute from the command line, `npm install aspose-slides-cloud-node --save`.

## Fetch PPTX Presentation Slides to Image Format using Node.js

```js
const sdkApi = require("asposeslidescloud/api");
const requests = require("asposeslidescloud/requests");
const models = require("asposeslidescloud/model");
const api = new sdkApi.ImagesApi("", "");



const request = new requests.GetSlidesImageWithFormatRequest();
request.name = "test.pptx"
request.index = "1"
request.format = "Jpeg";


api.getSlidesImageWithFormat(request).then((result) => {
    console.log(result.response);
});
```

[Product Page](https://products.aspose.cloud/slides/nodejs) | [Documentation](https://docs.aspose.cloud/display/slidescloud/Home) | [API Reference](https://apireference.aspose.cloud/slides/) | [Code Samples](https://github.com/aspose-slides-cloud/aspose-slides-cloud-nodejs) | [Blog](https://blog.aspose.cloud/category/slides/) | [Free Support](https://forum.aspose.cloud/c/slides) | [Free Trial](https://dashboard.aspose.cloud/#/apps)