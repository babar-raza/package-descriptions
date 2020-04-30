# .NET Cloud REST API for Visio Processing

This cloud SDK enables your C#, ASP.NET & other .NET cloud apps to [create & process Visio diagrams](https://products.aspose.cloud/diagram/net) from within your apps without installing Microsoft Visio.

## Visio Processing Features

- Retrieve document information of a Visio diagram.
- Programmatically create a new Microsoft Visio diagram file.
- Convert Visio flow-charts to other supported formats.
- Upload your business oriented Visio diagrams to cloud storage.
- Export Visio files to raster images, fixed-layout and HTML formats.

## New Features in Version 20.3

- Added support to:
  - Set page setting.
  - Add new empty page.
  - Get pages info.
- Added support to draw following objects on a page:
  - Polyline
  - Line
  - Ellipse

For the detailed notes, please visit [Aspose.Diagram Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/diagramcloud/Aspose.Diagram+Cloud+20.3+Release+Notes).

## Read & Write Visio Formats

**Microsoft Visio:** VSDX, VSX, VTX, VDX, VSSX, VSTX, VSDM, VSSM, VSTM

## Save Visio As

**Fixed Layout:** PDF, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG, EMF
**Web:** HTML
**Other:** XAML, SWF

## Read Visio Formats

**Microsoft Visio:** VDW, VSD, VSS, VST

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

[Product Page](https://products.aspose.cloud/diagram/net) | [Documentation](https://docs.aspose.cloud/display/diagramcloud/Home) | [Demo](https://products.aspose.app/diagram/family) | [API Reference](https://apireference.aspose.cloud/diagram/) | [Examples](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/diagram/) | [Free Support](https://forum.aspose.cloud/c/diagram) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
