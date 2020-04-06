Python Cloud SDK wraps GroupDocs.Conversion Cloud API so you could seamlessly integrate Document Conversion features into your own Python apps.

[GroupDocs.Conversion Cloud SDK for Python](https://products.groupdocs.cloud/conversion/python) helps developers implement document conversion for over 50 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe, CAD, markup & image file formats, and export to various other formats. 

Check out the [API Reference](https://apireference.groupdocs.cloud/conversion/) to know all about the GroupDocs.Conversion REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try it from Swagger UI.

## Document Conversion in the Cloud

- Load password protected documents.
- Protect destination document (if supported).
- Convert specific document pages.
- Convert N consecutive pages.
- Add watermark to destination document.
- Get document metadata.
- Get possible conversion options for any input document.
- Use PDF as an intermediary format while converting.
- Integrated storage API.

## Document Specific REST Models

- Convert specific cell range, skip empty rows & columns or substitute font during Excel document conversion.
- Display or hide email headers like "from", "to", "cc" & "bcc".
- Adjust resolution, contrast, brightness or gamma for image conversion. Also rotate, flip or convert to grayscale.
- Set page's DPI & zoom level while converting Word documents.
- Render specific CAD layouts.

## New Features in Version 20.2

- **New Source Formats:** DIB, XLT, POT, XLAM, MPX, JPC, DWT, JPEG-LS.
- **New Target Formats:** WMF, EMF, XLAM.
- Supports encoding for source `CSV` and `TXT` documents.
- Supports `TimeZoneOffset` and `ConvertAttachments` for source Email documents.

## Enhancements in Version 20.2

- Improved quality of Diagram to Word document conversion.
- Converting multi-page `TIFF` to `PDF`.
- Improvement in `MPP` to `XLS` conversion.

For the detailed notes, please visit, [GroupDocs.Conversion Cloud 20.2 Release Notes](https://wiki.groupdocs.cloud/conversioncloud/release-notes/2020/groupdocs-conversion-cloud-20-2-release-notes/).

## Conversion File Formats

GroupDocs.Conversion Cloud SDK for PythonET allows you to convert any of the following type of file formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLT, XLS2003, XLSB, XLSM, XLAM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX, POT
**Microsoft Visio:** VDW, VDX, VSD, VSDX, VSS, VST, VSX, VTX
**Microsoft Project:** MPP, MPT, MPX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**AutoCAD:** DWG, DWT, DXF
**Image:** BMP, GIF, ICO, JPEG, JPEG-LS, JPG, JPC, PNG, SVG, TIF, TIFF, DIB
**Email:** EML, EMLX, MSG
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML, MHT

to the following formats:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, RTF, TXT
**Microsoft Excel:** XLS, XLS2003, XLSB, XLSM, XLAM, XLSX, CSV
**Microsoft PowerPoint:** PPS, PPSX, PPT, PPTX
**OpenOffice:** ODP, ODS, ODT, OTT
**Adobe Photoshop:** PSD
**Image:** BMP, GIF, ICO, JPEG, JPG, PNG, TIF, TIFF
**Fixed Layout:** PDF, XPS
**Markup:** HTM, HTML
**Metafile:** WMF, EMF

## Getting Started with GroupDocs.Conversion Cloud SDK for Python

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-conversion-cloud/groupdocs-conversion-cloud-python). You can either directly use it in your project via source code or get PIP distribution as `pip install groupdocs-conversion-cloud`.


Execute following snippet to load all supported conversion formats.

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
