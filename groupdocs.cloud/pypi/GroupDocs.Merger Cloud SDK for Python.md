Python Cloud SDK wraps GroupDocs.Merger Cloud API so you could seamlessly integrate Document Joining features into your own Python apps.

[GroupDocs.Merger Cloud SDK for Python](https://products.groupdocs.cloud/merger/python) helps developers implement document merging for over 35 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe & markup file formats, and merge documents. 

Check out the [API Reference](https://apireference.groupdocs.cloud/merger/) to know all about the GroupDocs.Merger REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## Document Merging in the Cloud

- Load password protected documents.
- [Integrated storage API](https://wiki.groupdocs.cloud/editorcloud/developer-guide/storage-operations/) for unified access to files & folders.
- Extract basic information about the document.
- Set, update or remove document password.
- Change portrait or landscape orientation of the document pages.
- [Merge two of more documents](https://wiki.groupdocs.cloud/mergercloud/developer-guide/document-operations/join-multiple-documents/) into a single file.
- Merge specific pages from several different documents into a single file.
- Join page ranges from various documents into a single resultant file.
- [Split a source document](https://wiki.groupdocs.cloud/mergercloud/developer-guide/document-operations/split-document/) into many different files.
- Generate image representation of document pages as preview.
- Create document image preview of all pages, specific pages, or a page range.
- [Move, remove, rotate, swap, and extract](https://wiki.groupdocs.cloud/mergercloud/developer-guide/pages-operations/) document pages.

## Merge & Split File Formats

GroupDocs.Merger Cloud API [supports 35+ file formats](https://wiki.groupdocs.cloud/mergercloud/getting-started/supported-document-formats/) that it can load & perform merge or split operations.

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

The following file formats are supported for trimming, moving, swapping pages or changing page orientation.

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

## Getting Started with GroupDocs.Merger Cloud SDK for Python

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-python). You can either directly use the source code or get PIP distribution via `pip install groupdocs-merger-cloud`.

Execute following snippet to load supported formats.

```python
# Import module
import groupdocs_merger_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_merger_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    print("Supported file-formats:")
    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension)) 
except groupdocs_merger_cloud.ApiException as e:
    print("Exception when calling get_supported_file_formats: {0}".format(e.message))
```

## Python SDK to Join DOCX Document Pages

```python
# For complete examples and data files, please go to https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-python-samples
app_sid = "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
app_key = "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
documentApi = groupdocs_merger_cloud.DocumentApi.from_keys(app_sid, app_key)

item1 = groupdocs_merger_cloud.JoinItem()
item1.file_info = groupdocs_merger_cloud.FileInfo("WordProcessing/sample-10-pages.docx")
item1.pages = [3, 6, 8]

item2 = groupdocs_merger_cloud.JoinItem()
item2.file_info = groupdocs_merger_cloud.FileInfo("WordProcessing/four-pages.docx")
item2.start_page_number = 1
item2.end_page_number = 4
item2.range_mode = "OddPages"

options = groupdocs_merger_cloud.JoinOptions()
options.join_items = [item1, item2]
options.output_path = "Output/joined-pages.docx"

result = documentApi.join(groupdocs_merger_cloud.JoinRequest(options))
```

[Product Page](https://products.groupdocs.cloud/merger/python) | [Documentation](https://wiki.groupdocs.cloud/mergercloud/) | [API Reference](https://apireference.groupdocs.cloud/merger/) | [Code Samples](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/merger/) | [Free Support](https://forum.groupdocs.cloud/c/merger) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
