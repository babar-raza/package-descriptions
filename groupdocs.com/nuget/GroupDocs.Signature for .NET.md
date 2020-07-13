# .NET API for Document Signature

This on-premise .NET API lets your app end-users [sign the electronic documents](https://products.groupdocs.com/signature/net) from a wide range of file formats. Supports several types of e-signing methods.

## Document Signature Processing Features

- Create and add signatures to documents of various file formats.
- Specify visual attributes of signatures, such as, color, font, margins etc.
- Search and fetch list of signatures from a document.
- Determine if the document contains signatures meeting a specified criteria.
- Extract basic information about the document.
- Generate image representation of document pages for preview.
- Distinguish created signatures from the actual document.
- Put encrypted text into QR-code signature or embed custom data objects.

## New Features & Enhancements in Version 20.6

- Implemented native Watermark signature for Word Processing documents.
- Implemented `AES` encryption algorithm for `Net` Standard platform.
- Implemented modification of native Watermark sugantures for Word processing documents.
- Implemented ability to keep digital signature meta info layer for Document Info.
- Improved validation for unsupported text implementation scenarios.
- Updated implementation of signature rotation for Image documents.

For the detailed notes, please visit [GroupDocs.Signature for .NET 20.6 Release Notes](https://docs.groupdocs.com/signature/net/groupdocs-signature-for-net-20-6-release-notes/).

## Signature Supported Formats

The following section lists the supported file formats for the barcode, image, QR-code, stamp, and text signature types:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX\
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM\
**Microsoft PowerPoint:** PPTX, PPTM, PPT, PPSX, PPSM, PPS, POTX, POTM\
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP\
**Image:** BMP, GIF, JPG, JPEG, PNG, SVG, TIF, TIFF, WEBP\
**CorelDraw:** CDR, CMX\
**Photoshop:** PSD\
**eBook:** DJVU\
**Metafile:** WMF\
**Portable:** PDF

## Digital Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX\
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM\
**OpenOffice:** ODS, OTS\
**Portable:** PDF

## FormField Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX\
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM\
**OpenOffice:** ODS, OTS, ODP\
**Portable:** PDF

## Metadata Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX\
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM\
**Microsoft PowerPoint:** PPTX, PPTM, PPT, PPSX, PPSM, PPS, POTX, POTM\
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP\
**Image:** JPG, JPEG, PNG, SVG, TIF, TIFF\
**Photoshop:** PSD\
**Portable:** PDF

## Supported Signature Types

- Text stamps
- Text labels
- Text as image signature
- Image signature
- Digital signature
- Barcode signature
- QR-code signature
- Metadata signature
- Form-field signature

## Platform Independence

GroupDocs.Signature for .NET does not require any external software or third party tool to be installed. GroupDocs.Signature for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure\
**Mac OS:** Mac OS X\
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)\
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.\
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET and Mono frameworks.

## Getting Started with GroupDocs.Signature for .NET

Are you ready to give GroupDocs.Signature for .NET a try? Simply execute `Install-Package GroupDocs.Signature` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Signature assembly in your project. If you already have GroupDocs.Signature for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Signature` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-signature/GroupDocs.Signature-for.NET) for other common usage scenarios.

## Sign a PDF File and Save it in DOCX Format using C# Code

```csharp
using (Signature signature = new Signature("sample.pdf"))
{
    // create QRCode option with predefined QRCode text
    QRCodeSignOptions signOptions = new QRCodeSignOptions("JohnSmith")
    {
        EncodeType = QRCodeTypes.QR,
        Left = 100,
        Top = 100
    };
    PdfSaveOptions pdfSaveOptions = new PdfSaveOptions()
    {
        FileFormat = PdfSaveFileFormat.DocX,
        OverwriteExistingFiles = true
    };
    // sign document to file
    signature.Sign("SignedPdf.docx", signOptions, pdfSaveOptions);
}
```

## Use C# to Search and Delete Signatures from DOCX File

```csharp
// initialize Signature instance
using (Signature signature = new Signature("signed.docx"))
{
    BarcodeSearchOptions options = new BarcodeSearchOptions();
    List<BarcodeSignature> signatures = signature.Search<BarcodeSignature>(options);
    List<BaseSignature> signaturesToDelete = new List<BaseSignature>();
    // collect signatures to delete
    foreach (BarcodeSignature temp in signatures)
    {
        if (temp.Text.Contains("John"))
        {
            signaturesToDelete.Add(temp);
        }
    }
    // delete signatures
    DeleteResult deleteResult = signature.Delete(signaturesToDelete);
    if (deleteResult.Succeeded.Count == signaturesToDelete.Count)
    {
        Console.WriteLine("All signatures were successfully deleted!");
    }
    else
    {
        Console.WriteLine($"Successfully deleted signatures : {deleteResult.Succeeded.Count}");
        Console.WriteLine($"Not deleted signatures : {deleteResult.Failed.Count}");
    }
    Console.WriteLine("List of deleted signatures:");
    foreach (BaseSignature temp in deleteResult.Succeeded)
    {
        Console.WriteLine($"Signature# Id:{temp.SignatureId}, Location: {temp.Left}x{temp.Top}. Size: {temp.Width}x{temp.Height}");
    }
}
```

[Product Page](https://products.groupdocs.com/signature/net) | [Documentation](https://docs.groupdocs.com/signature/net/) | [Demo](https://products.groupdocs.app/signature/family) | [API Reference](https://apireference.groupdocs.com/net/signature) | [Examples](https://github.com/groupdocs-signature/GroupDocs.Signature-for.NET) | [Blog](https://blog.groupdocs.com/category/signature/) | [Free Support](https://forum.groupdocs.com/c/signature) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
