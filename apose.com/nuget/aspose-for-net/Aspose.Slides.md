A standalone class library to read, write, manipulate & convert Microsoft PowerPoint® presentations without installing PowerPoint or requiring Office Automation.

Aspose.Slides' object model gives complete control over presentation elements such as slides, shapes, charts, multimedia, embedded objects, tables, text, transitions and formatting. Developers can directly use this object model to create complex PowerPoint File Processing application that can dynamically generate presentation files, manipulate slides, apply transitions or animation effects, convert presentations to other popular formats as well as render slides to images for easy viewing.

## Presentation Processing Features
- Create presentations from scratch via API or templates & data.
- Load presentation files from various sources for editing or just examining.
- High-fidelity rendering of presentation or slides to fixed-layout & images formats.
- Control access to presentations & slides or certain objects via advanced security features.
- Create shapes such as rectangles, lines, poly-lines & ellipses on-the-fly.
- Copy or clone slides for the same or different presentation.
- Avalability of 24 pre-defined textures & 48 patterns for quick styling.

## Read & Write Presentations
**Microsoft PowerPoint:** PPT, PPTX, PPS, POT, PPSX, PPTM, PPSM, POTX, POTM
**OpenOffice:** ODP

## Save Presentations As
**Fixed Layout:** PDF, PDF/A, XPS
**Image:** JPEG, PNG, BMP, TIFF, GIF, SVG
**Web:** HTML

## Platform Independence
You can use Aspose.Slides for .NET to build any type of a 32-bit or 64-bit .NET application including ASP.NET, WCF & WinForms as well as via COM Interop from ASP, Perl, PHP and Python. Aspose.Slides for .NET works with Mono, on various flavors of Linux and on Mac OS X.

## Getting Started with Aspose.Slides for .NET
Let's give Aspose.Slides for .NET a try! Simply execute `Install-Package Aspose.Slides.NET` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Slides for .NET and want to upgrade the version, please execute `Update-Package Aspose.Slides.NET` to get the latest version.

### Create a PPTX Presentation from Scratch with C#
You can execute below code snippet to see how Aspose.Slides API performs in your environment or check the [GitHub Repository](https://github.com/aspose-slides/Aspose.Slides-for-.NET) for other common usage scenarios. 

```csharp
// instantiate a Presentation object that represents a presentation file
using (Presentation presentation = new Presentation())
{
    // get the first slide
    ISlide slide = presentation.Slides[0];
    
    // add an autoshape of type line
    slide.Shapes.AddAutoShape(ShapeType.Line, 50, 150, 300, 0);
    presentation.Save(dir + "output.pptx", SaveFormat.Pptx);
}
```

### Convert Specific Slides to PDF Format using C#
Aspose.Slides for .NET works as an independent rendering engine for presentations and slides with flexability override certain aspects such as converting specific PowerPoint slides to PDF format.
```csharp
// instantiate a Presentation object that represents a presentation file
using (Presentation presentation = new Presentation(dir + "template.pptx"))
{
    // setting array of slides positions
    int[] slides = { 1, 3 };
    // save the presentation to PDF
    presentation.Save(dir + "output.pdf", slides, SaveFormat.Pdf);
}
```
[Product Page](https://products.aspose.com/slides/net) | [Documentation](https://docs.aspose.com/display/slidesnet/Home) | [API Reference](https://apireference.aspose.com/net/slides) | [Code Examples](https://github.com/aspose-slides/Aspose.Slides-for-.NET) | [Blog](https://blog.aspose.com/category/slides/) | [Free Support](https://forum.aspose.com/c/slides) | [Temporary License](https://purchase.aspose.com/temporary-license)