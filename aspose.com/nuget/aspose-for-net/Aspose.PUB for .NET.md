# Process PUB files via .NET API

[Aspose.PUB for .NET](https://products.aspose.com/pub/net) is a simple API that allows to read & convert Microsoft Publisher® (PUB) files to PDF format. It also provides easy to understand interfaces to edit metadata of PUB files.

## PUB File Processing Features

- Read Microsoft Publisher [(PUB) files for conversion to PDF](https://docs.aspose.com/pub/net/pub-to-pdf/) format.
- [Read & write metadata of PUB files](https://docs.aspose.com/pub/net/programming-with-documents/) via API.

## New Features in Version 20.4

- Availbility of vector graphics support.
- Create static shape entities.
- Supports vector graphics in the converter.

For the detailed notes, please visit [Aspose.PUB for .NET 20.4 Release Notes](https://docs.aspose.com/pub/net/aspose-pub-for-net-20-4-release-notes/).

## Read PUB Files

**Microsoft Publisher:** PUB

## Save PUB As

**Fixed Layout:** PDF

## Platform Independence

You can use Aspose.PUB for .NET to develop applications in any development environment that targets the .NET platform including .NET Framework, .NET Core & Mono to develop both 32-bit & 64-bit applications.

## Getting Started with Aspose.PUB for .NET

Are you ready to give Aspose.PUB for .NET a try? Simply execute `Install-Package Aspose.PUB` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.PUB for .NET and want to upgrade the version, please execute `Update-Package Aspose.PUB` to get the latest version.

## Convert a Microsoft Publisher File to PDF using C# Code

You can execute below code snippet to see how Aspose.PDF API performs in your own development environment or check the [GitHub Repository](https://github.com/aspose-pub/Aspose.PUB-for-.NET) for other common usage scenarios.

```csharp
var parser = PubFactory.CreateParser(dir + "template.pub");
var doc = parser.Parse();
PubFactory.CreatePdfConvertor().ConvertToPdf(doc, dir + "output.pdf");
```

## Edit Metadata of Microsoft Publisher Files

Following C# code sample shows how to edit the metadata of a Microsoft Publisher file:

```csharp
IPubParser parser = PubFactory.CreateParser(dir + "template.pub");
Document document = parser.Parse();

document.DocumentSummaryInfo.SetCategory("category");
document.DocumentSummaryInfo.SetCompany("company");
document.DocumentSummaryInfo.SetLanguage("language");

document.SummaryInfo.SetComments("comments");
document.SummaryInfo.SetKeywords("keywords");
document.SummaryInfo.SetLastAuthor("last author");
document.SummaryInfo.SetTitle("title");
document.SummaryInfo.SetSubject("subject");
```

## Limitations

At the moment API lacks the support to convert images of PUB file to PDF file. So such images wont show up in the resultant output PDF file. This feature is in our plan to be released with future release.

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/pub/net) | [Docs](https://docs.aspose.com/pub/net/) | [API Reference](https://apireference.aspose.com/pub/net) | [Examples](https://github.com/aspose-pub/Aspose.PUB-for-.NET) | [Blog](https://blog.aspose.com/category/pub/) | [Free Support](https://forum.aspose.com/c/pub) | [Temporary License](https://purchase.aspose.com/temporary-license)
