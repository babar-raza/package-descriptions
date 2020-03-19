# Document Annotation Ruby Cloud REST API

This REST API enhances your Ruby cloud apps to [import, export & process text & figure annotations](https://products.groupdocs.cloud/annotation/ruby) within documents for 35+ file formats.

## Cloud Document Annotation Features

- Fetch document description with meta data and coordinates of text on pages.
- Fetch annotation data from files of supported formats.
- Import annotation information from documents.
- Export annotation information to a document and fetch it as a stream.
- Remove document annotations.
- Get image representation of the document pages.
- Render documents to PDF format with storage URL or stream output.
- Add or remove document or image annotations of various types.

## New Features in Version 19.5.0

- This is the first release of a completely new version of the API `GroupDocs.Annotation.Cloud v2.0`.
- `V2` provides much simpler and intuitive API comparing with `V1`.
- `V2` includes Storage and File API which enables users to manage storage and files.

For the detailed notes, please visit [GroupDocs.Annotation Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/annotationcloud/release-notes/2019/groupdocs-annotation-cloud-19-5-release-notes/).

## Supported Annotation Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF, TXT
**Microsoft Excel:** XLS, XLSX, XLSB, XLSX
**Microsoft PowerPoint:** PPT, PPTX, PPSX
**Microsoft Visio:** VSD, VDX, VSS, VSDM
**OpenOffice:** OTT, ODT, ODP, OTP
**Image:** JPEG, TIFF, BMP, GIF, DJVU
**Metafile:** EMF, WMF
**Email:** EML, EMLX, MSG
**Portable:** PDF
**Medical Imagery:** DICOM
**Markup:** HTML, MHTML
**AutoCAD:** CAD

## Supported Text Annotation Types

**Text annotation** – add comments to selected text.
**Text replacement** – highlight which text should be replaced with what.
**Text redaction** – hide confidential text.
**Strikeout/underline** – highlight text with strikethroughs/underlines.
**Typewriter** – add sticky notes with rich text.

## Supported Figure Annotation Types

**Area annotation** – add notes to an area highlighted with a rectangle.
**Point annotation** – add notes to any point in the document.
**Area redaction** – hide confidential parts of an image or text.
**Polyline** – draw freehand lines and shapes.
**Pointer/arrow** – drop arrows pointing to an object.
**Watermark** – create text-based watermark overlays.
**Distance** – measure the distance between any objects in a document.

## Platform Independence

GroupDocs.Annotation Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/groupdocs_annotation_cloud) (recommended).

## Installation

A gem of *groupdocs_annotation_cloud* is available at [rubygems.org](https://rubygems.org/). You can install it with:

`gem install groupdocs_annotation_cloud`

To add dependency to your app copy following into your *Gemfile* and run `bundle install`:

`gem "groupdocs_annotation_cloud", "~> 19.5"`

Please follow the installation procedure and then run the following code:

```ruby
# Load the gem
require 'groupdocs_annotation_cloud'

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API class
api = GroupDocsAnnotationCloud::InfoApi.from_keys(app_sid, app_key)

# Retrieve supported file-formats
response = api.get_supported_file_formats

# Print out supported file-formats
puts("Supported file-formats:")
response.formats.each do |format|
  puts("#{format.file_format} (#{format.extension})")
end
```

## Licensing

GroupDocs.Annotation Cloud Ruby SDK licensed under [MIT License](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/annotation/ruby) | [Documentation](https://wiki.groupdocs.cloud/annotationcloud/) | [API Reference](https://apireference.groupdocs.cloud/annotation/) | [Code Samples](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-ruby) | [Blog](https://blog.groupdocs.cloud/category/annotation/) | [Free Support](https://forum.groupdocs.cloud/c/annotation) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
