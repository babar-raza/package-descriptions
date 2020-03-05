# Document Comparison Python REST API

This cloud REST API enhances your Python cloud apps to [compare two documents](https://products.groupdocs.cloud/comparison/python), fetch, accept or reject the changes. Supports 90+ file formats.

## Cloud Document Comparison Features

- [Compare two documents](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-changes/) and fetch changes.
- Fetch [document changes based on change category](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-changes-categories/), such as, numeric only.
- [Accept or reject the changes](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-document-changes/) that come up after document comparison.
- Get the [image stream of resultant document](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-stream-of-images-of-result-document-changes/) via JsonRequest object.
- Save the resultant document to streams as set of images.
- Get the resultant document path.
- Add summary page to resultant document after comparison.
- Show deleted components in the resultant document.
- Detect style changes.
- Get or set password to the the resultant document.

## Supported Document Formats

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

## Platform Independence

GroupDocs.Comparison Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Installation

Install `groupdocs-comparison-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

`pip install groupdocs-comparison-cloud`

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

`python setup.py install`

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-python) for other common usage scenarios.

## Getting Started

Please follow the [installation procedure](https://pypi.org/project/groupdocs-comparison-cloud/#installation) and then run following:

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

[Product Page](https://products.groupdocs.cloud/comparison/python) | [Documentation](https://wiki.groupdocs.cloud/comparisoncloud/) | [API Reference](https://apireference.groupdocs.cloud/comparison/) | [Code Samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/comparison/) | [Free Support](https://forum.groupdocs.cloud/c/comparison) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
