# .NET API for Photoshop File Processing

A standalone .NET API to read, write, process & convert Adobe Photoshop PSD & PSB formats without needing to install Adobe Photoshop®.

[Aspose.PSD for .NET](https://products.aspose.com/psd/net) API allows to create and edit the Photoshop files as well as provides the ability to update layer properties, add watermarks, perform graphics operations and convert one file format to another.

## Photoshop File Processing Features

- Create Photoshop PSD & PSB files via API.
- Export PSD images to [popular image formats](https://docs.aspose.com/display/psdnet/Supported+File+Formats).
- Binarization with fixed & Otsu threshold.
- [Convert GIF image layers to TIFF](https://docs.aspose.com/display/psdnet/Converting+Images#ConvertingImages-ConvertGIFImageLayersToTIFFImage) & CMYK PSD to CMYK TIFF.
- Combine, expand or crop images.
- Create, read and write XMP data.
- Set default font as a replacement for all the missing fonts.
- Apply Median & Wiener filters to reduce image noise.
- Transform images to black-n-white or grayscale.
- [Crop images](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-CroppingImages) by shifts or rectangle.
- [Rotate an image](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-RotateandFlipanImage) on a specific angle
- Perform simple [image resize](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages), or by image proportions.
- Support for dithering of raster images.
- Adjust image brightness, contrast and gamma.
- Implement Lossy GIF Compression & Bicubic Resampling.
- Color Balance or invert Adjustment Layer.
- Draw basic objects such as lines, Ellipse, Rectangle, Arc, Bezier

## New Features in Version 20.3

- Support for .Net Core.
- Convert Adobe Illustrator files into PDFs.
- Ability to render different styles in one text layer.
- Support for Black and White Adjustment Layer.
- Export AI format (Version 8) to other formats.
- Support for PassThrough Blending Mode processing (Used for Layer Group Only).

For the detailed notes, please visit [Aspose.PSD for .NET 20.3 - Release Notes](https://docs.aspose.com/display/psdnet/Aspose.PSD+for+.NET+20.3+-+Release+Notes).

## New Feature Usage Example

### Convert Adobe Illustrator files into PDFs

```csharp
string sourceFile = "rect2_color.ai";
using (var aiImage = (AiImage)Image.Load(sourceFile))
{
    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());
}
```

For the detailed usage examples of all the new features, please visit [Aspose.PSD for .NET 20.3 - Release Notes](https://docs.aspose.com/display/psdnet/Aspose.PSD+for+.NET+20.3+-+Release+Notes).

## Read & Write Photoshop Formats

**Photoshop:** PSD, PSB

## Save Photoshop Files As

**Raster Formats:** TIFF, JPEG, PNG, GIF, BMP, JPEG2000

## Platform Independence

Aspose.PSD for .NET can work in any environment that supports .NET framework 2.0 or above.

## Getting Started with Aspose.PSD for .NET

Are you ready to give Aspose.PSD for .NET a try? Simply execute `Install-Package Aspose.PSD` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.PSD for .NET and want to upgrade the version, please execute `Update-Package Aspose.PSD` to get the latest version.

## Crop a PhotoShop PSD to Save Result in PNG format

You can execute below code snippet to see how Aspose.PSD API works in your own development environment or check the [GitHub Repository](https://github.com/aspose-psd/Aspose.PSD-for-.NET) for other common usage scenarios. 

```csharp
// implement correct Crop method for PSD files.
using (RasterImage image = Image.Load(dir + "template.psd") as RasterImage)
{
    image.Crop(new Rectangle(10, 30, 100, 100));
    image.Save(dir + "output.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
```

## Draw Rectangles in a PSD Image

Aspose.PSD for .NET provides options to process and manipulate Adobe Photoshop files including drawing new objects.

```csharp
// create an instance of Image
using (Image image = new PsdImage(100, 100))
{
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
    // draw a rectangle with Pen tool
    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
    // draw another rectangle with Solid Brush in Blue color
    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
}
```

[Product Page](https://products.aspose.com/psd/net) | [Documentation](https://docs.aspose.com/display/psdnet/Home) | [API Reference](https://apireference.aspose.com/net/psd) | [Code Examples](https://github.com/aspose-psd/Aspose.PSD-for-.NET) | [Blog](https://blog.aspose.com/category/psd/) | [Free Support](https://forum.aspose.com/c/psd) |  [Temporary License](https://purchase.aspose.com/temporary-license)
