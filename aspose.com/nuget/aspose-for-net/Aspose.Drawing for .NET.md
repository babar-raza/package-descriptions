# .NET API to Process Drawing File Formats

[Aspose.Drawing for .NET](https://products.aspose.com/drawing/net) is a cross-platform library that provides `System.Drawing` and `GDI+` compatible API.

Our drawing engine supports rendering vector graphics (such as lines, curves, and figures) and text (in a variety of fonts, sizes, and styles) onto raster images in popularly used graphics file formats (BMP, PNG, JPEG, GIF, TIFF).

## Graphic File Processing Features

- [Create bitmap](https://docs.aspose.com/display/drawingnet/Create+Image#CreateImage-CreateNewBitmap) from scratch or load from file.
- [Convert images](https://docs.aspose.com/display/drawingnet/Convert+Images#ConvertImages-ConvertImageinC#) from one format to another.
- [Draw arc](https://docs.aspose.com/display/drawingnet/Working+with+Vector+Graphics#WorkingwithVectorGraphics-DrawArc), bezier spline, cardinal spline, closed curve.
- Draw eclipse, lines, path, polygon, rectangle.
- Fill region.
- Set pen width and [pen color to Draw Graphics](https://docs.aspose.com/display/drawingnet/Working+with+Pens#WorkingwithPens-SetPenColortoDrawGraphics).
- Join paths using pen.
- Using [solid brush to draw graphics](https://docs.aspose.com/display/drawingnet/Working+with+Brushes#WorkingwithBrushes-UsingSolidBrushtoDrawGraphicsinC#).
- Work with [alpha blending](https://docs.aspose.com/display/drawingnet/Working+with+Image+Rendering#WorkingwithImageRendering-AlphaBlending), antialiasing, and clipping.
- Support for transformations, such as, [matrix](https://docs.aspose.com/display/drawingnet/Working+with+Coordinate+System+Transformations#WorkingwithCoordinateSystemTransformations-MatrixTransformation), page, world, local & global.
- Format fonts and [text styles](https://docs.aspose.com/display/drawingnet/Working+with+Text+and+Fonts#WorkingwithTextandFonts-TextStyles-Hinting) to draw text during graphics drawing.

## New Features & Enhancements in Version 20.6

- This is the first release of this new product.

For the detailed notes, please visit [Aspose.Drawing for .NET 20.6](https://docs.aspose.com/display/drawingnet/Aspose.Drawing+for+.NET+20.6).

## Read & Write Drawing Formats

BMP, PNG, JPEG, GIF, TIFF

## Platform Independence

The project is based on managed .NET core and does not have dependencies on native code and libraries, with the rendering algorithms working the same way on all supported platforms.

Aspose.Drawing for .NET supports any 32-bit or 64-bit operating system where .NET Framework or .NET Core is installed including, but not limited to:

- Microsoft Windows desktop (XP, Vista, 7, 8, 10) and server operating systems (2003, 2008, 2012, 2016, 2019)
- Windows Azure
- Linux
- Mac OS X

It also supports .NET Framework version 2.0 and .NET Core 2.0 or later. You can use Aspose.Drawing for .NET to develop applications in any development environment that targets the .NET platform. However, Microsoft Visual Studio 2012, 2013, 2015, 2017, 2019 are explicitly supported.

## Getting Started with Aspose.Drawing for .NET

Are you ready to give Aspose.Drawing for .NET a try? Simply execute `Install-Package Aspose.Drawing` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Drawing for .NET and want to upgrade the version, please execute `Update-Package Aspose.Drawing` to get the latest version.

## Create New Bitmap using C# Code

You can execute below code snippet to see how Aspose.Drawing API performs in your own environment or check the [GitHub Repository](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET) for other common usage scenarios. 

```csharp
// For complete examples and data files, please go to https://github.com/aspose-drawing/Aspose.Drawing-for-.NET
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);

Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawArc(pen, 0, 0, 700, 700, 0, 180);

bitmap.Save(RunExamples.GetDataDir() + @"LinesCurvesShapes\DrawArc_out.png");
```

[Product Page](https://products.aspose.com/drawing/net) | [Docs](https://docs.aspose.com/display/drawingnet/Home) | [API Reference](https://apireference.aspose.com/net/drawing) | [Examples](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET) | [Blog](https://blog.aspose.com/category/drawing/) | [Free Support](https://forum.aspose.com/c/drawing) | [Temporary License](https://purchase.aspose.com/temporary-license)
