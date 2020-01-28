A standalone C++ class library to create, read, write, edit & convert Microsoft PowerPoint® presentations without needing PowerPoint or Office Automation.

Aspose.Slides' object model gives complete control over presentation elements such as slides, shapes, charts, multimedia, embedded objects, tables, text, transitions and formatting. Developers can directly use this object model to create complex PowerPoint File Processing application that can dynamically generate presentation files, manipulate slides, apply transitions or animation effects, convert presentations to other popular formats as well as render slides to images for easy viewing.

## Presentation Processing Features
- Generate presentations from scratch via API.
- Load PowerPoint presentations from various sources for editing or just examining. 
- High-fidelity rendering of slides to C++ supported & SVG images formats.
- Control access to presentations & slides or certain objects via advanced security features.
- Copy or clone slides to the same or another presentation.
- Create shapes such as rectangles, lines, poly-lines & ellipses on-the-fly.
- Copy or clone slides for the same or different presentation.
    

## Read & Write PowerPoint Files
**Microsoft PowerPoint:** PPT, POT, PPS, PPTX, POTX, PPSX, PPTM, PPSM, POTM
**OpenOffice:** ODP
**Open Document:** OTP
**Other:** TIFF, EMF, XML

## Save Presentation As
**Fixed Layout:** PDF, XPS
**Images:** JPEG, PNG, GIF, BMP, SVG
**Web:** HTML


## Platform Independence
Aspose.Slides for C++ is a native C++ library that supports 64-bit operating systems, such as, Windows (XP and onward) & Linux (Ubuntu 16.04 or later). The supported platforms include Windows (Microsoft Visual C++)  & Linux (Clang). 


## Getting Started with Aspose.Slides for C++
Let's give Aspose.Slides for C++ a try! Simply execute `Install-Package Aspose.Slides.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Slides for C++ and want to upgrade the version, please execute `Update-Package Aspose.Slides.Cpp` to get the latest version.

Try executing below code snippet to see how Aspose.Slides for C++ performs in your environment or check the [GitHub Repository](https://github.com/aspose-slides/Aspose.Slides-for-C) for other common usage scenarios. 

### Create PPTX Presentation using C++
```c++
// instantiate Presentation class that represents PPTX file
SharedPtr<Presentation> pres = MakeObject<Presentation>();
SharedPtr<ISlide> slide = pres->get_Slides()->idx_get(0);

// add an autoshape of type line
slide->get_Shapes()->AddAutoShape(Aspose::Slides::ShapeType::Line, 50.0, 150.0, 300.0, 0.0);
// save presentation
pres->Save(u"output.pptx", Aspose::Slides::Export::SaveFormat::Pptx);
```

### Convert PPTX to PDF
The following code sample demonstrates the conversion of Microsoft PowerPoint PPTX presentation to PDF format with C++.
```c++
// instantiate Presentation class that represents PPTX file
SharedPtr<Presentation> pres = MakeObject<Presentation>(u"template.pptx");
pres->Save(u"output.pdf", Aspose::Slides::Export::SaveFormat::Pdf);
```

[Product Page](https://products.aspose.com/slides/cpp) | [Documentation](https://docs.aspose.com/display/slidescpp/Home) | [API Reference](https://apireference.aspose.com/cpp/slides) | [Code Examples](https://github.com/aspose-slides/Aspose.Slides-for-C) | [Blog](https://blog.aspose.com/category/slides/) | [Free Support](https://forum.aspose.com/c/slides) |  [Temporary License](https://purchase.aspose.com/temporary-license)