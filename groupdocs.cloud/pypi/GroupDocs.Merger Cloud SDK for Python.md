This REST API enables your Python apps to [perform document merging & joining](https://products.groupdocs.cloud/merger/python) for [40+ file formats](https://wiki.groupdocs.cloud/mergercloud/getting-started/supported-document-formats/), while page manipulation for 35+ formats.

## Cloud Document Merger Features

- [Merge two of more documents](https://wiki.groupdocs.cloud/mergercloud/developer-guide/document-operations/join-multiple-documents/) into a single file.
- Merge specific pages from several different documents into a single file.
- Join page ranges from various documents into a single resultant file.
- Split a source document into many different files.
- Generate image representation of document pages as preview.
- Create document image preview of all pages, specific pages, or a page range.
- Move, remove, rotate, swap, and extract document pages.
- [Change portrait or landscape orientation](https://wiki.groupdocs.cloud/mergercloud/developer-guide/pages-operations/change-page-orientation/) of the document pages.
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

## Dependencies

- Python 2.7 or 3.4+

## Installation

Install `groupdocs-merger-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

`pip install groupdocs-merger-cloud`

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

`python setup.py install`

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-python) for other common usage scenarios.

## Getting Started

Please follow the [installation procedure](https://pypi.org/project/groupdocs-merger-cloud/#installation) and then run following:

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
