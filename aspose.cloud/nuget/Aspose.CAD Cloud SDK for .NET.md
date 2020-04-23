# AutoCAD File Processing .NET Cloud REST API

This Cloud SDK helps you perform [AutoCAD drawing conversion, processing & manipulation](https://products.aspose.cloud/cad/net) from within your C#, ASP.NET, & other .NET cloud apps without AutoCAD.

## CAD Processing Features

- Export CAD drawings to other file formats.
- Get image properties of a CAD drawing.
- Change scale of an AutoCAD sketch.
- Flip and rotate a CAD image.
- Upload or download CAD drawings to the cloud storage.
- Copy, move, delete CAD files from the cloud storage.

## Read & Write CAD Formats

DXF (R12/2007/2010)

## Save CAD As

**Fixed Layout:** PDF (as a vector and as a raster)
**Images:** BMP, PNG, JPG, JPEG, JPEG2000, TIF, TIFF, PSD, GIF, WMF

## Read CAD Formats

DWG (13, 14, 2000, 2004), DWG (2010, 2013, 2014), DWG (2015, 2017, 2018), DWT (13, 14, 2000, 2004), DWT (2010, 2013, 2014), DWT (2015, 2017, 2018), DWF, DGN v7, IGES (IGS), PLT, Industry Foundation Classes (IFC), STereoLithography (STL)

## Getting Started with Aspose.CAD Cloud SDK for .NET

You do not need to install anything to get started with Aspose.CAD Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.CAD-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.CAD assembly in your project. If you already have Aspose.CAD Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.CAD-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-cad-cloud/aspose-cad-cloud-dotnet) for other common usage scenarios.

## Using C# to Get Image Properties of a DXF File

The following code sample demonstrates, how to retrieve image properties of a DXF file format drawing using C# code:

```csharp
 CADApi cadApi = new CADApi(AppKey, AppSid);
string fileName = "Input.dxf";

// Upload document to Cloud Storage
uploadFileToCloudStorage(fileName);

var request = new GetImagePropertiesRequest(fileName, null, null);
var properties = cadApi.GetImageProperties(request);
```

## Using C# Convert DWG CAD drawing to PDF Format

The following code snippet elaborates, how to convert a DWG file to PDF file format in the cloud using C# code:

```csharp
CADApi cadApi = new CADApi(AppKey, AppSid);
string fileName = "Input.dwg";
string formatToExport = "pdf";
string destFileName = "Output.pdf";

// Upload document to Cloud Storage
uploadFileToCloudStorage(fileName);

var request = new GetImageSaveAsRequest(fileName, formatToExport, null, null, null, null);
var responseStream = cadApi.GetImageSaveAs(request);

// Save the output file to disk
saveFileToDisk(responseStream, destFileName);
```

[Product Page](https://products.aspose.cloud/cad/net) | [Documentation](https://docs.aspose.cloud/display/cadcloud/Home) | [Demo](https://products.aspose.app/cad/family) | [API Reference](https://apireference.aspose.cloud/cad/) | [Examples](https://github.com/aspose-cad-cloud/aspose-cad-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/cad/) | [Free Support](https://forum.aspose.cloud/c/cad) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
