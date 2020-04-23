# Document Merger Ruby Cloud REST API

This REST API enables your Ruby apps to [perform document merging & joining](https://products.groupdocs.cloud/merger/ruby) for 40+ file formats, while page manipulation for 35+ formats.

## Cloud Document Merger Features

- Merge two of more documents into a single file.
- Merge specific pages from several different documents into a single file.
- Join page ranges from various documents into a single resultant file.
- Split a source document into many different files.
- Generate image representation of document pages as preview.
- Create document image preview of all pages, specific pages, or a page range.
- Move, remove, rotate, swap, and extract document pages.
- Change portrait or landscape orientation of the document pages.
- Set, update or remove document password.
- Extract basic information about the document.

## Merge & Split File Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX
**Microsoft Visio:** VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
**Microsoft OneNote:** ONE
**OpenOffice:** ODT, OTT, ODP, OTP, ODS
**Markup:** HTML, MHT
**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB, CSV, TSV, TXT

## Page Manipulation File Formats

The following file formats are supported for trimming, moving, swapping pages or changing page orientation:
**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX
**Microsoft Visio:** VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
**Microsoft OneNote:** ONE
**OpenOffice:** ODT, OTT, ODP, OTP, ODS
**Markup:** HTML, MHT
**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB

## Page Rotation File Formats

**Fixed Layout:** PDF, XPS
**Other:** TEX, EPUB

## Platform Independence

GroupDocs.Merger Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/groupdocs_merger_cloud) (recommended).

## Installation

A gem of *groupdocs_merger_cloud* is available at [rubygems.org](https://rubygems.org/). You can install it with:

`gem install groupdocs_merger_cloud`

To add dependency to your app copy following into your *Gemfile* and run `bundle install`:

`gem "groupdocs_merger_cloud", "~> 19.10"`

Please follow the installation procedure and then run the following code:

```ruby
# Load the gem
require 'groupdocs_merger_cloud'

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API class
api = GroupDocsMergerCloud::InfoApi.from_keys(app_sid, app_key)

# Retrieve supported file-formats
response = api.get_supported_file_formats

# Print out supported file-formats
puts("Supported file-formats:")
response.formats.each do |format|
  puts("#{format.file_format} (#{format.extension})")
end
```

## Extract DOCX Pages by Page Numbers using Ruby REST API

```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-ruby-samples
$app_sid = "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$app_key = "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud

pagesApi = GroupDocsMergerCloud::PagesApi.from_keys($app_sid, $app_key)

options = GroupDocsMergerCloud::ExtractOptions.new
options.file_info = GroupDocsMergerCloud::FileInfo.new
options.file_info.file_path = 'WordProcessing/sample-10-pages.docx'
options.output_path = "Output/extract-pages-by-numbers.docx"
options.pages = [2, 4, 7]

result = pagesApi.extract(GroupDocsMergerCloud::ExtractRequest.new(options))
```

## Licensing

GroupDocs.Merger Cloud Ruby SDK licensed under [MIT License](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/merger/ruby) | [Documentation](https://wiki.groupdocs.cloud/mergercloud/) | [Live Demo](https://products.groupdocs.app/merger/family) | [API Reference](https://apireference.groupdocs.cloud/merger/) | [Examples](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-ruby) | [Blog](https://blog.groupdocs.cloud/category/merger/) | [Free Support](https://forum.groupdocs.cloud/c/merger) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
