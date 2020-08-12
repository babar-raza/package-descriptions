# CAD File Conversion API for .NET

[Aspose.CAD for .NET](https://products.aspose.com/cad/net) is a standalone class library to enhance ASP.NET & Windows applications to process & render CAD drawings without requiring AutoCAD or any other rendering workflow. The CAD Class Library allows high quality [conversion of DWG, DWF, DWT and DXF](https://docs.aspose.com/cad/net/supported-file-formats/) files, layouts and layers to PDF & raster image formats.

## CAD File Processing Features

- Supports the latest versions of DWG, DWF, DWT & DXF formats.
- Convert [CAD to PDF](https://docs.aspose.com/cad/net/converting-cad-drawings-to-pdf-and-raster-image-formats/).
- Convert CAD to images.
- Select and convert specific layouts of CAD drawings.
- Select and convert specific layers of CAD drawings.
- [Adjust CAD drawing size before rendering](https://docs.aspose.com/cad/net/adjusting-cad-drawing-size/).

## New Features & Enhancements in Version 20.6

- There are several enhancements in this version.

## Added APIs in Version 20.6

- **Class**:         `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellElement`
- **Field/Enum**:    `Aspose.CAD.ImageOptions.RenderErrorCode.PdfRendererFailed`
- **Method**:        `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellDefinitionElement.AddChild(Aspose.CAD.FileFormats.Dgn.DgnElements.DgnElement)`
- **Method**:        `Aspose.CAD.FileFormats.Dgn.DgnTransform.DgnQuaternion.#ctor(System.Int64,System.Int64,System.Int64,System.Int64)`
- **Method**:        `Aspose.CAD.Point.op_Explicit(Aspose.CAD.Point)`
- **Method**:        `Aspose.CAD.PointF.op_Explicit(Aspose.CAD.PointF)`
- **Method**:        `Aspose.CAD.Xmp.XmpPackage.SetValue(System.String,)`
- **Property**:      `Aspose.CAD.FileFormats.Cad.CadAciColor.White`
- **Property**:      `Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities.CadAttrib.Visible`
- **Property**:      `Aspose.CAD.FileFormats.Cad.CadObjects.CadMaterial.Attribute282`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnShapeElement.Filled`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellDefinitionElement.Childs`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellDefinitionElement.Name`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellElement.Definition`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellElement.Id`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellElement.MaxPoint`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellElement.MinPoint`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellElement.Name`
- **Property**:      `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellElement.Origin`
- **Property**:      `Aspose.CAD.ImageOptions.CadRenderResult.Failures`
- **Property**:      `Aspose.CAD.LoadOptions.CustomFontFolders`

## Removed APIs in Version 20.6

- **Class**:        `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellDefinition`
- **Field/Enum**:   `Aspose.CAD.ImageOptions.CadRenderResult.Failures`
- **Method**:       `Aspose.CAD.FileFormats.Dgn.DgnTransform.DgnQuaternion.#ctor(System.Int32,System.Int32,System.Int32,System.Int32)`
- **Method**:       `Aspose.CAD.Point.op_Explicit(Aspose.CAD.Point)`
- **Method**:       `Aspose.CAD.PointF.op_Explicit(Aspose.CAD.PointF)`
- **Method**:       `Aspose.CAD.Xmp.XmpPackage.SetValue(System.String)`
- **Class**:        `Aspose.CAD.FileFormats.Dgn.DgnElements.DgnSharedCellDefinition`
- **Field/Enum**:   `Aspose.CAD.ImageOptions.CadRenderResult.Failures`
- **Method**:       `Aspose.CAD.FileFormats.Dgn.DgnTransform.DgnQuaternion.#ctor(System.Int32,System.Int32,System.Int32,System.Int32)`
- **Method**:       `Aspose.CAD.Point.op_Explicit(Aspose.CAD.Point)`
- **Method**:       `Aspose.CAD.PointF.op_Explicit(Aspose.CAD.PointF)`
- **Method**:       `Aspose.CAD.Xmp.XmpPackage.SetValue(System.String)`

## Read CAD Formats

**AutoCAD:** DWG, DWT, DWF, DWXF, IFC, PLT
**MicroStation:** DGN
**The Advanced Visualizer:** OBJ
**Other:** STL, IGES, CFF2

## Save CAD As

**Fixed Layout:** PDF
**Raster Images:** PNG, BMP, TIFF, JPEG, GIF

## Read & Write

**CAD:** DXF
(Write features is partially supported.)

## Platform Independence

Aspose.CAD for .NET supports .NET framework (ASP.NET applications & Windows applications) as well as .NET Core. It supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed, this includes but is not limited to, Microsoft Windows desktop (XP, Vista, 7, 8, 10), Microsoft Windows Server (2003, 2008, 2012), Microsoft Azure, Linux (Ubuntu, OpenSUSE, CentOS and others), and Mac OS X.

# Getting Started with Aspose.CAD for .NET

Are you ready to give Aspose.CAD for .NET a try? Simply execute `Install-Package Aspose.CAD` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.CAD for .NET and want to upgrade the version, please execute `Update-Package Aspose.CAD` to get the latest version. 

## Add Watermark to CAD using C#

You can execute below code snippet to see how the API performs in your environment or check the [GitHub Repository](https://github.com/aspose-cad/Aspose.CAD-for-.NET) for other common usage scenarios.

```csharp
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
```

## Export DXF to PDF using C#

Aspose.CAD for .NET enables your applications to perform various export operations on CAD files. It supports to read and export ACAD Proxy Entities as well as IGES files. Similarly you can [load and convert CAD drawings to raster images or PDF](https://docs.aspose.com/display/cadnet/Converting+CAD+Drawings+to+PDF+and+Raster+Image+Formats). 

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;

rasterizationOptions.Layouts = new string[] { "Model" };
var pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(dir + "output.pdf", pdfOptions);
```

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/cad/net) | [Docs](https://docs.aspose.com/cad/net/) | [Demos](https://products.aspose.app/cad/family) | [API Reference](https://apireference.aspose.com/cad/net) | [Examples](https://github.com/aspose-cad/Aspose.CAD-for-.NET) | [Blog](https://blog.aspose.com/category/cad/) | [Free Support](https://forum.aspose.com/c/cad) | [Temporary License](https://purchase.aspose.com/temporary-license)
