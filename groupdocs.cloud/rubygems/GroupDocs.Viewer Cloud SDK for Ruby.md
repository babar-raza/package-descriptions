# Ruby Cloud REST API for Document Rendering

This REST API enhances your Ruby based cloud apps to [render](https://products.groupdocs.cloud/viewer/ruby) 85+ types of file formats to image, PDF or HTML formats from within your apps.

## Cloud Document Viewer Features

- Support for rendering lots of document and image file formats.
- Fetch the list of all installed fonts or delete the fonts cache.
- Download HTML page resources, e.g., images, CSS, fonts etc.
- Render a document to PDF for HTML or image representation and download it.
- Fetch document information via various methods.
- Obtain list of links to document pages as HTML or images.
- Fetch and download ZIP archive of document pages as HTML or images.
- Rotate and reorder document pages.
- Specify image quality while rendering PDF as HTML.
- Decrease the resultant file size by excluding fonts when rendering as HTML.
- Render specific sections of worksheets defined as "print area" as HTML.
- Choose to include or exclude hidden content in Excel documents.
- Make the output content in HTML and SVG minified.
- Render a document to responsive HTML.
- Render email messages & render Outlook data files as HTML.
- Get list of all email attachments in its HTML or image representation.
- Download resources of a specific email attachment page for HTML representation.

## Enhancements in Version 19.5

- Improved Cloud products API Reference grouping.

For the detailed notes, please visit [GroupDocs.Viewer Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/viewercloud/release-notes/2019/groupdocs-viewer-cloud-19-5-release-notes/).

## Supported File Formats

**Word Processing:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Spreadsheet:** XLS, XLSB, XLSM, XLSX, ODS, OTS, CSV, TSV
**Presentation:** PPT, PPTM, PPTX, PPS, PPSM, PPSX, POTX, POTM, ODP, OTP
**Project Management:** MPP, MPT
**Email:** EML, EMLX, MSG, OST, PST
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**Markup:** HTML, MHTML
**Diagram:** VDW, VDX, VSD, VSDM, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Note:** ONE
**Portable:** PDF, TEX, XPS
**Image:** BMP, CGM, DCM, DJVU, DNG, EMF, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PCL, PNG, PS, PSD, SVG, TIF, TIFF, WEBP, WMF
**eBook:** EPUB, MOBI

## Getting Started

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/groupdocs_viewer_cloud) (recommended).

## Installation

A gem of *groupdocs_viewer_cloud* is available at [rubygems.org](https://rubygems.org/). You can install it with:

`gem install groupdocs_viewer_cloud`

To add dependency to your app copy following into your *Gemfile* and run `bundle install`:

`gem "groupdocs_viewer_cloud", "~> 19.5"`

## Getting Started

Please follow the installation procedure and then run the following code:

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API class
api = GroupDocsViewerCloud::InfoApi.from_keys(app_sid, app_key)

# Retrieve supported file-formats
response = api.get_supported_file_formats

# Print out supported file-formats
puts("Supported file-formats:")
response.formats.each do |format|
  puts("#{format.file_format} (#{format.extension})")
end
```

## Use Ruby REST API to View DWF Files

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_View
  def self.Viewer_Ruby_Create_View_With_CAD_Options()

    # Getting instance of the API
    $api = Common_Utilities.Get_ViewApi_Instance()

    $viewOptions = GroupDocsViewerCloud::ViewOptions.new()

    $fileInfo = GroupDocsViewerCloud::FileInfo.new()
    $fileInfo.file_path = "viewerdocs/three-layouts.dwf"
    $fileInfo.password = ""
    $fileInfo.storage_name = $myStorage

    $viewOptions.file_info = $fileInfo;

    $renderOptions = GroupDocsViewerCloud::RenderOptions.new()

    $cadOptions = GroupDocsViewerCloud::CadOptions.new()
    $cadOptions.scale_factor = 50

    $renderOptions.cad_options = $cadOptions
    $viewOptions.render_options = $renderOptions

    $request = GroupDocsViewerCloud::CreateViewRequest.new($viewOptions)
    $response = $api.create_view($request)

    puts("Expected response type is ViewResult: " + ($response).to_s)
  end
end
```

## Licensing

GroupDocs.Viewer Cloud Ruby SDK licensed under [MIT License](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/viewer/ruby) | [Documentation](https://wiki.groupdocs.cloud/viewercloud/) | [Live Demo](https://products.groupdocs.app/viewer/family) | [API Reference](https://apireference.groupdocs.cloud/viewer/) | [Examples](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby) | [Blog](https://blog.groupdocs.cloud/category/viewer/) | [Free Support](https://forum.groupdocs.cloud/c/viewer) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
