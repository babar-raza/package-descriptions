# Document Editing Python REST API

Use this REST API to enhance your Python apps to [edit documents](https://products.groupdocs.cloud/editor/python), spreadsheets, presentations of [40+ file formats](https://wiki.groupdocs.cloud/editorcloud/getting-started/supported-document-formats/) from within your cloud apps.

## Cloud Document Editor Features

- Edit word processing documents in [flow or paged mode](https://wiki.groupdocs.cloud/editorcloud/getting-started/features-overview/).
- Extract font information for a consistent look and feel of the edited documents.
- Support for the editing of multi-tabbed spreadsheets.
- Ability to specify the index of the currently edited worksheet.
- [Works with DSV](https://wiki.groupdocs.cloud/editorcloud/developer-guide/document-edit-operations/working-with-dsv-documents/) (Delimiter Separated Values) files.
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

## Platform Independence

GroupDocs.Editor Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Installation

Install `groupdocs-editor-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

`pip install groupdocs-editor-cloud`

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

`python setup.py install`

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-python) for other common usage scenarios.

## Getting Started

Please follow the [installation procedure](https://pypi.org/project/groupdocs-editor-cloud/#installation) and then run following:

```python
# Import module
import groupdocs_editor_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_editor_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    print("Supported file-formats:")
    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension))
except groupdocs_editor_cloud.ApiException as e:
    print("Exception when calling get_supported_file_formats: {0}".format(e.message))
```

## Working with Presentations using Python SDK

```python
# For complete examples and data files, please go to https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-python-samples
import groupdocs_editor_cloud

app_sid = "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
app_key = "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
editApi = groupdocs_editor_cloud.EditApi.from_keys(app_sid, app_key)
fileApi = groupdocs_editor_cloud.FileApi.from_keys(app_sid, app_key)

# The document already uploaded into the storage.
# Load it into editable state
fileInfo = groupdocs_editor_cloud.FileInfo("Presentation/with-notes.pptx")
loadOptions = groupdocs_editor_cloud.PresentationLoadOptions()
loadOptions.file_info = fileInfo
loadOptions.output_path = "output"
loadOptions.slide_number = 0
loadResult = editApi.load(groupdocs_editor_cloud.LoadRequest(loadOptions))

# Download html document
htmlFile = fileApi.download_file(groupdocs_editor_cloud.DownloadFileRequest(loadResult.html_path))
html = ""
with open(htmlFile, 'r') as file:
    html = file.read()

# Edit something...
html = html.replace("Slide sub-heading", "Hello world!")

# Upload html back to storage
with open(htmlFile, 'w') as file:
    file.write(html)

fileApi.upload_file(groupdocs_editor_cloud.UploadFileRequest(loadResult.html_path, htmlFile))

# Save html back to pptx
saveOptions = groupdocs_editor_cloud.PresentationSaveOptions()
saveOptions.file_info = fileInfo
saveOptions.output_path = "output/edited.pptx"
saveOptions.html_path = loadResult.html_path
saveOptions.resources_path = loadResult.resources_path
saveResult = editApi.save(groupdocs_editor_cloud.SaveRequest(saveOptions))

# Done
print("Document edited: " + saveResult.path)
```

## Licensing

GroupDocs.Editor Cloud Python SDK licensed under [MIT License](http://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-python/LICENSE).

[Product Page](https://products.groupdocs.cloud/editor/python) | [Documentation](https://wiki.groupdocs.cloud/editorcloud/) | [API Reference](https://apireference.groupdocs.cloud/editor/) | [Code Samples](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/editor/) | [Free Support](https://forum.groupdocs.cloud/c/editor) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
