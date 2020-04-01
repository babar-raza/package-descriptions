# AutoCAD File Conversion API for .NET

[Aspose.CAD for .NET](https://products.aspose.com/cad/net) is a standalone class library to enhance ASP.NET & Windows applications to process & render AutoCAD® drawings without requiring AutoCAD or any other tools. The CAD .NET API allows high quality [conversion of AutoCAD DWG, DWF, DWT and DXF](https://docs.aspose.com/display/cadnet/Supported+File+Formats) files, layouts and layers to PDF & raster image formats.

## AutoCAD File Processing Features

- Supports the latest versions of AutoCAD DWG, DWF, DWT and DXF formats.
- Convert the [AutoCAD files to PDF](https://docs.aspose.com/display/cadnet/Converting+CAD+Drawings+to+PDF+and+Raster+Image+Formats).
- Convert the AutoCAD files to raster images.
- Select and convert specific layouts of AutoCAD drawings.
- Select and convert specific layers of AutoCAD drawings.
- [Adjust AutoCAD drawing size before rendering](https://docs.aspose.com/display/cadnet/Adjusting+CAD+Drawing+Size).
- Track the file conversion process.

## New Features in Version 20.3

- Interrupt or put a timeout on `Save`.
- Support for `DXF` Version.
- Support for `DWFX` files.
- Automatic codepage detection for DWG and DXF.

For the detailed notes, please visit [Aspose.CAD for .NET 20.3 - Release Notes](https://docs.aspose.com/display/CADNET/Aspose.CAD+for+.NET+20.3+-+Release+Notes).

## Read AutoCAD File Formats

**AutoCAD:** DWG, DWT, DWF, DWXF, IFC, PLT
**MicroStation:** DGN
**The Advanced Visualizer:** OBJ
**Other:** STL, IGES, CFF2

## Save AutoCAD Drawings As

**Fixed Layout:** PDF
**Raster Images:** PNG, BMP, TIFF, JPEG, GIF

## Read & Write Formats

**AutoCAD:** DXF
(Write features is partially supported.)

## Platform Independence

Aspose.CAD for .NET supports .NET framework (ASP.NET applications & Windows applications) as well as .NET Core. It supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed, this includes but is not limited to, Microsoft Windows desktop (XP, Vista, 7, 8, 10), Microsoft Windows Server (2003, 2008, 2012), Microsoft Azure, Linux (Ubuntu, OpenSUSE, CentOS and others), and Mac OS X.

# Getting Started with Aspose.CAD for .NET

Are you ready to give Aspose.CAD for .NET a try? Simply execute `Install-Package Aspose.CAD` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.CAD for .NET and want to upgrade the version, please execute `Update-Package Aspose.CAD` to get the latest version. 

## Add Watermark to an AutoCAD File using C#

You can execute below code snippet to see how the API performs in your environment or check the [GitHub Repository](https://github.com/aspose-cad/Aspose.CAD-for-.NET) for other common usage scenarios.

```csharp
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
```

## Export DXF Drawing to PDF using C#

Aspose.CAD for .NET enables your applications to perform various export operations on AutoCAD files. It supports to read and export ACAD Proxy Entities as well as IGES files. Similarly you can [load and convert CAD drawings to raster images or PDF](https://docs.aspose.com/display/cadnet/Converting+CAD+Drawings+to+PDF+and+Raster+Image+Formats). 

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;

rasterizationOptions.Layouts = new string[] { "Model" };
var pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(dir + "output.pdf", pdfOptions);
```

[Product Page](https://products.aspose.com/cad/net) | [Documentation](https://docs.aspose.com/display/cadnet/Home) | [API Reference](https://apireference.aspose.com/net/cad/) | [Code Examples](https://github.com/aspose-cad/Aspose.CAD-for-.NET) | [Blog](https://blog.aspose.com/category/cad/) | [Free Support](https://forum.aspose.com/c/cad) |  [Temporary License](https://purchase.aspose.com/temporary-license)
