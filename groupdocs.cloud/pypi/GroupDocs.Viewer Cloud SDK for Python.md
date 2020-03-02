This REST API enhances your C#, ASP.NET, & other .NET based cloud apps to render 85+ types of file formats to image, PDF or HTML formats from within your apps.

## Cloud Document Viewer Features

- Support for rendering lots of document and image file formats.
- Fetch the list of all installed fonts or delete the fonts cache.
- Download HTML page resources, e.g., images, css, fonts etc.
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

## Installation

Install `groupdocs-viewer-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

`pip install groupdocs-viewer-cloud`

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

`python setup.py install`

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository]() for other common usage scenarios.

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

## [HEADING]

```python

```

## Licensing

GroupDocs.Viewer Cloud Python SDK licensed under [MIT License](http://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python/LICENSE).


[Product Page]() | [Documentation](https://wiki.groupdocs.cloud/viewercloud/) | [API Reference](https://apireference.groupdocs.cloud/viewer/) | [Code Samples]() | [Blog](https://blog.groupdocs.cloud/category/viewer/) | [Free Support](https://forum.groupdocs.cloud/c/viewer) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
