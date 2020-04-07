Python Cloud SDK wraps GroupDocs.Comparison Cloud API so you could seamlessly integrate Document Comparison features into your own Python apps.

[GroupDocs.Comparison Cloud SDK for Python](https://products.groupdocs.cloud/comparison/python) helps developers implement document comparison for over 90 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe, CAD, markup & image file formats, and compare 2 similar documents to retrieve differences as a file or array of images. 

Check out the [API Reference](https://apireference.groupdocs.cloud/comparison/) to know all about the GroupDocs.Comparison REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

# Document Comparison in the Cloud

- Load password protected documents.
- [Fetch document changes](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-document-changes/) based on category, such as, change in numeric values only.
- Accept or reject retrieved changes.
- [Get the image stream of resultant document](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-stream-of-images-of-result-document-changes/).
- Detect changes in text style.
- Add summary page to resultant document after comparison.
- Show deleted components in the resultant document.

## New Features in Version 19.5

- This is the first release of a completely new version of the API `GroupDocs.Comparison.Cloud v2.0`.
- `V2` provides much simpler and intuitive API as compared to `V1`.
- `V2` includes Storage and File API which enables you to manage storage and files.
- Internal cloud solution is based on the modern micro-service architecture.

For the detailed notes, please visit [GroupDocs.Comparison Cloud 19.5 Release Notes](https://wiki.groupdocs.cloud/comparisoncloud/release-notes/2019/groupdocs-comparison-cloud-19-5-release-notes/).

## Compare Document Formats

GroupDocs.Comparison Cloud API [supports 90+ file formats](https://wiki.groupdocs.cloud/comparisoncloud/getting-started/supported-document-formats/) that it can load & compare.

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX, XLTM, XLTX, ODS, OTS, CSV, TSV
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POTM, POTX, ODP, OTP
**Microsoft Visio:** VDW, VDX, VSD, VSDML, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Microsoft Project:** MPP, MPT
**Microsoft OneNote:** ONE
**Email:** EML, EMLX, MSG, OST, PST
**Adobe Photoshop:** PSD
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**eBook:** EPUB, MOBI
**Image:** BMP, CGM, DCM, DJVU, DNG, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PNG, SVG, TIF, TIFF, WEBP
**Markup:** HTML, MHT, MHTML, XML
**Portable:** PDF, TEX, XPS
**Metafile:** EMF, WMF
**Other:** PCL, PS

## Getting Started with GroupDocs.Comparison Cloud SDK for Python

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-python). You can either directly use the source code or get PIP distribution via `pip install groupdocs-comparison-cloud`.

Execute following snippet to load supported formats.

```python
# Import module
import groupdocs_comparison_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_comparison_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    print("Supported file-formats:")
    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension))
except groupdocs_comparison_cloud.ApiException as e:
    print("Exception when calling get_supported_file_formats: {0}".format(e.message))
```

## Compare Spreadsheets via Cloud SDK for Python

```python
from __future__ import absolute_import

import unittest

from groupdocs_comparison_cloud import *
from test.test_context import TestContext
from test.test_file import TestFile, TestFiles

options = Options()
options.source_file = source.ToFileInfo()
options.output_path = "/resultFilePath/" + source.file_name

options = self.GetComparisonOptions(TestFiles.SourceCell, TestFiles.TargetCell)
response = self.compare_api.comparisons(ComparisonsRequest(options))
self.assertEqual(response.href, options.output_path)
```

## Licensing

GroupDocs.Comparison Cloud Python SDK licensed under [MIT License](http://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-python/LICENSE).

[Product Page](https://products.groupdocs.cloud/comparison/python) | [Documentation](https://wiki.groupdocs.cloud/comparisoncloud/) | [Live Demo](https://products.groupdocs.app/comparison/family) | [API Reference](https://apireference.groupdocs.cloud/comparison/) | [Code Samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/comparison/) | [Free Support](https://forum.groupdocs.cloud/c/comparison) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
