# .NET API for Image Processing

It is a [standalone Imaging API](https://products.aspose.com/imaging/net) consists of C# routines that enable your .NET applications to draw as well as perform basic to advanced level processing of raster & vector images.

Aspose.Imaging for .NET offers robust image compression and high processing speed through native byte access and a range of efficient algorithms. It not only manipulate, export and convert images but also lets you dynamically draw objects using pixel manipulation and Graphics Path.

## Imaging API Features

- Draw raster images with graphics.
- Draw vector images.
- Converting images to various formats.
- [Apply masking](https://docs.aspose.com/display/imagingnet/Applying+Masking+to+Images) as well as [Median & Wiener](https://docs.aspose.com/display/imagingnet/Applying+Median+and+Wiener+Filters) filters.
- Crop, rotate & resize images via API.
- De-skew & transform images.
- Set image properties.

## New Features in Version 20.4

- Supports text in the *CDR* format on *X3* and below versions.
- Export to *Html5* canvas format.
- Allow speed or memory optimization strategies for *Webp* format.
- Supports compressed vector formats.

## PSD Off Notice

Please switch to [Aspose.PSD](https://products.aspose.com/psd) for PSD loading functionality. The functionality is not supported from this release.

## Compact Framework Off Notice

Please note in next Aspose.Imaging releases support of .NET Compact Framework in Aspose.Imaging will be removed.

For the detailed notes, please visit [Aspose.Imaging for .NET 20.4 - Release notes](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+20.4+-+Release+notes).

## Read & Write Image Formats

**Raster Formats:** JPEG2000, JPEG, BMP, TIFF, GIF, PNG
**Metafiles:** EMF, WMF
**Other:** WEBP, SVG

## Save Images As

**Fixed:** PDF
**Photoshop:** PSD

## Read Image Formats

**Various:** DICOM, DjVu, DNG, ODG, CMX, CDR, DIB, OTG, FODG, EPS (raster preview only)

## Platform Independence

Aspose.Imaging for .NET can be used to develop applications on Windows Desktop (x86, x64), Windows Server (x86, x64), Windows Azure, Windows Embedded (CE 6.0 R2), as well as Linux x64. The supported platforms include .NET Framework version 2.0 or higher, and .NET Compact Framework 3.5.

## Getting Started with Aspose.Imaging for .NET

Are you ready to give Aspose.Imaging for .NET a try? Simply execute `Install-Package Aspose.Imaging` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Imaging for .NET and want to upgrade the version, please execute `Update-Package Aspose.Imaging` to get the latest version.

## Resize a JPG Image via C# Code

Execute below code snippet to see how Aspose.Imaging performs in your environment or check the [GitHub Repository](https://github.com/aspose-imaging/Aspose.Imaging-for-.NET) for other common usage scenarios. 

```csharp
using (Image image = Image.Load(dir + "template.jpg"))
{
    image.Resize(300, 300);
    image.Save(dir + "output.jpg");
}
```

## Recover a Broken TIFF

You can programmatically recover a damaged TIFF file with the help of Aspose.Imaging for .NET API as demonstrated below.

```csharp
// create an instance of LoadOptions and set LoadOptions properties
var loadOptions = new LoadOptions();
loadOptions.DataRecoveryMode = DataRecoveryMode.ConsistentRecover;
loadOptions.DataBackgroundColor = Color.Red;

// create an instance of Image and load a damaged image by passing the instance of LoadOptions
using (var image = Image.Load(dir + "template.tiff", loadOptions))
{
    // do processing
}
```

[Product Page](https://products.aspose.com/imaging/net) | [Documentation](https://docs.aspose.com/display/imagingnet/Home) | [Demo](https://products.aspose.app/imaging/family) | [API Reference](https://apireference.aspose.com/net/imaging) | [Examples](https://github.com/aspose-imaging/Aspose.Imaging-for-.NET) | [Blog](https://blog.aspose.com/category/imaging/) | [Free Support](https://forum.aspose.com/c/imaging) | [Temporary License](https://purchase.aspose.com/temporary-license)
