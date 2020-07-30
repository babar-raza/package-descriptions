# Document Viewer .NET API

This robust .NET on-premise [file viewer API](https://products.groupdocs.com/viewer/net) supports rendering of 130+ format types in HTML, image & PDF formats. 90+ formats are supported for auto-detection.

## Document Viewer Processing Features

- View documents by rendering in an HTML, image or PDF format.
- Reuse common resources across several HTML pages.
- Make each HTML page self=sufficient by rendering it with embedded resources.
- Render files in the lossless PNG file format or lossy JPG compressed image format.
- Apply page rotation or change page order when rendering a document to HTML or image formats.
- Apply the specified text as watermark to all pages while being rendered into HTML or image.
- Boost document loading speed to optimize application performance via caching.
- Perform document text extract for PNG and JPG formats.
- Fetch basic information about source documents.
- Extract list of folders contained in an archive.
- Fetch list of layers and layouts from a CAD drawing.
- Get list of folders contained in an Outlook data file.
- Extract information about PDF document printing restrictions.
- Fetch start and end dates of a project from MS Project file.
- Minify HTML & CSS to improve the rendering process.
- Render to responsive HTML.
- Apply watermark on the output pages of HTML, image or PDF files.
- Render documents with comments, notes, and custom fonts.
- Replace missing fonts while rendering.

## New Featrues & Enhancements in Version 20.7

- Ability to render text files into single `HTML` page.
- Support of setting margins when converting `HTML` files.
- Added feature to identify if the file is Password Protected.
- Added Apple numbers (`.numbers`) file-format support.
- Added Excel 2003 XML file (SpreadsheetML) (`.xml`) file-format support.
- Added WinRAR Compressed Archive (`.rar`) file-format support.
- Ability to split up archives into multiple pages.

For the detailed notes, please visit [GroupDocs.Viewer for .NET 20.7 Release Notes](https://docs.groupdocs.com/viewer/net/groupdocs-viewer-for-net-20-7-release-notes/).

## HTML, Image, PDF Rendering Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX\
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX, XLT, XLTX, XLAM\
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POT, POTM, POTX\
**Microsoft Visio:** VDW, VDX, VSD, VSDM, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX\
**Microsoft Project:** MPP, MPT, MPX\
**Microsoft OneNote:** ONE\
**OpenOffice:** ODG, OTG, OXPS, ODP, OTP, ODS, OTS, ODT, OTT, OXPS\
**AutoCAD:** DGN, DWF, DWT, DWG, DXF\
**CorelDraw:** CDR\
**Adobe Photoshop:** PSD\
**Programming:** CS, VB, AS, AS3, ASM, BAT, C, CC, CMAKE, CPP, CSS, CXX, ERB, GROOVY, H, HAML, HH, JAVA, JS, JSON, LESS, LOG, M, MAKE, MD, ML, MM, PHP, PL, PROPERTIES, PY, RB, RST, SASS, SCALA, SCM, SCRIPT, SH, SML, SQL, VIM, YAML\
**Image:** GIF, ICO, JP2, JPF, JPX, JPM, J2C, J2K, JPC, JPG, JPEG, SVG, TIF, TIFF\
**Markup:** HTML, MHT, MHTML, MD\
**Portable:** PDF\
**Archive:** TAR, ZIP, BZ2\
**Email:** EML, EMLX, MSG, OST, PST\
**Metafile:** CGM, EMF, WMF\
**Other:** IFC, STL, PS, XPS, TEX, SXC, DJVU, DNG, DIB, EPS

## Supported Formats for Auto Detection

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX\
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX, XLTX, XLAM\
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POT, POTM, POTX\
**Microsoft Visio:** VDW, VDX, VSD, VSDM, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX\
**Microsoft Project:** MPP, MPT, MPX\
**Microsoft OneNote:** ONE\
**OpenOffice:** ODG, OTG, OXPS, ODP, OTP, ODS, OTS, ODT, OTT, OXPS\
**AutoCAD:** DGN, DWF, DWT, DWG, DXF\
**CorelDraw:** CDR\
**Adobe Photoshop:** PSD\
**Programming:** CS, VB\
**Image:** GIF, ICO, JP2, JPF, JPX, JPM, J2C, J2K, JPC, JPG, JPEG, SVG, TIF, TIFF\
**Markup:** HTML, MD\
**Portable:** PDF\
**Archive:** TAR, ZIP, BZ2\
**Email:** EML, EMLX, MSG, OST, PST\
**Metafile:** CGM, EMF, WMF\
**Other:** IFC, STL, PS, XPS, TEX, SXC, DJVU, DNG, DIB, EPS

## Platform Independence

GroupDocs.Viewer for .NET does not require any external software or third party tool to be installed. GroupDocs.Viewer for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure\
**Mac OS:** Mac OS X\
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)\
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.\
**Supported Frameworks:** GroupDocs.Conversion for .NET supports .NET and Mono frameworks.

## Getting Started with GroupDocs.Viewer for .NET

Are you ready to give GroupDocs.Viewer for .NET a try? Simply execute `Install-Package GroupDocs.Viewer` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Viewer assembly in your project. If you already have GroupDocs.Viewer for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Viewer` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-viewer/GroupDocs.Viewer-for-.NET) for other common usage scenarios.

## Use C# Code to Render All Layouts of a DWG CAD Drawing

```csharp
string outputDirectory = @"C:\output\RenderAllLayouts";
string pageFilePathFormat = Path.Combine(outputDirectory, "page_{0}.html");
using (Viewer viewer = new Viewer("with_layers_and_layouts.dwg"))
{
   HtmlViewOptions options = HtmlViewOptions.ForEmbeddedResources(pageFilePathFormat);
   options.CadOptions.RenderLayouts = true;
   viewer.View(options);
}
```

## Apply Password to PDF File via C# Code

```csharp
string outputDirectory = @"C:\output\ProtectPdfDocument";
string filePath = Path.Combine(outputDirectory, "output.pdf");
using (Viewer viewer = new Viewer("sample.docx"))
{
    // set PDF file security
    Security security = new Security();
    security.DocumentOpenPassword = "o123";
    security.PermissionsPassword = "p123";
    security.Permissions = Permissions.AllowAll ^ Permissions.DenyPrinting;

    PdfViewOptions options = new PdfViewOptions(filePath);
    options.Security = security;

    viewer.View(options);
}
```

[Product Page](https://products.groupdocs.com/viewer/net) | [Documentation](https://docs.groupdocs.com/viewer/net/) | [Demo](https://products.groupdocs.app/viewer/family) | [API Reference](https://apireference.groupdocs.com/net/viewer) | [Examples](https://github.com/groupdocs-viewer/GroupDocs.Viewer-for-.NET) | [Blog](https://blog.groupdocs.com/category/viewer/) | [Free Support](https://forum.groupdocs.com/c/viewer) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
