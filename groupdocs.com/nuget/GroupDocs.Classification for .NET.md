# .NET API for Data Classification

A .NET component that enables your applications to [analyze text and files as well as classify](https://products.groupdocs.com/classification/net) them based on [IAB-2 and Documents taxonomies](https://docs.groupdocs.com/display/classificationnet/Taxonomies).

## Classification Processing Features

- Support for [IAB-2](https://docs.groupdocs.com/display/classificationnet/Classify+document+by+path) and [Documents](https://docs.groupdocs.com/display/classificationnet/Classify+document+from+stream) taxonomies.
- Select the number of results to return.
- Select precision/recall balance for Documents taxonomy.
- Classify document from stream.

## New Features in Version 20.3

- Sentiment Classification (Analysis) is added.
- Raw text classification speed has been increased several times.

For the detailed list, please visit [GroupDocs.Classification for .NET 20.3 Release Notes](https://docs.groupdocs.com/display/classificationnet/GroupDocs.Classification+for+.NET+20.3+Release+Notes).
  
## Other File Formats

**OpenOffice:** ODT, OTT
**Fixed Layout:** PDF
**Other:** TXT

## Supported Platforms

The machine that GroupDocs.Classification for .NET runs on doesn't need to have Adobe Acrobat, Microsoft Office or OpenOffice installed: GroupDocs.Classification for .NET has their own document processing engine.
**Microsoft Windows:** Microsoft Windows Desktop (x64) (XP & up), Microsoft Windows Server (x64) (2000 & up), Windows Azure
**Mac OS:** Mac OS X x64 (10.12+)
**Linux:** Linux x64 ( 6, 7 ,27, 9, 8.7+, 18.04, 16.04, 14.04, 18, 17, 42.3+, 12 SP2+)
**Memory Requirements:** 3GB RAM
**Development Environments:** Microsoft Visual Studio (2013, 2015, 2017, 2019)
**Supported Frameworks:** .NET Framework 4.7 or later, .NET Core 2.0 or later

## Getting Started with GroupDocs.Classification for .NET

Are you ready to give GroupDocs.Classification for .NET a try? Simply execute `Install-Package GroupDocs.Classification` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Classification assembly in your project. If you already have GroupDocs.Classification for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Classification` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-classification/GroupDocs.Classification-for-.NET) for other common usage scenarios.

## Classify PDF document by path with IAB-2 taxonomy via C# Code

```csharp
var response = classifier.Classify("document.pdf", ".", 3, Taxonomy.Iab2);
Console.WriteLine(response.BestClassName, response.BestClassProbability);
```

[Product Page](https://products.groupdocs.com/classification/net) | [Documentation](https://docs.groupdocs.com/display/classificationnet) | [Live Demo](https://products.groupdocs.app/classification/family) | [API Reference](https://apireference.groupdocs.com/net/classification) | [Code Samples](https://github.com/groupdocs-classification/GroupDocs.Classification-for-.NET) | [Blog](https://blog.groupdocs.com/category/classification/) | [Free Support](https://forum.groupdocs.com/c/classification) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
