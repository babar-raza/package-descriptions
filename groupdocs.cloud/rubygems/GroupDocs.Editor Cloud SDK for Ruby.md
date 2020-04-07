# Ruby Cloud REST API for Document Editing

Use this REST API to enhance your Ruby apps to [edit documents, spreadsheets, presentations](https://products.groupdocs.cloud/editor/ruby) of 40+ file formats from within your cloud apps.

## Cloud Document Editor Features

- Edit word processing documents in flow or paged mode.
- Extract font information for a consistent look and feel of the edited documents.
- Support for the editing of multi-tabbed spreadsheets.
- Ability to specify the index of the currently edited worksheet.
- Works with DSV (Delimiter Separated Values) files.
- Specify the separator for the CSV and TSV files.
- Flexible conversion options for dates and numbers in TSV, CSV files.
- Optimize memory usage of large CSV, TSV files.
- Fix incorrect document structure of the XML files.
- Recognize email addresses and URIs in the XML files.
- Support for highlighting and formatting options for XML files.
- Ability to extract basic information about the document.
- Support to work with files and folders in the cloud.

## Supported File Formats

**Word Processing:** DOC, DOCX, DOCM, DOT, DOTM, DOTX, FlatOPC, ODT, OTT, RTF, WordML
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLTX, XLTM, XLSB, XLAM, SXC, SpreadsheetML, ODS, FODS, DIF, DSV, CSV, TSV
**Presentation:** PPT (95), PPT (97-2003), PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, POTM, ODP, OTP
**Markup:** HTML, XML
**Other:** TXT

## Getting Started

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/groupdocs_editor_cloud) (recommended).

## Installation

A gem of *groupdocs_editor_cloud* is available at [rubygems.org](https://rubygems.org/). You can install it with:

`gem install groupdocs_editor_cloud`

To add dependency to your app copy following into your *Gemfile* and run `bundle install`:

`gem "groupdocs_editor_cloud", "~> 19.11"`

Please follow the installation procedure and then run the following code:

```ruby
# Load the gem
require 'groupdocs_editor_cloud'

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API class
api = GroupDocsEditorCloud::InfoApi.from_keys(app_sid, app_key)

# Retrieve supported file-formats
response = api.get_supported_file_formats

# Print out supported file-formats
puts("Supported file-formats:")
response.formats.each do |format|
  puts("#{format.file_format} (#{format.extension})")
end
```

## Edit DOCX Files in Cloud using Ruby REST API

```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-ruby-samples
require 'groupdocs_editor_cloud'

$app_sid = "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$app_key = "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
# Create necessary API instances
fileApi = GroupDocsEditorCloud::FileApi.from_keys($app_sid, $app_key)
editApi = GroupDocsEditorCloud::EditApi.from_keys($app_sid, $app_key)

# The document already uploaded into the storage.
# Load it into editable state
fileInfo = GroupDocsEditorCloud::FileInfo.new
fileInfo.file_path = 'WordProcessing/password-protected.docx'
fileInfo.password = 'password'

loadOptions = GroupDocsEditorCloud::WordProcessingLoadOptions.new
loadOptions.file_info = fileInfo
loadOptions.output_path = "output"

loadRequest = GroupDocsEditorCloud::LoadRequest.new(loadOptions)
loadResult = editApi.load(loadRequest)

# Download html document
htmlFile = fileApi.download_file(GroupDocsEditorCloud::DownloadFileRequest.new loadResult.html_path)
htmlFile.open
html = htmlFile.read
htmlFile.close

# Edit something...
html = html.gsub("Sample test text", "Hello world")

# Upload html back to storage
htmlFile = File.open(htmlFile.path, "w")
htmlFile.write(html)
htmlFile.close
uploadRequest = GroupDocsEditorCloud::UploadFileRequest.new loadResult.html_path, File.open(htmlFile.path, "r")
fileApi.upload_file(uploadRequest)

# Save html back to docx
saveOptions = GroupDocsEditorCloud::WordProcessingSaveOptions.new
saveOptions.file_info = fileInfo
saveOptions.output_path = "output/edited.docx"
saveOptions.html_path = loadResult.html_path
saveOptions.resources_path = loadResult.resources_path

saveRequest = GroupDocsEditorCloud::SaveRequest.new(saveOptions)
saveResult = editApi.save(saveRequest)

puts("Document edited: " + saveResult.path)
```

## Licensing

GroupDocs.Editor Cloud Ruby SDK licensed under [MIT License](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.groupdocs.cloud/editor/ruby) | [Documentation](https://wiki.groupdocs.cloud/editorcloud/) | [Live Demo](https://products.groupdocs.app/editor/family) | [API Reference](https://apireference.groupdocs.cloud/editor/) | [Code Samples](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-ruby) | [Blog](https://blog.groupdocs.cloud/) | [Free Support](https://forum.groupdocs.cloud/c/editor) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
