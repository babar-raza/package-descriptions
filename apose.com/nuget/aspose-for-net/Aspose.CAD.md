A standalone C# class library to enhance ASP.NET & Windows applications to process & render AutoCAD® drawings without requiring AutoCAD or any other tools.

Aspose.CAD for .NET allows you to work with 3D solids (Conic, Sphere, Torus, Cylinder, Box, Wedge), wired models, basic cube positions, 3D faces, surfaces as well as meshes.

## AutoCAD File Processing Features
- Adjust CAD drawing size.
- Render entire drawing in DWF as a PDF.
- Export a DWG file with embedded DGN.
- Export embedded OLE objects from DWG.
- Export AutoCAD DXF 2010 to PDF.
- Export specific DXF layer to PDF & images.
- Export IFC to PNG format.
- Export IGES to PDF format.
- Export PLT to PDF & images.
- Export SLT to PNG format.
- Export 3D AutoCAD images to PDF format.
- Export DGN to PDF & raster images.
- Convert CF2 to PDF.
- Convert DXF & DWG to raster images.
- Convert all CAD layers to separate images.
- Search text in DWG drawings.
- Access & update hyperlink properties in a DWG.
- Add Text or MText watermark to a DWG.
- Load & save DWT files.
- Distinguish among DWG & DWT file formats.
- Supports all widespread 2D entities of DXF.
- Highly customizable CAD to PDF & image conversion process.
- Enable tracking for CAD rendering.

## Read AutoCAD File Formats
DWG Release 11, 12, 13, 14, DWG 2000/2000i/2002, DWG 2004/2005/2006, DWG 2010/2011/2012, DWG 2013/2014/2015/2016, AutoCAD® DXF, Autodesk DWF, DGN, Industry Foundation Classes (IFC), STereoLithography (STL)

## Save AutoCAD Drawings As
**Fixed Layout:** PDF
**Raster Images:** PNG, BMP, TIFF, JPEG, GIF

## Platform Independence
Aspose.CAD for .NET supports, .NET framework (ASP.NET applications & Windows applications) as well as .NET code. It supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed, this includes but is not limited to, Microsoft Windows desktop (XP, Vista, 7, 8, 10), Microsoft Windows Server (2003, 2008, 2012), Microsoft Azure, Linux (Ubuntu, OpenSUSE, CentOS and others), and Mac OS X.


## Getting Started with Aspose.CAD for .NET
Are you ready to give Aspose.CAD for .NET a try? Simply execute `Install-Package Aspose.CAD` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.CAD for .NET and want to upgrade the version, please execute `Update-Package Aspose.CAD` to get the latest version. 

### Add Watermark to an AutoCAD File using C#
You can execute below code snippet to see how the API performs in your environment or check the [GitHub Repository](https://github.com/aspose-cad/Aspose.CAD-for-.NET) for other common usage scenarios.
```csharp
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
```

### Export DXF Drawing to PDF using C#
Aspose.CAD for .NET enables your applications to perform various export operations on AutoCAD files. It supports to read and export ACAD Proxy Entities as well as IGES files. Similarly you can load a DGN file and convert it to a raster image or PDF file format. 

The following example highlights, how to export DXF file to PDF format using simple C# code:
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