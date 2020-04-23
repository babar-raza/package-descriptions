# Ruby Cloud REST API for Document Conversion

This REST API allows your Ruby cloud-based apps to [convert documents](https://products.groupdocs.cloud/conversion/ruby) of 50+ file formats from within your apps without any 3rd party tool.

## Cloud Document Conversion Features

- Specify document conversion settings.
- Specify page width & height while converting CAD diagrams.
- Choose specific CAD diagram layouts to be converted.
- Substitute specific fonts during cells document conversion.
- Convert specific cell range while converting to non-cell formats.
- Skip empty rows and columns when converting cells documents.
- Display or hide email header, "from", "to", "cc" & "bcc".
- Substitute specific fonts when converted some supported formats.
- Start converting from specified page number.
- Convert a specific number of pages from the specified page.
- Use PDF as an intermediary format while converting.
- Apply watermark during conversion process.

## New Features in Version 20.2

- **New Source Formats:** DIB, XLT, POT, XLAM, MPX, JPC, DWT, JPEG-LS.
- **New Target Formats:** WMF, EMF, XLAM.
- Supports encoding for source `CSV` and `TXT` documents.
- Supports `TimeZoneOffset` and `ConvertAttachments` for source Email documents.

## Enhancements in Version 20.2

- Improved quality of Diagram to Word document conversion.
- Converting multi-page `TIFF` to `PDF`.
- Improvement in `MPP` to `XLS` conversion.

For the detailed notes, please visit, [GroupDocs.Conversion Cloud 20.2 Release Notes](https://wiki.groupdocs.cloud/conversioncloud/release-notes/2020/groupdocs-conversion-cloud-20-2-release-notes/).

## Conversion File Formats

GroupDocs.Conversion Cloud SDK for .NET allows you to convert any of the following type of file formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLT, XLS2003, XLSB, XLSM, XLAM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX, POT
**Microsoft Visio:** VDW, VDX, VSD, VSDX, VSS, VST, VSX, VTX
**Microsoft Project:** MPP, MPT, MPX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**AutoCAD:** DWG, DWT, DXF
**Image:** BMP, GIF, ICO, JPEG, JPEG-LS, JPG, JPC, PNG, SVG, TIF, TIFF, DIB
**Email:** EML, EMLX, MSG
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML, MHT

to the following formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLS2003, XLSB, XLSM, XLAM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**Image:** BMP, GIF, ICO, JPEG, JPG, PNG, TIF, TIFF
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML
**Metafile:** WMF, EMF

## Getting Started

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/groupdocs_conversion_cloud) (recommended).

## Installation

A gem of *groupdocs_conversion_cloud* is available at [rubygems.org](https://rubygems.org/). You can install it with:

`gem install groupdocs_conversion_cloud`

To add dependency to your app copy following into your *Gemfile* and run `bundle install`:

`gem "groupdocs_conversion_cloud", "~> 20.2"`

Please follow the installation procedure and then run the following code:

```ruby
# Load the gem

require 'groupdocs_conversion_cloud'

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API class
api = GroupDocsConversionCloud::InfoApi.from_keys(app_sid, app_key)

# Retrieve supported converison types
request = GroupDocsConversionCloud::GetSupportedConversionTypesRequest.new
response = api.get_supported_conversion_types(request)

# Print out supported conversion types
puts("Supported file-formats:")
response.each do |format|
puts("#{format.source_format} to [#{format.target_formats.join(', ')}]")
```

## Advanced Document Conversion Options using Ruby REST API

```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-ruby-samples
require 'groupdocs_conversion_cloud'

$app_sid = "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$app_key = "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
# Create necessary API instances
apiInstance = GroupDocsConversionCloud::ConvertApi.from_keys($app_sid, $app_key)

# Prepare convert settings
settings = GroupDocsConversionCloud::ConvertSettings.new
settings.file_path = "WordProcessing/four-pages.docx"
settings.format = "html"
convertOptions = GroupDocsConversionCloud::HtmlConvertOptions.new
convertOptions.from_page = 1
convertOptions.pages_count = 1
convertOptions.fixed_layout = true
settings.convert_options = convertOptions
settings.output_path = "converted"

# Convert
result = apiInstance.convert_document(GroupDocsConversionCloud::ConvertDocumentRequest.new(settings))
```

## Licensing

GroupDocs.Conversion Cloud Ruby SDK licensed under [MIT License](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/conversion/ruby) | [Documentation](https://wiki.groupdocs.cloud/conversioncloud/) | [Live Demo](https://products.groupdocs.app/conversion/family) | [API Reference](https://apireference.groupdocs.cloud/conversion/) | [Examples](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-ruby) | [Blog](https://blog.groupdocs.cloud/category/conversion/) | [Free Support](https://forum.groupdocs.cloud/c/conversion) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
