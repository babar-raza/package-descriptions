# C++ Class Library to Process Presentations

A [standalone C++ class library](https://products.aspose.com/slides/cpp) to create, read, write, edit & convert Microsoft PowerPoint® presentations without needing PowerPoint or Office Automation.

## Presentation Processing Features

- Create, open and work with presentations without Microsoft PowerPoint.
- [Convert presentation](https://docs.aspose.com/slides/cpp/converting-a-presentation/) to any of the [supported file formats](https://docs.aspose.com/slides/cpp/supported-file-formats/).
- Adding, formatting, and manipulating charts, shapes, slides, SmartArt, [tables](https://docs.aspose.com/slides/cpp/adding-updating-and-manipulating-tables/), and text in presentations.

## New Features & Enhancements in Version 20.7

- Ability to convert Mathematical Text to `MathML` Format.
- Support to extract equation from `PPT` to `LaTeX`.
- Support for rotation options for line shape.
- Ability to render `SVG` image as `PNG` image in the generated `PDF`.
- Automatic wrapped text exported with line breaks in `PDF`.
- Improved thumbnails rendering quality.

For the detailed notes, please visit [Aspose.Slides for C++ 20.7 Release Notes](https://docs.aspose.com/slides/cpp/aspose-slides-for-cpp-20-7-release-notes/).

## Read & Write PowerPoint Files

**Microsoft PowerPoint:** PPT, POT, PPS, PPTX, POTX, PPSX, PPTM, PPSM, POTM
**OpenOffice:** ODP, FODP
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

## Create PPTX Presentation using C++

Try executing below code snippet to see how Aspose.Slides for C++ performs in your environment or check the [GitHub Repository](https://github.com/aspose-slides/Aspose.Slides-for-C) for other common usage scenarios. 

```c++
// instantiate Presentation class that represents PPTX file
SharedPtr<Presentation> pres = MakeObject<Presentation>();
SharedPtr<ISlide> slide = pres->get_Slides()->idx_get(0);

// add an autoshape of type line
slide->get_Shapes()->AddAutoShape(Aspose::Slides::ShapeType::Line, 50.0, 150.0, 300.0, 0.0);
// save presentation
pres->Save(u"output.pptx", Aspose::Slides::Export::SaveFormat::Pptx);
```

## Convert PPTX to PDF using C++

The following code sample demonstrates the conversion of Microsoft PowerPoint PPTX presentation to PDF format with C++:

```c++
// instantiate Presentation class that represents PPTX file
SharedPtr<Presentation> pres = MakeObject<Presentation>(u"template.pptx");
pres->Save(u"output.pdf", Aspose::Slides::Export::SaveFormat::Pdf);
```

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/slides/cpp) | [Docs](https://docs.aspose.com/slides/cpp/) | [Demos](https://products.aspose.app/slides/family) | [API Reference](https://apireference.aspose.com/slides/cpp) | [Examples](https://github.com/aspose-slides/Aspose.Slides-for-C) | [Blog](https://blog.aspose.com/category/slides/) | [Free Support](https://forum.aspose.com/c/slides) | [Temporary License](https://purchase.aspose.com/temporary-license)
