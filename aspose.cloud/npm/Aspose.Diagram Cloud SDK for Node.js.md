This cloud SDK enables your Node.js cloud apps to create & process Visio diagrams from within your apps without installing Microsoft Visio.

Aspose.Diagram Cloud SDK for Node.js is built on top of Aspose.Diagram REST API and is distributed for use under an MIT license.

## Visio Processing Features

- Retrieve document information of a Visio diagram.
- Programmatically create a new Microsoft Visio diagram file.
- Convert Visio flow-charts to other supported formats.
- Upload your business oriented Visio diagrams to cloud storage.
- Export Visio files to raster images, fixed-layout and HTML formats.

## Read & Write Visio Formats

**Microsoft Visio:** VSDX, VSX, VTX, VDX, VSSX, VSTX, VSDM, VSSM, VSTM

## Save Visio As

**Fixed Layout:** PDF, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG, EMF
**Web:** HTML
**Other:** XAML, SWF

## Read Visio Formats

**Microsoft Visio:** VDW, VSD, VSS, VST

## Platform Independence

Aspose.Diagram Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.Diagram Cloud SDK for Node.js. All you need to do is create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.Diagram for Cloud via NPM, please execute from the command line, `npm install aspose-diagram-cloud-node --save`.

## Create a Diagram File in Cloud via Node.js

```js
const { DiagramFileApi, DiagramFile_PutCreateRequest } = require("asposediagramcloud");

var AppSid = ""
var AppKey = ""

diagramFileApi = new DiagramFileApi(AppSid, AppKey);

var req = new DiagramFile_PutCreateRequest();
req.name = "file_create_node.vdx";
req.isOverwrite = true;

diagramFileApi.diagramFilePutCreate(req).then((result) => {
    console.log('API Response:', result);
}).catch(function(err) {
    // Deal with an error
    console.log('Error:', err);
});
```

[Product Page](https://products.aspose.cloud/diagram/nodejs) | [Documentation](https://docs.aspose.cloud/display/diagramcloud/Home) | [API Reference](https://apireference.aspose.cloud/diagram/) | [Code Samples](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-node) | [Blog](https://blog.aspose.cloud/category/diagram/) | [Free Support](https://forum.aspose.cloud/c/diagram) | [Free Trial](https://dashboard.aspose.cloud/#/apps)