Node.js Cloud SDK wraps Aspose.Diagram REST API so you could seamlessly integrate Microsoft Visio® file generation, manipulation, conversion & processing features into your own Node.js applications.

# Process Visio® Files in the Cloud with Node.js
[Aspose.Diagram Cloud SDK for Node.js](https://products.aspose.cloud/diagram/nodejs) helps you develop Visio file manipulation applications while using the REST API. Diagram Cloud SDK allows your applications to work with Microsoft Visio Object Model in order to create the diragrams from scratch, edit existing diagrams or convert diagrams to popular formats including PDF, HTML, images and other Visio formats.

## Visio File Processing Features
- Programmatically create a new Microsoft Visio diagram file.
- Convert Visio flow-charts to other supported formats.
- Retrieve document information of a Visio file.
- Export Visio files to raster images, fixed-layout and HTML formats.
- Upload your business oriented Visio diagrams to cloud storage.

please refer to [Developer's Guide](https://docs.aspose.cloud/display/diagramcloud/Developer+Guide) to see what else you can achieve.


## Read & Write Visio File Formats

**Microsoft Visio:** VSDX, VSX, VTX, VDX, VSSX, VSTX, VSDM, VSSM, VSTM

## Save Visio Diagrams As

**Fixed Layout:** PDF, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG, EMF
**Web:** HTML
**Other:** XAML, SWF

## Read Visio Formats

**Microsoft Visio:** VDW, VSD, VSS, VST

## Platform Independence

Aspose.Diagram Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for diagram documents. 

## Integrated Storage API
Since version 19.10, SDK includes support of storage operations for better user experience and unification, so now there's no need to use 2 different SDKs!

It gives you an ability to:
- Upload, download, copy, move and delete files, including versions handling (if you are using Cloud storage that supports this feature - true by default).
- Create, copy, move and delete folders.
- Copy and move files and folders accross separate storages in scope of a single operation.
- Check if certain file, folder or storage exists.

## Getting Started with Aspose.Digram Cloud SDK for Node.js

You do not need to install anything to get started with Aspose.Diagram Cloud SDK for Node.js. All you need to do is create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information. 

The complete source code is available at [GitHub Repository](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-node). You can directly use it in your project via source code or get nmpjs distribution (recommended).

Please execute `npm install aspose-diagram-cloud-node --save` from the command line to install Aspose.Diagram Cloud SDK for Node.js via NPM.

## Create a Diagram File in the Cloud via Node.js

```js
const { DiagramFileApi, DiagramFile_PutCreateRequest } = require("asposediagramcloud");

var AppSid = ""
var AppKey = ""

diagramFileApi = new DiagramFileApi(AppSid, AppKey);

var req = new DiagramFile_PutCreateRequest();
req.name = "output.vdx";
req.isOverwrite = true;

diagramFileApi.diagramFilePutCreate(req).then((result) => {
    console.log('API Response:', result);
}).catch(function(err) {
    // deal with error
    console.log('Error:', err);
});
```

## Convert Visio to PDF in the Cloud via Node.js
```js
const { DiagramFileApi, DiagramFile_PostSaveAsRequest, FileFormatRequest } = require("asposediagramcloud");

var AppSid = "" 
var AppKey = "" 

diagramFileApi = new DiagramFileApi(AppSid, AppKey);

var StorageApi = require("asposestoragecloud")
var config = {'appSid':AppSid, 'apiKey':AppKey};
var storageApi = new StorageApi(config);

var fileName = 'template.vsd';
var data_path = '../your path/';

storageApi.PutCreate(fileName, versionId=null, storage=null, file= data_path + fileName , function(responseMessage) {
	console.log('status:', responseMessage.status);
	console.log('body:', responseMessage.body);
});

var req = new DiagramFile_PostSaveAsRequest();
var format = new FileFormatRequest();
format.format = "pdf";
req.name = fileName;
req.isOverwrite = true;
req.newfilename = "output.pdf";
req.format = format;

diagramFileApi.diagramFilePostSaveAs(req).then((result) => {
    console.log('API Response:', result);
}).catch(function(err) {
    // deal with error
    console.log('Error:', err);
});
```

[Product Page](https://products.aspose.cloud/diagram/nodejs) | [Documentation](https://docs.aspose.cloud/display/diagramcloud/Home) | [API Reference](https://apireference.aspose.cloud/diagram/) | [Code Samples](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-node) | [Blog](https://blog.aspose.cloud/category/diagram/) | [Free Support](https://forum.aspose.cloud/c/diagram) | [Free Trial](https://dashboard.aspose.cloud/#/apps)