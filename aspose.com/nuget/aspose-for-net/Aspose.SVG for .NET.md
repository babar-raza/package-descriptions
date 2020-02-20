This .NET on-premise API helps you seamlessly integrate SVG file processing & manipulation functionality into your C#, VB.NET, ASP.NET & other .NET based apps.

## SVG File Processing Features

- Create, read and write SVG format files.
- Convert SVG to other supported file formats.
- DOM Tree manipulation as per official SVG specs.
- Support for content navigation via XPath Query, CSS Selectors, Element and Document Traversal features.
- Support for quality rendering.

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

[Product Page](https://products.aspose.com/svg/net) | [Documentation](https://docs.aspose.com/display/svgnet/Home) | [API Reference](https://apireference.aspose.com/net/svg) | [Code Examples](https://github.com/aspose-svg/Aspose.SVG-for-.NET) | [Blog](https://blog.aspose.com/category/svg/) | [Free Support](https://forum.aspose.com/c/svg) |  [Temporary License](https://purchase.aspose.com/temporary-license)
