# Document Conversion Python REST API

This REST API allows your Python cloud-based apps to [convert documents](https://products.groupdocs.cloud/conversion/python) of [50+ file formats](https://wiki.groupdocs.cloud/conversioncloud/getting-started/supported-document-formats/) from within your apps without any 3rd party tool.

## Cloud Document Conversion Features

- Specify [document conversion settings](https://wiki.groupdocs.cloud/conversioncloud/developer-guide/data-structures/conversionsettings/).
- Specify page width & height while converting CAD diagrams.
- Choose specific CAD diagram layouts to be converted.
- Substitute specific fonts during cells document conversion.
- Convert specific cell range while converting to non-cell formats.
- Skip empty rows and columns when converting cells documents.
- Display or hide email header, "from", "to", "cc" & "bcc".
- Substitute specific fonts when converted some supported formats.
- Start converting from specified page number.
- Convert a specific number of pages from the specified page.
- Use PDF as an intermediary format while converting.
- Apply [watermark during conversion](https://wiki.groupdocs.cloud/conversioncloud/developer-guide/data-structures/convertoptions/) process.

## New Features Added in Version 20.2.0

- Support of encoding for source CSV and TXT documents.
- Added `TimeZoneOffset`, `ConvertAttachments` for source Email documents.

## Conversion File Formats

GroupDocs.Conversion Cloud SDK for Python allows you to convert any of the following type of file formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLS2003, XLSB, XLSM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX
**Microsoft Visio:** VDW, VDX, VSD, VSDX, VSS, VST, VSX, VTX
**Microsoft Project:** MPP, MPT
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**AutoCAD:** DWG, DXF
**Image:** BMP, GIF, ICO, JPEG, JPG, PNG, SVG, TIF, TIFF
**Email:** EML, EMLX, MSG
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML, MHT

to the following formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLS2003, XLSB, XLSM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**Image:** BMP, GIF, ICO, JPEG, JPG, PNG, TIF, TIFF
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML

## Conversion File Formats Added in Version 20.2.0

**Source Conversion Formats:** DIB, XLT, POT, XLAM, MPX, JPC, DWT, JPEG-LS
**Target Conversion Formats:** WMF, EMF, XLAM

## Platform Independence

GroupDocs.Conversion Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Installation

Install `groupdocs-conversion-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

`pip install groupdocs-conversion-cloud`

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

`python setup.py install`

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-python) for other common usage scenarios.

## Getting Started

Please follow the [installation procedure](https://pypi.org/project/groupdocs-conversion-cloud/#installation) and then run following:

```python
# Import module
import groupdocs_conversion_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_conversion_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported conversion types
    request = groupdocs_conversion_cloud.GetSupportedConversionTypesRequest()
    response = api.get_supported_conversion_types(request)

    # Print out supported conversion types
    print("Supported conversion types:")
    for format in response:
        print('{0} to [{1}]'.format(format.source_format, ', '.join(format.target_formats)))
except groupdocs_conversion_cloud.ApiException as e:
    print("Exception when calling get_supported_conversion_types: {0}".format(e.message))
```

## Convert DOCX Word Document to HTML using Python

```python
# Get your App SID and App Key at https://dashboard.groupdocs.cloud (free registration is required).

# Create instance of the API
api = groupdocs_conversion_cloud.ConversionApi.from_keys(app_sid, app_key)

settings = groupdocs_conversion_cloud.ConvertSettings()
settings.storage_name = "Storage Name"
settings.file_path = "document.docx"
settings.format = "html"

loadOptions = groupdocs_conversion_cloud.DocxLoadOptions()
loadOptions.password = "password"

settings.load_options = loadOptions;

convertOptions = groupdocs_conversion_cloud.HtmlConvertOptions()
convertOptions.fixed_layout = True
convertOptions.use_pdf = False

settings.convert_options = convertOptions
settings.output_path = "convertedDocs"

request = groupdocs_conversion_cloud.ConvertDocumentRequest(settings)
response = api.convert_document(request)
```

## Licensing

GroupDocs.Conversion Cloud Python SDK licensed under [MIT License](http://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-python/LICENSE).

[Product Page](https://products.groupdocs.cloud/conversion/python) | [Documentation](https://wiki.groupdocs.cloud/conversioncloud/) | [API Reference](https://apireference.groupdocs.cloud/conversion/) | [Code Samples](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/conversion/) | [Free Support](https://forum.groupdocs.cloud/c/conversion) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
