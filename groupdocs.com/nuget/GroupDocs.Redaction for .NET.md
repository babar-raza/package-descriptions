# .NET API to Redact Documents

This .NET component makes it very easy to [remove classified or sensitive data](https://products.groupdocs.com/redaction/net) from documents via your own .NET apps. Multiple redaction types are supported.

## Document Redaction Processing Features

- Remove classified or sensitive information from the documents.
- Remove document metadata and annotations.
- Make a rasterized PDF version of the redacted document for better security.
- Keep the document in its original format after the redaction process.
- Set the redaction scope to a specific worksheet or column.
- Apply multiple redaction in a single call.
- Modify compliance level from PDF/A-1b to PDF/A-1a during rasterizing PDF.

## Enhancements in the Version 20.2

- Support for metadata redaction of raster images (i.e. ability to edit or erase image metadata).

For the detailed notes, please visit [GroupDocs.Redaction for .NET 20.2 Release Notes](https://docs.groupdocs.com/display/redactionnet/GroupDocs.Redaction+for+.NET+20.2+Release+Notes).

## Document Body & Metadata Redaction Formats

**Microsoft Word:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, RTF
**Microsoft Excel:** XLSX, XLSM, XLTX, XLTM, XLS, XLT, CSV
**Microsoft PowerPoint:** PPT, PPTX, PPSX, POT, PPS, PPTM, PPSM, POTM
**Image:** JPEG, TIF, TIFF, PNG, BMP, GIF
**Fixed Layout:** PDF

## Annotations (Comments) Redaction Formats

**Microsoft Word:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, RTF
**Microsoft Excel:** XLSX, XLSM, XLTX, XLTM, XLS, XLT, CSV
**Microsoft PowerPoint:** PPT, PPTX, PPSX, POT, PPS, PPTM, PPSM, POTM
**Fixed Layout:** PDF

## Supported Redaction Types

**Text:** Replace or hide a textual area within the document body with a colored block.
**Metadata:** Replace metadata values with empty ones or redact metadata values.
**Annotation:** Remove annotations from the document or redact their content.
**Image:** Replace specific area of an image with a colored box.

## Platform Independence

GroupDocs.Redaction for .NET does not require any external software or third party tool to be installed. GroupDocs.Redaction for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure
**Mac OS:** Mac OS X
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET and Mono frameworks.

## Getting Started with GroupDocs.Redaction for .NET

Are you ready to give GroupDocs.Redaction for .NET a try? Simply execute `Install-Package GroupDocs.Redaction` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Redaction assembly in your project. If you already have GroupDocs.Redaction for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Redaction` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-.NET) for other common usage scenarios.

## Perform Exact Phrase Case Sensitive Redaction via C# Code

```csharp
// For complete examples and data files, please go to https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-.NET
using (Redactor redactor = new Redactor(@"sample.docx"))
{
  redactor.Apply(new ExactPhraseRedaction("John Doe", true /*isCaseSensitive*/, new ReplacementOptions("[personal]")));
  redactor.Save();
}
```

## Use C# to Redact Specific String from Annotations

```csharp
using (Redactor redactor = new Redactor(@"C:\test.pdf"))
{
   redactor.Apply(new AnnotationRedaction("(?im:john)", "[redacted]"));

   redactor.Save()
}
```

[Product Page](https://products.groupdocs.com/redaction/net) | [Documentation](https://docs.groupdocs.com/display/redactionnet/Home) | [API Reference](https://apireference.groupdocs.com/net/redaction) | [Code Samples](https://github.com/groupdocs-redaction/GroupDocs.Redaction-for-.NET) | [Blog](https://blog.groupdocs.com/category/redaction/) | [Free Support](https://forum.groupdocs.com/c/redaction) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
