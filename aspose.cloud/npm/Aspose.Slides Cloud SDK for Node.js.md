Node.js Cloud SDK wraps Aspose.Slides REST API so you could seamlessly integrate PowerPoint® presentation generation, manipulation, conversion & inspection features into your own Node.js applications.

# PowerPoint File Processing in the Cloud

[Aspose.Slides Cloud SDK for Node.js](https://products.aspose.cloud/slides/nodejs) enhance your Node.js programs to create presentations in the cloud, pick and merge specific slides, split presentations, extract images from presentation in any of the supported file formats, extract & download slide notes, clone master slide information, and more. 

Feel free to explore the [Developer's Guide](https://docs.aspose.cloud/display/slidescloud/Developer+Guide) & [API Reference](https://apireference.aspose.cloud/slides/) to know all about Aspose.Slides Cloud API. 

## Presentation Processing Features

- Fetch presentation images in any of the supported file formats.
- Copy layout side or clone master slide from the source presentation.
- Process slides shapes, slides notes, placeholders, colors & font theme info.
- Create presentation from HTML & export to various popular formats.
- Merge multiple presentations or split single presentation into multiple ones.
- Extract and replace text from specific slide or entire presentation.
- Manage shapes, animation, text, images, theme, notes & more with REST Models.

## Enhancements  in Version 20.4

- Supports ViewProperties.
- Supports new Powerpoint 2016 Chart types.

## Public API Changes

- Added `viewproperties` resource. It allows to GET and set (PUT) view properties of a document (`LastView`, `HorizontalBarState`, `VerticalBarState` etc.)
- Added `Treemap`, `Sunburst`, `Histogram`, `ParetoLine`, `BoxAndWhisker`, `Waterfall`, and `Funnel` chart types.

For the detailed notes, please visit [Aspose.Slides Cloud 20.4 Release Notes](https://docs.aspose.cloud/display/slidescloud/Aspose.Slides+Cloud+20.4+Release+Notes).

## Read & Write Presentation Formats

**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX, PPTM, PPSM, POTX, POTM
**OpenOffice:** ODP, OTP

## Save Presentations As

**Fixed Layout:** PDF, PDF/A, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Web:** HTML
**Other:** SWF (export whole presentations)

## Getting Started with Aspose.Slides Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install asposeslidescloud --save` from the command line to install Aspose.Slides Cloud SDK for Node.js via NPM.

The complete source code is available at [GitHub Repository](https://github.com/aspose-slides-cloud/aspose-slides-cloud-nodejs).

## Convert PowerPoint to PDF in the Cloud

```js
const api = require("asposeslidescloud");
const fs = require('fs');

const slidesApi = new api.SlidesApi("MyAppSid", "MyAppKey");
const postSlidesConvertRequest = new api.GetSlidesApiInfoRequest();
postSlidesConvertRequest.format = 'pdf';
postSlidesConvertRequest.document = fs.createReadStream("MyPresentation.pptx");
slidesApi.postSlidesConvert(postSlidesConvertRequest).then((response) => {
    fs.writeFile("MyPresentation.pdf", response.body, (err) => {
        if (err) throw err;
    });
});
```

## Fetch & Save Images from Presentation using Node.js

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

[Product Page](https://products.aspose.cloud/slides/nodejs) | [Documentation](https://docs.aspose.cloud/display/slidescloud/Home) | [Demo](https://products.aspose.app/slides/family) | [API Reference](https://apireference.aspose.cloud/slides/) | [Examples](https://github.com/aspose-slides-cloud/aspose-slides-cloud-nodejs) | [Blog](https://blog.aspose.cloud/category/slides/) | [Free Support](https://forum.aspose.cloud/c/slides) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
