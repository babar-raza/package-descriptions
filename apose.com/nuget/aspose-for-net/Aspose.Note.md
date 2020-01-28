It is a standalone class library that allows to interact with Microsoft OneNote® documents for processing and conversion. 

Aspose.Note for .NET can be used for printing ONE documents as well as manipulation of pages, images, text, tables, attachments, tags, tasks, text styles, and hyperlinks, without needing Microsoft OneNote.

## Microsoft OneNote File Processing Features
-  Load, edit and save Microsoft OneNote documents via API.
-  Navigate through the OneNote Document Object Model (DOM).
-  Insert an image into an OneNote file.
-  Parse and export various numbered list formats.
-  Extract text from any part of an OneNote document.
-  Export OneNote documents as other popular formats.

## Read & Write OneNote Format
**Microsoft OneNote:** ONE

## Save OneNote Files As
**Fixed Layout:** PDF
**Web:** HTML
**Images:** GIF, JPEG, PNG, BMP, TIFF

## Read Formats
ONETOC2 

## Platform Independence
Aspose.Note for .NET can be used to build both the 32-bit and the 64-bit .NET applications, including ASP.NET, Web Services & WinForms. Its deployment is very easy and consists of a single assembly with no dependencies (except for the .NET framework). Aspose.Note.dll is CLS compliant, written entirely in C# and contains only safe managed code for .NET Framework, .NET Core & Sliverlight 3.

## Getting Started with Aspose.Note for .NET
Are you ready to give Aspose.Note for .NET a try? Simply execute `Install-Package Aspose.Note` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Note for .NET and want to upgrade the version, please execute `Update-Package Aspose.Note` to get the latest version.

## Convert Microsoft OneNote to PDF Format using C#
Execute below code snippet to see how Aspose.Note API performs in your environment or check the [GitHub Repository](https://github.com/aspose-note/Aspose.Note-for-.NET) for other common usage scenarios.

```csharp
// load the document into Aspose.Note.
Document oneFile = new Document(dir + "template.one");
// save the document as PDF
oneFile.Save(dir + "output.pdf", SaveFormat.Pdf);
```

## Extract Images from Microsoft OneNote Document
Aspose.Note for .NET enables your .NET applications to list and manipulate images from an OneNote document as demonstrated with following snippet:

```csharp
// load the document into Aspose.Note.
Document oneFile = new Document(dir + "template.one");
// get all image nodes
IList<Aspose.Note.Image> nodes = oneFile.GetChildNodes<Aspose.Note.Image>();
foreach (Aspose.Note.Image image in nodes)
{
    using (MemoryStream stream = new MemoryStream(image.Bytes))
    {
        using (Bitmap bitMap = new Bitmap(stream))
        {
            // save image bytes to a file
            bitMap.Save(dir + image.FileName);
        }
    }
}
```

[Product Page](https://products.aspose.com/note/net) | [Documentation](https://docs.aspose.com/display/notenet/Home) | [API Reference](https://apireference.aspose.com/net/note) | [Code Examples](https://github.com/aspose-note/Aspose.Note-for-.NET) | [Blog](https://blog.aspose.com/category/note/) | [Free Support](https://forum.aspose.com/c/note) |  [Temporary License](https://purchase.aspose.com/temporary-license)