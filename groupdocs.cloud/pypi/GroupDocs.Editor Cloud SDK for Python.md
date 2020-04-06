Python Cloud SDK wraps GroupDocs.Editor Cloud API so you could seamlessly integrate Document Editing features into your own Python apps.

[GroupDocs.Comparison Cloud SDK for Python](https://products.groupdocs.cloud/editor/python) helps developers implement document comparison for over 40 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, text & markup file formats, and edit documents using front-end WYSIWYG editor. 

Check out the [API Reference](https://apireference.groupdocs.cloud/editor/) to know all about the GroupDocs.Editor REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## Document Editing in the Cloud

- Load password protected documents.
- [Integrated storage API](https://wiki.groupdocs.cloud/editorcloud/developer-guide/storage-operations/) for unified access to files & folders.
- Extract basic information about the document.
- Support for highlighting and formatting options.

## Document Specific REST Models

- [Edit word processing documents](https://wiki.groupdocs.cloud/editorcloud/developer-guide/document-edit-operations/working-with-wordprocessing-documents/) in flow or paged mode.
- Extract font information for a consistent look and feel of the edited documents.
- Editing multi-tabbed spreadsheets with the ability to specify the index of the worksheet.
- [Edit DSV files](https://wiki.groupdocs.cloud/editorcloud/developer-guide/document-edit-operations/working-with-dsv-documents/).
- Specify the separator for the CSV and TSV files with flexible conversion options for dates and numbers.
- Optimize memory usage for large files.
- Fix incorrect document structure of the XML files.
- Recognize email addresses and URIs in the XML files.
- Enable pagination and protection while saving Word documents.

## Supported File Formats for Editing

GroupDocs.Editor Cloud API [supports 40+ file formats](https://wiki.groupdocs.cloud/editorcloud/getting-started/supported-document-formats/) that it can load & edit.

**Word Processing:** DOC, DOCX, DOCM, DOT, DOTM, DOTX, FlatOPC, ODT, OTT, RTF, WordML
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLTX, XLTM, XLSB, XLAM, SXC, SpreadsheetML, ODS, FODS, DIF, DSV, CSV, TSV
**Presentation:** PPT (95), PPT (97-2003), PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, POTM, ODP, OTP
**Markup:** HTML, XML
**Other:** TXT

## Getting Started with GroupDocs.Editor Cloud SDK for Python

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-python). You can either directly use the source code or get PIP distribution via `pip install groupdocs-editor-cloud`.

Execute following snippet to load supported formats.

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

## Edit Presentations in the Cloud using Python SDK

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
