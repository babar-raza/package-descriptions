# Document Parser .NET API

This text parser on-premise API works well to [search & extract formatted text](https://products.groupdocs.com/parser/net) as well as the raw text from a variety of documents of [supported file formats](https://docs.groupdocs.com/parser/net/supported-document-formats/).

## Document Parser Processing Features

- Parse documents by user-defined templates.
- Extract plain and structured text.
- Extract text areas with coordinates, text styles and other information.
- Search text by a keyword or regular expression; extract text around that word.
- Extract HTML or Markdown (MD) formatted text for a fast preview.
- Increase performance by extracting raw text.
- Extract formatted text, metadata, images, containers, and attachments.
- Extract table of contents for some supported document formats.
- Parse form data from PDF documents.

## New Features & Enhancements in Version 20.6.1

- Fixed the Misspelling in `GetHyperlinks` method name.

For the detailed notes, please visit [GroupDocs.Parser for .NET 20.6.1 Release Notes](https://docs.groupdocs.com/parser/net/groupdocs-parser-for-net-20-6-1-release-notes/).

## Parse Document by Template

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF, TXT\
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS\
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP\
**Portable:** PDF

## Extract Text (Accurate)

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF, TXT\
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS\
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP\
**Email:** EML, EMLX, MSG\
**Markup:** HTML, XHTML, MHTML, MD, XML\
**eBooks:** CHM, EPUB, FB2\
**Portable:** PDF\
**Notes:** ONE\
**Databases:** Databases are supported via ADO.NET. To work with the corresponding database format install its database provider.

## Extract Text (Raw)

**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, XLA, XLAM\
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM\
**Portable:** PDF

## Extract Structured Text and Formatted Text

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF\
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLTX, XLTM, XLA, XLAM\
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP\
**Email:** EML, EMLX, MSG\
**Markup:** MD (Formatted Text is Not supported)\
**eBooks:** CHM, EPUB, FB2

## Extract Text Areas

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF\
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, XLA, XLAM, NUMBERS\
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP\
**Portable:** PDF

## Extract Metadata

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF\
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, XLA, XLAM\
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP\
**Email:** EML, EMLX, MSG\
**eBooks:** EPUB, FB2\
**Portable:** PDF

## Extract Images

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF\
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, XLA, XLAM, NUMBERS\
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP\
**Email:** EML, EMLX, MSG\
**Portable:** PDF\
**Archive:** ZIP

## Extract Containers and Attachments

**Email:** PST, OST, EML, EMLX, MSG\
**Portable:** PDF\
**Archive:** ZIP

## Parse Form Data

**Portable:** PDF

## Extract Table of Contents

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF\
**eBooks:** CHM, EPUB\
**Portable:** PDF\
**Databases:** Databases are supported via ADO.NET. To work with the corresponding database format install its database provider.

## Platform Independence

GroupDocs.Parser for .NET does not require any external software or third party tool to be installed. GroupDocs.Parser for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure\
**Mac OS:** Mac OS X\
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)\
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.\
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET and Mono frameworks.

## Getting Started with GroupDocs.Parser for .NET

Are you ready to give GroupDocs.Parser for .NET a try? Simply execute `Install-Package GroupDocs.Parser` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Parser assembly in your project. If you already have GroupDocs.Parser for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Parser` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-parser/GroupDocs.Parser-for-.NET) for other common usage scenarios.

## Use C# Code to Extract Data from Database

```csharp
string connectionString = string.Format("Provider=System.Data.Sqlite;Data Source={0};Version=3;", "database.db");
// create an instance of Parser class to extract tables from the database
// as filePath connection parameters are passed; LoadOptions is set to Database file format
using (Parser parser = new Parser(connectionString, new LoadOptions(FileFormat.Database)))
{
    // check if text extraction is supported
    if (!parser.Features.Text)
    {
        Console.WriteLine("Text extraction isn't supported.");
        return;
    }
    // check if toc extraction is supported
    if (!parser.Features.Toc)
    {
        Console.WriteLine("Toc extraction isn't supported.");
        return;
    }
    // get a list of tables
    IEnumerable<TocItem> toc = parser.GetToc();
    // iterate over tables
    foreach (TocItem i in toc)
    {
        // print the table name
        Console.WriteLine(i.Text);
        // extract a table content as a text
        using (TextReader reader = parser.GetText(i.PageIndex.Value))
        {
            Console.WriteLine(reader.ReadToEnd());
        }
    }
}
```

## Extract all Images and Save them in PNG Format via C# Code

```csharp
// create an instance of Parser class
using (Parser parser = new Parser(Constants.SampleZip))
{
    // extract images from document
    IEnumerable<PageImageArea> images = parser.GetImages();
    // check if images extraction is supported
    if (images == null)
    {
        Console.WriteLine("Page images extraction isn't supported");
        return;
    }
    // create the options to save images in PNG format
    ImageOptions options = new ImageOptions(ImageFormat.Png);
    int imageNumber = 0;
    // iterate over images
    foreach (PageImageArea image in images)
    {
        // save the image to the png file
        image.Save(imageNumber.ToString() + ".png", options);
        imageNumber++;
    }
}
```

[Product Page](https://products.groupdocs.com/parser/net) | [Documentation](https://docs.groupdocs.com/parser/net/) | [Demo](https://products.groupdocs.app/parser/family) | [API Reference](https://apireference.groupdocs.com/net/parser) | [Examples](https://github.com/groupdocs-parser/GroupDocs.Parser-for-.NET) | [Blog](https://blog.groupdocs.com/category/parser/) | [Free Support](https://forum.groupdocs.com/c/parser) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
