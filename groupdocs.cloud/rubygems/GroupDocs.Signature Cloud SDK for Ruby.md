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

## Working with Digital Signatures using Ruby REST API

```ruby
# Load the gem
require 'groupdocs_signature_cloud'
require 'common_utilities/Utils.rb'

class Signing_Documents
  def self.Signature_Ruby_Digital_Signature()

    # Getting instance of the API
    api = Common_Utilities.Get_SignApi_Instance()

    $info = GroupDocsSignatureCloud::FileInfo.new()
    $info.file_path = "signaturedocs\\one-page.docx"
    $info.password = nil

    $opts = GroupDocsSignatureCloud::SignDigitalOptions.new()
    $opts.document_type = "WordProcessing"
    $opts.signature_type = 'Digital'
    $opts.image_guid = "signaturedocs\\signature.jpg"
    $opts.certificate_guid = "signaturedocs\\temp.pfx"
    $opts.password = '1234567890'

    $settings = GroupDocsSignatureCloud::SignSettings.new()
    $settings.options = [$opts]

    $settings.save_options = GroupDocsSignatureCloud::SaveOptions.new()
    $settings.save_options.output_file_path = "signaturedocs\\signedDigitalOne_page.docx"
    $settings.file_info = $info

    $request = GroupDocsSignatureCloud::CreateSignaturesRequest.new($settings)

    # Executing an API.
    $response = api.create_signatures($request)

    puts("file_path: " + $response.file_info.file_path)
  end
end
```

## Licensing

GroupDocs.Signature Cloud Ruby SDK licensed under [MIT License](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/signature/ruby) | [Documentation](https://wiki.groupdocs.cloud/signaturecloud/) | [Demo](https://products.groupdocs.app/signature/family) | [API Reference](https://apireference.groupdocs.cloud/signature/) | [Examples](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/signature/) | [Free Support](https://forum.groupdocs.cloud/c/signature) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
