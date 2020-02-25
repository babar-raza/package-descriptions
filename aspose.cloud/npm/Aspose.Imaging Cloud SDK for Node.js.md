This cloud SDK assists to process & manipulate images from within your Node.js based cloud applications, without installing any 3rd party tool.

Apose.Imaging Cloud SDK for Node.js is built on top of Aspose.Imaging REST API and is distributed under an MIT license. Aspose.Imaging Cloud SDK for Node.js enables your Node.js code to fetch images from cloud storage and perform various operations, such as, resizing, cropping, merging, scaling, and converting images. You can also perform various operations on TIFF images. Extract a single TIFF from to crop, resize, rotate, or flip it. Aspose.Imaging Cloud SDK for Node.js also enables you to convert TIFF to fax compatible format.

## Image Processing Features

- Fetch or update properties of cloud hosted images.
- Scale, flip, crop and export an image with a single API call.
- Resize, crop, flip, convert and export an image to other supported formats.
- Update image parameters of JPEG2000 & WEBP images.
- Access and multi-frame TIFF image and extract the desired frames from it.
- Rotate, flip, crop, resize or fetch properties of the selected TIFF frame.
- Merge multiple TIFF images.

## Read & Write Image Formats

BMP, GIF, JPEG, JPEG2000, PSD, TIFF, WEBP, PNG, WMF, EMF, SVG

## Save Image As

PDF

## Read Image Formats

DJVU, DICOM, CDR, CMX, ODG, DNG

## Platform Independence

Aspose.Imaging Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.Imaging Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.Imaging for Cloud via NPM, please execute from the command line, `npm install aspose-imaging-cloud-node --save`.

## Use Node.js to Compare two Images

```js
const imagingApi = new imaging.ImagingApi("yourAppKey", "yourAppSID");
 
// create search context or use existing search context ID if search context was created earlier
const apiResponse = await imagingApi.createImageSearch(
    new imaging.CreateImageSearchRequest());
const searchContextId = apiResponse.id;
 
// specify images for comparing (image ID is a path to image in storage)
const imageInStorage1 = "WorkFolder\Image1.jpg";
const imageInStorage2 = "WorkFolder\Image2.jpg";
  
// compare images
const response = await imagingApi.compareImages(
    new imaging.CompareImagesRequest({ 
        searchContextId, imageId1: imageInStorage1, imageId2: imageInStorage2 }));
const similarity = response.results[0].similarity;
```

[Product Page](https://products.aspose.cloud/imaging/nodejs) | [Documentation](https://docs.aspose.cloud/display/imagingcloud/Home) | [API Reference](https://apireference.aspose.cloud/imaging/) | [Code Samples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-node) | [Blog](https://blog.aspose.cloud/category/imaging/) | [Free Support](https://forum.aspose.cloud/c/imaging) | [Free Trial](https://dashboard.aspose.cloud/#/apps)