# Ruby Cloud REST API for eSigning Documents

Use this REST API to [search, verify & create signatures](https://products.groupdocs.cloud/signature/ruby) of 6 different types for a lot of file formats from within your Ruby cloud apps.

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

## New Features in Version 19.5.0

- This is the first release of a completely new version of the API `GroupDocs.Signature.Cloud v2.0`.
- `V2` provides a much simpler and intuitive API comparing with `V1`.
- `V2` includes Storage and File API which enables you to manage storage and files.

For the detailed notes, please visit [GroupDocs.Signature Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/signaturecloud/release-notes/release-notes-2019/groupdocs-signature-cloud-19-5-release-notes/).

## Signature Supported File Formats

The following file formats are supported for the barcode, image, QR-code, stamp and text type of signatures:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP
**Image:** BMP, GIF, JPG, JPEG, PNG, SVG, TIF, TIFF, WEBP, DJVU
**Metafile:** WMF
**CorelDraw:** CDR, CMX
**Adobe Photoshop:** PSD
**Adobe Acrobat:** PDF

## Digital Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**OpenOffice:** ODS, OTS
**Adobe Acrobat:** PDF

## FormField Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**OpenOffice:** ODS, OTS, ODP
**Adobe Acrobat:** PDF

## Metadata Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP
**Image:** JPG, JPEG, PNG, SVG, TIF, TIFF
**Adobe Photoshop:** PSD
**Adobe Acrobat:** PDF

## Supported Signature Types

- Text
- Image
- Barcode
- QR-code
- Digital
- Stamp

## Platform Independence

GroupDocs.Signature Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/groupdocs_signature_cloud) (recommended).

## Installation

A gem of *groupdocs_signature_cloud* is available at [rubygems.org](https://rubygems.org/). You can install it with:

`gem install groupdocs_signature_cloud`

To add dependency to your app copy following into your *Gemfile* and run `bundle install`:

`gem "groupdocs_signature_cloud", "~> 19.5"`

## Getting Started

Please follow the installation procedure and then run the following code:

```ruby
# Load the gem

require 'groupdocs_signature_cloud'

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API class
api = GroupDocsSignatureCloud::InfoApi.from_keys(app_sid, app_key)

# Retrieve supported file-formats
response = api.get_supported_file_formats

# Print out supported file-formats
puts("Supported file-formats:")
response.formats.each do |format|
  puts("#{format.file_format} (#{format.extension})")
end
```

## Licensing

GroupDocs.Signature Cloud Ruby SDK licensed under [MIT License](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/signature/ruby) | [Documentation](https://wiki.groupdocs.cloud/signaturecloud/) | [API Reference](https://apireference.groupdocs.cloud/signature/) | [Code Samples](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/signature/) | [Free Support](https://forum.groupdocs.cloud/c/signature) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
