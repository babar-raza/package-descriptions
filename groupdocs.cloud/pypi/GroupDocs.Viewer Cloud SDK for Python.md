This [REST API](https://products.groupdocs.cloud/viewer/python) enhances your C#, ASP.NET, & other .NET based cloud apps to [render 85+ types of file formats](https://wiki.groupdocs.cloud/viewercloud/getting-started/supported-document-formats/) to image, PDF or HTML formats from within your apps.

## Cloud Document Viewer Features

- Support for rendering lots of document and image file formats.
- Fetch the [list of all installed fonts](https://wiki.groupdocs.cloud/viewercloud/developer-guide/fonts-resource/#HGetFontsResource) or [delete the fonts cache](https://wiki.groupdocs.cloud/viewercloud/developer-guide/fonts-resource/#HDeleteFontsCache).
- Download [HTML page resources](https://wiki.groupdocs.cloud/viewercloud/developer-guide/page-resources/), e.g., images, CSS, fonts etc.
- Render a document to PDF for HTML or image representation and download it.
- Fetch document information via various methods.
- Obtain list of links to document pages as HTML or images.
- Fetch and download ZIP archive of document pages as HTML or images.
- Rotate and reorder document pages.
- Specify image quality while rendering PDF as HTML.
- Decrease the resultant file size by excluding fonts when rendering as HTML.
- Render specific sections of worksheets defined as "print area" as HTML.
- Choose to include or exclude hidden content in Excel documents.
- Make the output content in [HTML and SVG minified](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/minification-of-html-and-svg/).
- Render a [document to responsive HTML](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/rendering-document-to-responsive-html/).
- Render email messages & render Outlook data files as HTML.
- Get list of all email attachments in its HTML or image representation.
- Download resources of a specific email attachment page for HTML representation.

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

## Platform Independence

GroupDocs.Viewer Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Dependencies

- Python 2.7 or 3.4+

## Installation

Install `groupdocs-viewer-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

`pip install groupdocs-viewer-cloud`

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

`python setup.py install`

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python) for other common usage scenarios.

## Getting Started

Please follow the [installation procedure](https://pypi.org/project/groupdocs-viewer-cloud/#installation) and then run following:

```python
# Import module
import groupdocs_viewer_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_viewer_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    print("Supported file-formats:")
    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension)) 
except groupdocs_viewer_cloud.ApiException as e:
    print("Exception when calling get_supported_file_formats: {0}".format(e.message))
```

## Use Python SDK to Render XLSX Spreadsheet

```python
# Get your App SID and App Key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXX-XXXX-XXXX"
app_key = "XXXXXXXXXXXX"

# Create instance of the API.
api = groupdocs_viewer_cloud.ViewerApi.from_keys(app_sid, app_key)

viewOptions = groupdocs_viewer_cloud.ViewOptions()

fileInfo = groupdocs_viewer_cloud.FileInfo()
fileInfo.file_path = "docs\\document.xlsx"
fileInfo.password = "password"
fileInfo.storage_name = "Storage Name"

viewOptions.file_info = fileInfo;

request = groupdocs_viewer_cloud.GetInfoRequest(viewOptions)
response = api.get_info(request)
print(response)
```

## Licensing

GroupDocs.Viewer Cloud Python SDK licensed under [MIT License](http://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python/LICENSE).

[Product Page](https://products.groupdocs.cloud/viewer/python) | [Documentation](https://wiki.groupdocs.cloud/viewercloud/) | [API Reference](https://apireference.groupdocs.cloud/viewer/) | [Code Samples](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/viewer/) | [Free Support](https://forum.groupdocs.cloud/c/viewer) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
