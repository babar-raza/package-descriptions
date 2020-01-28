A standalone C# class library that developers can use to embed Microsoft Visio® file creation, manipulation & processing capabilities to their own C#, VB.NET or other .NET applications.

Aspose.Diagram for .NET API is a comprehensive solution for all Microsoft Visio manipulation requirements while allowing the .NET applications to read, write, export and process Microsoft Visio diagrams. It supports all Visio objects such as shapes, pages, images, shape masters, Visio stencils, text, layers, header, footers, user-defined cells, hyperlinks, file protection, font operations, printing, geometries, SQL Server data sources, text boxes, and comments. 

Aspose.Diagram for .NET can also be used to apply protection to the Microsoft Visio drawings by locking backgrounds,  stencils (master) as well as  shapes and styles to avoid any accidental amendments.

## Visio File Processing Features
-  Create Microsoft Visio diagrams from scratch via API.
-  Read or write Microsoft Visio drawings with Automation.
-  Export Visio diagrams to various popular formats including PDF, images, HTML and more.
-  Print Visio diagrams on phlysical printer or on a server using XpsPrint API.
-  Access Visio diagram properties.
-  Protect Visio diagrams via applying locks on various levels.
-  Manipulate the embedded OLE objects in the Visio diagrams.
-  Insert ActiveX control within the Visio file.
-  Customize the gradient of a Visio shape.

## Read & Write Visio Files
**Microsoft Visio:** VSDX, VSX, VTX, VDX, VSSX, VSTX, VSDM, VSSM, VSTM

## Save Visio Diagrams As
**Fixed Layout:** PDF, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG, EMF
**Web:** HTML
**Other:** XAML, SWF

## Read Visio Formats
**Microsoft Visio:** VDW, VSD, VSS, VST

## Platform Independence
You can use Aspose.Diagram for .NET to build any type of a 32-bit or 64-bit .NET application including ASP.NET, WCF, WinForms, UWP, .NET Standard, .NET Core etc. You can also use Aspose.Diagram for .NET to build applications with Mono.

## Getting Started with Aspose.Diagram for .NET
Are you ready to give Aspose.Diagram for .NET a try? Simply execute `Install-Package Aspose.Diagram` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Diagram for .NET and want to upgrade the version, please execute `Update-Package Aspose.Diagram` to get the latest version.

### Load a VSS Template to Create a Visio Diagram with C#
You can execute below code snippet to see how Aspose.Diagram API performs against your own samples or check the [GitHub Repository](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET) for other common usage scenarios. 

```csharp
// create a new diagram
var diagram = new Diagram(dataDir + "template.vss");
// add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
var shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));
// add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));
// save the diagram in VDX format
diagram.Save(dir + "output.vdx", SaveFileFormat.VDX);
```

### Retrieve Layers of a Visio VSDX Diagram
Aspose.Diagram for .NET allows .NET applications to work with layers of Visio drawings. The following C# code example shows how to fetch all the layers of a VSDX file.
```csharp
// load source Visio diagram
var diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get diagram page
var page = diagram.Pages.GetPage("Page-1");
// iterate through the layers and print properties
foreach (Layer layer in page.PageSheet.Layers)
{
    Console.WriteLine("Name: " + layer.Name.Value);
    Console.WriteLine("Visibility: " + layer.Visible.Value);
    Console.WriteLine("Status: " + layer.Status.Value);
}
```

[Product Page](https://products.aspose.com/diagram/net) | [Documentation](https://docs.aspose.com/display/diagramnet/Home) | [API Reference](https://apireference.aspose.com/net/diagram) | [Code Examples](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET) | [Blog](https://blog.aspose.com/category/diagram/) | [Free Support](https://forum.aspose.com/c/diagram) |  [Temporary License](https://purchase.aspose.com/temporary-license)