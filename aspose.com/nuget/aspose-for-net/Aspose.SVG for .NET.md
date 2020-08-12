# Process & Manipulate SVG via .NET API

This .NET on-premise API helps you [seamlessly integrate SVG file processing & manipulation](https://products.aspose.com/svg/net) functionality into your C#, VB.NET, ASP.NET & other .NET based apps.

## SVG File Processing Features

- [Create, read](https://docs.aspose.com/svg/net/create-and-read-svg-documents/) and [write SVG](https://docs.aspose.com/svg/net/save-svg-files/) format files.
- [Convert SVG](https://docs.aspose.com/svg/net/how-to-convert-svg-files/) to other [supported file formats](https://docs.aspose.com/svg/net/supported-file-formats/).
- DOM Tree manipulation as per official SVG specs.
- Support for content navigation via [XPath Query](https://docs.aspose.com/svg/net/traverse-svg-dom/), CSS Selectors, Element and Document Traversal features.
- Support for quality rendering.

## New Features & Enhancements in Version 20.7

- Added support for the *comp-op* property with the following list of values: `clear`, `src`, `dst`, `src-over`, `dst-over`, `src-in`, `dst-in`, `src-out`, `dst-out`, `src-atop`, `dst-atop`, `xor`, `plus`, `overlay`, `color-dodge`, `color-burn`, `hard-light`, `soft-light`, `difference`, `exclusion`.
- The algorithm processing the type of the *discrete transfer function* has been fixed;
- Improved precision of the `GetBBox` method.
- Added new signatures to the `SVGFEBlendElement` class

For the detailed notes, please visit [Aspose.SVG for .NET 20.7 Release Notes](https://docs.aspose.com/svg/net/aspose-svg-for-net-20-7-release-notes/).

## Read Supported Formats

SVG

## Save SVG As

**Fixed Layout:** PDF, XPS
**Image:** TIFF, BMP, PNG, JPEG, GIF

## Platform Independence

Any operating system that can install Mono (.NET 4.0 Framework support) or use .NET core can use Aspose.SVG for .NET. This includes Windows, Linux, and MacOS.

## Getting Started with Aspose.SVG for .NET

Are you ready to give Aspose.SVG for .NET a try? Simply execute `Install-Package Aspose.SVG` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.SVG for .NET and want to upgrade the version, please execute `Update-Package Aspose.SVG` to get the latest version.

## Use C# to Convert SVG to PNG format

```csharp
string dataDir = RunExamples.GetDataDir_Data();
using (var document = new SVGDocument(Path.Combine(dataDir, "sourcefile.svg"))){
    using (var device = new ImageDevice(new ImageRenderingOptions(ImageFormat.Png), dataDir + "targetfile.png")){
        document.RenderTo(device);
    }
}
```

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/svg/net) | [Docs](https://docs.aspose.com/svg/net/) | [API Reference](https://apireference.aspose.com/svg/net) | [Examples](https://github.com/aspose-svg/Aspose.SVG-for-.NET) | [Blog](https://blog.aspose.com/category/svg/) | [Free Support](https://forum.aspose.com/c/svg) | [Temporary License](https://purchase.aspose.com/temporary-license)
