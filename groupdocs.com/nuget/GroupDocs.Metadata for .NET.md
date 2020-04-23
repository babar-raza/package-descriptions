# .NET API for Metadata Processing

This .NET API can be consumed to [integrate metadata viewer](https://products.groupdocs.com/metadata/net), editor, reader, writer, and remover operations within your .NET apps.

## Document Metadata Processing Features

- Read, update and remove metadata in a variety of formats.
- Search, update and remove particular metadata properties as per specified predicate.
- Use tags to easily manipulate most common metadata properties in a unified manner.
- Work with password-protected documents.
- Extract information about hidden document pages, digital signatures, user comments, revisions, etc.
- Supports many popular metadata standards, such as, IPTC, XMP, EXIF, Image Resources.
- Manipulate native metadata properties in various formats.
- Extract technical information from images, audio and video files.
- Calculate common document statistics (word count, character count, etc.).
- Detect the format and MIME type of a file by its internal structure.
- Work with various audio tags (ID3, Lyrics, APE).
- Load file from a local disk or a stream.
- Load a file of a specific format or load a password protected file.
- Traverse a whole metadata tree.
- Work with the APEv2, ID3v1, ID3v2, Lyrics & other tags of MP3 metadata.

## New Features in Version 20.4

- Ability to work with *EXIF* metadata in *PNG* images.
- Ability to work with *XMP* metadata in *MP3* files.

## Enhancements in Version 20.4

- Ability to parse most common *EXIF* Makernote metadata formats using the new API.

For the detailed notes, please visit [GroupDocs.Metadata for .NET 20.4 Release Notes](https://docs.groupdocs.com/display/metadatanet/GroupDocs.Metadata+for+.NET+20.4+Release+Notes).

## Read & Write Metadata Formats

**Microsoft Word:** DOC, DOT, DOCX, DOCM, DOTX
**Microsoft Excel:** XLSX, XLSM, XLTM, XLS
**Microsoft PowerPoint:** PPTX, PPTM, PPSX, PPSM, POTX, POTM, PPT, PPS
**Microsoft Visio:** VSD, VDX, VSDX, VSS, VSX
**Microsoft OneNote:** ONE
**Microsoft Project:** MPP
**OpenOffice:** ODS, ODT, OTF, OTC
**Audio:** MP3, WAV
**Video:** AVI, MOV / QT, ASF, FLV
**Email:** EML, MSG, VCF, VCR
**Image:** BMP, GIF, JPG, JPEG, JPE, JP2, PNG, TIFF, DICOM, WEBP
**Archive:** ZIP
**Font:** TTF, TTC
**Metafile:** EMF, WMF
**Adobe Photoshop:** PSD
**AutoCAD:** DWG, DXF
**Portable:** PDF
**eBook:** EPUB, DJVU, DJV
**Other:** TORRENT

## Platform Independence

GroupDocs.Metadata for .NET does not require any external software or third party tool to be installed. GroupDocs.Metadata for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure
**Mac OS:** Mac OS X
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET and Mono frameworks.

## Getting Started with GroupDocs.Metadata for .NET

Are you ready to give GroupDocs.Metadata for .NET a try? Simply execute `Install-Package GroupDocs.Metadata` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Metadata assembly in your project. If you already have GroupDocs.Metadata for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Metadata` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-metadata/GroupDocs.Metadata-for-.NET) for other common usage scenarios.

## Use C# to Remove All Metadata Properties from a File

```csharp
using (Metadata metadata = new Metadata(Constants.InputPdf))
{
    // Remove detected metadata packages
    var affected = metadata.Sanitize();
    Console.WriteLine("Properties removed: {0}", affected);

    metadata.Save(Constants.OutputPdf);
}
```

## Extract Metadata from Files via C# Code

```csharp
foreach (string file in Directory.GetFiles(Constants.InputPath))
{
    using (Metadata metadata = new Metadata(file))
    {
        if (metadata.FileFormat != FileFormat.Unknown && !metadata.GetDocumentInfo().IsEncrypted)
        {
            Console.WriteLine();
            Console.WriteLine(file);

            // fetch all metadata properties that fall into a particular category
            var properties = metadata.FindProperties(p => p.Tags.Any(t => t.Category == Tags.Content));
            Console.WriteLine("The metadata properties describing some characteristics of the file content: title, keywords, language, etc.");
            foreach (var property in properties)
            {
                Console.WriteLine("{0} = {1}", property.Name, property.Value);
            }

            // fetch all properties having a specific type and value
            var year = DateTime.Today.Year;
            properties = metadata.FindProperties(p => p.Value.Type == MetadataPropertyType.DateTime &&
                                                     p.Value.ToStruct(DateTime.MinValue).Year == year);

            Console.WriteLine("All datetime properties with the year value equal to the current year");
            foreach (var property in properties)
            {
                Console.WriteLine("{0} = {1}", property.Name, property.Value);
            }
        }
    }
}
```

[Product Page](https://products.groupdocs.com/metadata/net) | [Documentation](https://products.groupdocs.com/metadata/net) | [Demo](https://products.groupdocs.app/metadata/family) | [API Reference](https://apireference.groupdocs.com/net/metadata) | [Examples](https://github.com/groupdocs-metadata/GroupDocs.Metadata-for-.NET) | [Blog](https://blog.groupdocs.com/category/metadata/) | [Free Support](https://forum.groupdocs.com/c/metadata) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
