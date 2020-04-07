# Document Comparison Ruby Cloud REST API

This cloud REST API enhances your Ruby cloud apps to [compare two documents](https://products.groupdocs.cloud/comparison/ruby), fetch, accept or reject the changes. Supports 90+ file formats.

## Cloud Document Comparison Features

- Compare two documents and fetch changes.
- Fetch document changes based on change category, such as, numeric only.
- Accept or reject the changes that come up after document comparison.
- Get the image stream of resultant document via `JsonRequest` object.
- Save the resultant document to streams as set of images.
- Get the resultant document path.
- Add summary page to resultant document after comparison.
- Show deleted components in the resultant document.
- Detect style changes.
- Get or set password to the the resultant document.

## New Features in Version 19.5

- This is the first release of a completely new version of the API `GroupDocs.Comparison.Cloud v2.0`.
- `V2` provides much simpler and intuitive API as compared to `V1`.
- `V2` includes Storage and File API which enables you to manage storage and files.
- Internal cloud solution is based on the modern micro-service architecture.

For the detailed notes, please visit [GroupDocs.Comparison Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/comparisoncloud/release-notes/2019/groupdocs-comparison-cloud-19-5-release-notes/).

## Supported Document Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX, XLTM, XLTX, ODS, OTS, CSV, TSV
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POTM, POTX, ODP, OTP
**Microsoft Visio:** VDW, VDX, VSD, VSDML, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Microsoft Project:** MPP, MPT
**Microsoft OneNote:** ONE
**Email:** EML, EMLX, MSG, OST, PST
**Adobe Photoshop:** PSD
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**eBook:** EPUB, MOBI
**Image:** BMP, CGM, DCM, DJVU, DNG, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PNG, SVG, TIF, TIFF, WEBP
**Markup:** HTML, MHT, MHTML, XML
**Portable:** PDF, TEX, XPS
**Metafile:** EMF, WMF
**Other:** PCL, PS

## Getting Started

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/groupdocs_comparison_cloud) (recommended).

## Installation

A gem of *groupdocs_comparison_cloud* is available at [rubygems.org](https://rubygems.org/). You can install it with:

`gem install groupdocs_comparison_cloud`

To add dependency to your app copy following into your *Gemfile* and run `bundle install`:

`gem "groupdocs_comparison_cloud", "~> 19.5"`

Please follow the installation procedure and then run the following code:

```ruby
# Load the gem
require 'groupdocs_comparison_cloud'

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API class
api = GroupDocsComparisonCloud::InfoApi.from_keys(app_sid, app_key)

# Retrieve supported file-formats
response = api.get_supported_file_formats

# Print out supported file-formats
puts("Supported file-formats:")
response.formats.each do |format|
  puts("#{format.file_format} (#{format.extension})")
end
```

## Compare Multiple Documents using Ruby REST API

```ruby
# Load the gem
require 'groupdocs_comparison_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Comparisons
  def self.Comparison_Ruby_Compare_Multiple_Documents()

    # Getting instance of the API
    api = Common_Utilities.Get_CompareApi_Instance()

    $options = GroupDocsComparisonCloud::Options.new()

    # Source file
    $sourceFileInfo = GroupDocsComparisonCloud::FileInfo.new();
    $sourceFileInfo.file_path = "Comparisondocs\\source_protected.docx";
    $sourceFileInfo.password = "1231";
    $sourceFileInfo.storage_name = $myStorage;

    $options.source_file = $sourceFileInfo
    $options.output_path = "Comparisondocs\\result_multi_protected.docx"

    $options.settings = GroupDocsComparisonCloud::Settings.new()
    $options.settings.generate_summary_page = true
    $options.settings.show_deleted_content = true
    $options.settings.style_change_detection = true
    $options.settings.use_frames_for_del_ins_elements = false
    $options.settings.meta_data = nil
    $options.settings.detail_level = "Low"
    $options.settings.diagram_master_setting = nil
    $options.settings.calculate_component_coordinates = false
    $options.settings.clone_metadata = "Default"
    $options.settings.mark_deleted_inserted_content_deep = false
    $options.settings.password = "1111"
    $options.settings.password_save_option = "User"

    $options.settings.deleted_items_style = GroupDocsComparisonCloud::ItemsStyle.new()
    $options.settings.deleted_items_style.begin_separator_string = ""
    $options.settings.deleted_items_style.end_separator_string = ""
    $options.settings.deleted_items_style.font_color = "16711680"
    $options.settings.deleted_items_style.highlight_color = "16711680"
    $options.settings.deleted_items_style.bold = false
    $options.settings.deleted_items_style.italic = false
    $options.settings.deleted_items_style.strike_through = false

    $options.settings.inserted_items_style = GroupDocsComparisonCloud::ItemsStyle.new()
    $options.settings.inserted_items_style.begin_separator_string = ""
    $options.settings.inserted_items_style.end_separator_string = ""
    $options.settings.inserted_items_style.font_color = "255"
    $options.settings.inserted_items_style.highlight_color = "255"
    $options.settings.inserted_items_style.bold = false
    $options.settings.inserted_items_style.italic = false
    $options.settings.inserted_items_style.strike_through = false

    $options.settings.style_changed_items_style = GroupDocsComparisonCloud::ItemsStyle.new()
    $options.settings.style_changed_items_style.begin_separator_string = ""
    $options.settings.style_changed_items_style.end_separator_string = ""
    $options.settings.style_changed_items_style.font_color = "65280"
    $options.settings.style_changed_items_style.highlight_color = "65280"
    $options.settings.style_changed_items_style.bold = false
    $options.settings.style_changed_items_style.italic = false
    $options.settings.style_changed_items_style.strike_through = false

    # First target file
    $targetFileInfo1 = GroupDocsComparisonCloud::FileInfo.new();
    $targetFileInfo1.file_path = "Comparisondocs\\target_protected.docx";
    $targetFileInfo1.password = "5784";
    $targetFileInfo1.storage_name = $myStorage;

    # Second target file
    $targetFileInfo2 = GroupDocsComparisonCloud::FileInfo.new();
    $targetFileInfo2.file_path = "Comparisondocs\\target_2_protected.docx";
    $targetFileInfo2.password = "5784";
    $targetFileInfo2.storage_name = $myStorage;

    $options.target_files = [$targetFileInfo1, $targetFileInfo2]

    $request = GroupDocsComparisonCloud::ComparisonsRequest.new($options)
    $response = api.comparisons($request)

    puts("Expected response type is Link: " + $response.href)
  end
end
```

## Licensing

GroupDocs.Comparison Cloud Ruby SDK licensed under [MIT License](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/comparison/ruby) | [Documentation](https://wiki.groupdocs.cloud/comparisoncloud/) | [Live Demo](https://products.groupdocs.app/comparison/family) | [API Reference](https://apireference.groupdocs.cloud/comparison/) | [Code Samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-ruby) | [Blog](https://blog.groupdocs.cloud/category/comparison/) | [Free Support](https://forum.groupdocs.cloud/c/comparison) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
