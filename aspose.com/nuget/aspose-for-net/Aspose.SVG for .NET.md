# Process & Manipulate SVG via .NET API

This .NET on-premise API helps you [seamlessly integrate SVG file processing & manipulation](https://products.aspose.com/svg/net) functionality into your C#, VB.NET, ASP.NET & other .NET based apps.

## SVG File Processing Features

- [Create, read](https://docs.aspose.com/display/svgnet/Create+and+Read+SVG+Documents) and [write SVG](https://docs.aspose.com/display/svgnet/Save+SVG+Files) format files.
- [Convert SVG](https://docs.aspose.com/display/svgnet/How+to+Convert+SVG+Files) to other [supported file formats](https://docs.aspose.com/display/svgnet/Supported+File+Formats).
- DOM Tree manipulation as per official SVG specs.
- Support for content navigation via [XPath Query](https://docs.aspose.com/display/svgnet/Traverse+SVG+DOM#TraverseSVGDOM-UsingXPathQuery), [CSS Selectors](https://docs.aspose.com/display/svgnet/Traverse+SVG+DOM#TraverseSVGDOM-UsingCSSSelector), Element and Document Traversal features.
- Support for quality rendering.

## Added APIs in Version 20.5

- Added new signatures to the Document creation methods. Now you can specify a base URL using the `Aspose.Svg.Url class`.
- Added new service `IRuntimeService`, which provides `JavaScriptTimeout` property, that allows you to specify JavaScript processing timeout. It can be used to speed up the rendering process or to stop the execution of infinite JavaScripts.
- We have also added the empty constructor to the `ImageSaveOptions` class.

## Enhancements in Version 20.5

- Updated the processing of many `CSS` properties according to the latest documentation.
- Made some usability improvements, like, clarified the URL parsing exceptions and added new signatures to the Document creation methods.

For the detailed notes, please visit [Aspose.SVG for .NET 20.5 Release Notes](https://docs.aspose.com/display/svgnet/Aspose.SVG+for+.NET+20.5+Release+Notes).

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

[Product Page](https://products.aspose.com/svg/net) | [Docs](https://docs.aspose.com/display/svgnet/Home) | [API Reference](https://apireference.aspose.com/svg/net) | [Examples](https://github.com/aspose-svg/Aspose.SVG-for-.NET) | [Blog](https://blog.aspose.com/category/svg/) | [Free Support](https://forum.aspose.com/c/svg) |  [Temporary License](https://purchase.aspose.com/temporary-license)
