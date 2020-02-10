This cloud SDK assists to process & manipulate images from within your C#, ASP.NET & other .NET based cloud applications, without installing any 3rd party tool.

Apose.Imaging Cloud SDK for .NET is built on top of Aspose.Imaging REST API and is distributed under an MIT license. Aspose.Imaging Cloud SDK for .NET enables your C# code to fetch images from cloud storage and perform various operations, such as, resizing, cropping, merging, scaling, and converting images. You can also perform various operations on TIFF images. Extract a single TIFF from to crop, resize, rotate, or flip it. Aspose.Imaging Cloud SDK for .NET also enables you to convert TIFF to fax compatible format.

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

## Getting Started with Aspose.Imaging Cloud SDK for .NET

You do not need to install anything to get started with Aspose.Imaging Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.Imaging-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.Imaging assembly in your project. If you already have Aspose.Imaging Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.Imaging-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-dotnet) for other common usage scenarios.

## Export an Image to PDF Format via C# Code

This code sample demonstrates, how to convert an image to PDF format using C# code via REST API:

```csharp
string format = "pdf"; // specify the export output format
string outPath = null; // Path to updated file (if this is empty, response contains streamed image)
string storage = null; // Cloud Storage name

var request = new CreateSavedImageAsRequest(inputImageStream, format, outPath, storage);

Console.WriteLine($"Call CreateSavedImageAs with params: format:{format}");

using (Stream updatedImage = this.ImagingApi.CreateSavedImageAs(request))
    {
        SaveUpdatedImageToOutput(updatedImage, true, format);
    }
```

[Product Page](https://products.aspose.cloud/imaging/net) | [Documentation](https://docs.aspose.cloud/display/imagingcloud/Home) | [API Reference](https://apireference.aspose.cloud/imaging/) | [Code Samples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/imaging/) | [Free Support](https://forum.aspose.cloud/c/imaging) | [Free Trial](https://dashboard.aspose.cloud/#/apps)