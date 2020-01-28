A standalone .NET API to read, write, process & convert Adobe Photoshop PSD & PSB formats without needing to install Adobe Photoshop®. 

Aspose.PSD for .NET API allows to create and edit the Photoshop files as well as provides the ability to update layer properties, add watermarks, perform graphics operations or convert one file format to another.

## Photoshop File Processing Features
- Create Photoshop PSD & PSB files via API.
- Export PSD images to popular image formats.
- Binarization with fixed & Otsu threshold.
- Convert GIF image layers to TIFF & CMYK PSD to CMYK TIFF.
- Combine, expand or crop images.
- Create, read and write XMP data.
- Set default font as a replacement for all the missing fonts.
- Apply Median & Wiener filters to reduce image noise.
- Transform images to black-n-white or grayscale.
- Crop images by shifts or rectangle.
- Rotate an image on a specific angle
- Perform simple image resize, or by image proportions.
- Support for dithering of raster images.
- Adjust image brightness, contrast and gamma.
- Implement Lossy GIF Compression & Bicubic Resampling.
- Color Balance or invert Adjustment Layer.
- Draw basic objects such as lines, Elipse, Rectangle, Arc, Bezier

## Read & Write Photoshop Formats
**Photoshop:** PSD, PSB

## Save Photoshop Files As
**Raster Formats:** TIFF, JPEG, PNG, GIF, BMP, JPEG2000

## Platform Independence
Aspose.PSD for .NET can work in any environment that supports .NET framework 2.0 or above.

## Getting Started with Aspose.PSD for .NET
Are you ready to give Aspose.PSD for .NET a try? Simply execute `Install-Package Aspose.PSD` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.PSD for .NET and want to upgrade the version, please execute `Update-Package Aspose.PSD` to get the latest version.

### Crop a PhotoShop PSD to Save Result in PNG format
You can execute below code snippet to see how Aspose.PSD API works against your own sample or check the [GitHub Repository](https://github.com/aspose-psd/Aspose.PSD-for-.NET) for other common usage scenarios. 

```csharp
// implement correct Crop method for PSD files.
using (RasterImage image = Image.Load(dir + "template.psd") as RasterImage)
{
    image.Crop(new Rectangle(10, 30, 100, 100));
    image.Save(dir + "output.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
```

### Draw Rectangles in a PSD Image
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