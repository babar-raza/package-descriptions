Python Cloud SDK wraps GroupDocs.Viewer Cloud API so you could seamlessly integrate Document Viewing features into your own Python apps.

[GroupDocs.Viewer Cloud SDK for Python](https://products.groupdocs.cloud/viewer/python) helps developers implement document merging for over 85+ file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Visio®, Project®, Adobe, markup & image file formats to view as HTML, PDF or images. 

Check out the [API Reference](https://apireference.groupdocs.cloud/viewer/) to know all about the GroupDocs.Viewer REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

# View Documents in the Cloud

- [Render documents pages](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/rendering-document-pages/) as images.
- Fetch the list of all installed fonts or delete the fonts cache.
- Download HTML page resources, e.g., images, CSS, fonts etc.
- Render document as PDF, HTML or image representation and download as ZIP.
- Fetch document information via various methods.
- Obtain list of links to document pages as HTML.
- Rotate and reorder document pages.
- Specify image quality while rendering PDF as HTML.
- Decrease the resultant file size by excluding fonts.
- Render specific sections of worksheets defined as "Print Area".
- Choose to include or exclude hidden content.
- Save result in [minified HTML and SVG](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/minification-of-html-and-svg/).
- Render documents [responsive HTML](https://wiki.groupdocs.cloud/viewercloud/developer-guide/document-pages/rendering-document-to-responsive-html/).
- Render email messages & Outlook data files.
- Integrated storage API.

## New Features in Version 19.5.0

- Improve Cloud products API Reference grouping.

For the detailed notes, please visit [GroupDocs.Viewer Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/viewercloud/release-notes/2019/groupdocs-viewer-cloud-19-5-release-notes/).

## Supported File Formats

GroupDocs.Viewer Cloud API [supports 85+ file formats](https://wiki.groupdocs.cloud/viewercloud/getting-started/supported-document-formats/) that it can load & render.

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

## Getting Started with GroupDocs.Viewer Cloud SDK for Python

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python). You can either directly use the source code or get PIP distribution via `pip install groupdocs-viewer-cloud`.

Execute following snippet to load supported document formats.

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
