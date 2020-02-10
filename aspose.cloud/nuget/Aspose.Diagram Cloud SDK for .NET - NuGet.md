This cloud SDK enables your C#, ASP.NET & other .NET cloud apps to create & process Visio diagrams from within your apps without installing Microsoft Visio.

Aspose.Diagram Cloud SDK for .NET is built on top of Aspose.Diagram REST API and is distributed for use under an MIT license.

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

## Getting Started with Aspose.Diagram Cloud SDK for .NET

You do not need to install anything to get started with Aspose.Diagram Cloud SDK for .NET. All you need to do is create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.Diagram-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.Diagram assembly in your project. If you already have Aspose.Diagram Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.Diagram-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-dotnet) for other common usage scenarios.

## Using C# to Create a New VDX Format Diagram in the Cloud

This code example demonstrates, how to create a new diagram of VDX format using C# code:

```csharp
DiagramFileApi instance = new DiagramFileApi(GetConfiguration());

string name = "New_Diagram.vdx";
bool isOverwrite = true;
string folder = null;

var response = instance.DiagramFilePutCreate(name, folder, isOverwrite);
```

[Product Page](https://products.aspose.cloud/diagram/net) | [Documentation](https://docs.aspose.cloud/display/diagramcloud/Home) | [API Reference](https://apireference.aspose.cloud/diagram/) | [Code Samples](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/diagram/) | [Free Support](https://forum.aspose.cloud/c/diagram) | [Free Trial](https://dashboard.aspose.cloud/#/apps)