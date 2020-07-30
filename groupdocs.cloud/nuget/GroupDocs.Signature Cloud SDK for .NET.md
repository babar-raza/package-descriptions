# .NET Cloud REST API for eSigning Documents

Use this REST API to [search, verify & create signatures](https://products.groupdocs.cloud/signature/net) of 6 different types for a lot of file formats from within your C#, ASP.NET, & other .NET cloud apps.

## Cloud Document Signing Features

- Supports application of several types of document signatures.
- Specify pages (even, odd, specific etc.) to apply the signature on.
- Configure page padding options.
- Specify font, color, alignment & other appearance settings for the signature.
- Apply crop settings for the signature background.
- Setting to repeat the signature string to fill the specified area.
- Supports `CryptoApi` & `XmlDsig` methods of digital signatures.
- Configure alignment of text string along the barcode type signature.
- Support for various types of brushes to perform signature formatting.
- Apply signature to password-protected documents.
- Perform document signature verification.
- Get or set the time at which the document was digitally signed.
- Option to search some type of signatures from the document.

## New Features & Enhancements in Version 20.7

- Added support for new file formats.
- Implemented `Z-Order` for Text Signature.
- Implemented border for Image Signature.
- Ability to set up additional properties for digital signatures.
- `Opacity` option has been renamed to `Transparency`.
- `Border` options replaced with `BorderLine` class.

For the detailed notes, please visit [GroupDocs.Signature Cloud 20.7 Release Notes](https://wiki.groupdocs.cloud/signaturecloud/release-notes/release-notes-2020/groupdocs-signature-cloud-20-7-release-notes/).

## Signature Supported File Formats

The following file formats are supported for the image, stamp and text type of signatures:

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POT, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, ODP
**Image:** JPG, PNG, BMP, GIF, TIFF, CDR
**Rich Text:** RTF
**Adobe Acrobat:** PDF

## Digital Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPTM, PPTX
**OpenOffice:** ODT
**Adobe Acrobat:** PDF

## Barcode Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** POT, POTM, PPSX, PPTX
**OpenOffice:** ODT, ODP, ODS, OTT
**Image:** JPG, PNG, BMP, GIF, TIFF, CDR
**Rich Text:** RTF
**Adobe Acrobat:** PDF

## QR-Code Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSM, XLT, XLTX, XLTM
**OpenOffice:** OTT
**Image:** JPG, PNG, BMP, GIF, TIFF, CDR
**Rich Text:** RTF
**Adobe Acrobat:** PDF

## Supported Signature Types

- Text
- Image
- Barcode
- QR-code
- Digital
- Stamp

## Getting Started

You do not need to install anything to get started with GroupDocs.Signature Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Signature-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Signature assembly in your project. If you already have GroupDocs.Signature Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Signature-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-dotnet) for other common usage scenarios.

## Verifying QRCode Signature in a Document via C# Code

```csharp
var configuration = new Configuration
{
    AppSid = Sid,
    AppKey = Key
};

var apiInstance = new SignatureApi(configuration);
var verifyOptionsData = new GroupDocs.Signature.Cloud.Sdk.Model.PdfVerifyQRCodeOptionsData()
{
    DocumentPageNumber = 1,
    QRCodeTypeName="QR",
    Text = "1234567890",
    VerifyAllPages = false
};
    var request = new PostVerificationQRCodeRequest
{
    Name = "02_pages.pdf",
    VerifyOptionsData = verifyOptionsData,
    Password = null,
    Folder = "Output"
};

var response = apiInstance.PostVerificationQRCode(request);

Debug.Print("FleName: " + response.FileName);
Debug.Print("Result: " + response.Result);
```

[Product Page](https://products.groupdocs.cloud/signature/net) | [Documentation](https://wiki.groupdocs.cloud/signaturecloud/) | [Demo](https://products.groupdocs.app/signature/family) | [API Reference](https://apireference.groupdocs.cloud/signature/) | [Examples](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/signature/) | [Free Support](https://forum.groupdocs.cloud/c/signature) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
