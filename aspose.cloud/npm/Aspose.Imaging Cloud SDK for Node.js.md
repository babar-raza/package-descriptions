Node.js Cloud SDK wraps Aspose.Imaging REST API so you could seamlessly integrate image file creation, manipulation & conversion features into your own Node.js applications.

# Create, Manipulate & Convert Images in the Cloud

[Aspose.Imaging Cloud](https://products.aspose.cloud/imaging) is a true [REST API](https://apireference.aspose.cloud/imaging/) that enables you to perform a wide range of image processing operations including creation, manipulation and conversion in the cloud, with zero initial cost. Checkout the [API Reference](https://apireference.aspose.cloud/imaging/) to know what else Aspose.Imaging Cloud can do.

## Image Processing Features

- Export images to variety of other formats.
- [Fetch or update properties of cloud hosted images](https://docs.aspose.cloud/display/imagingcloud/Working+with+Image+Properties).
- Scale, flip, crop, rotate and export images with a single API call.
- Update image parameters of JPEG2000 & WEBP formats.
- [Access multi-frame TIFF image](https://docs.aspose.cloud/display/imagingcloud/Working+with+TIFF+Frames) and extract the desired frames as well as merge multiple TIFF images.
- Convert images for PDF.
- Apply imaging filters.
- Imaging AI operations:
	- Context-based image search.
	- [Duplicate image search](https://docs.aspose.cloud/display/imagingcloud/Find+Duplicate+Images).
	- [Image search by custom registered tags](https://docs.aspose.cloud/display/imagingcloud/Find+Images+By+Tags).
	- Image comparison and similarity detection.
	- Image features extraction (for now, AKAZE detector is supported).

## New Features in Version 20.2

- Added support for grayscale images.

For the detailed notes, please visit [Aspose.Imaging Cloud 20.2 - Release Notes](https://docs.aspose.cloud/display/imagingcloud/Aspose.Imaging+Cloud+20.2+-+Release+Notes).

## Read & Write Image Formats

BMP, GIF, JPEG, JPEG2000, PSD, TIFF, WEBP, PNG, WMF, EMF, SVG

## Save Images As

PDF

## Read Images From

DJVU, DICOM, CDR, CMX, ODG, DNG

## Storage API Support

Since version 19.4, SDK includes support of storage operations for better user experience and unification, so now there's no need to use 2 different SDKs!

It gives the ability to:

- Upload, download, copy, move and delete files, including versions handling (if you are using Cloud storage that supports this feature - true by default).
- Create, copy, move and delete folders.
- Copy and move files and folders across separate storages in scope of a single operation.
- Check if certain file, folder or storage exists.

## Getting Started with Aspose.Imaging Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install @asposecloud/aspose-imaging-cloud --save` from the command line to install Aspose.Imaging Cloud SDK for Node.js via NPM. The complete source code is available at [GitHub Repository](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-node).

The best way to become familiar with how to use the SDK is to read the [Developer Guide](https://docs.aspose.cloud/display/imagingcloud/Developer+Guide) whereas the [Getting Started](https://docs.aspose.cloud/display/imagingcloud/Getting+Started) section will help you understand the common concepts.

## Using Node.js to Compare Images

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

[Product Page](https://products.aspose.cloud/imaging/nodejs) | [Documentation](https://docs.aspose.cloud/display/imagingcloud/Home) | [Live Demo](https://products.aspose.app/imaging/family) | [API Reference](https://apireference.aspose.cloud/imaging/) | [Examples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-node) | [Blog](https://blog.aspose.cloud/category/imaging/) | [Free Support](https://forum.aspose.cloud/c/imaging) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
