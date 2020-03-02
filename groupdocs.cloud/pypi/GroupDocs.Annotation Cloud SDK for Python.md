# Document Annotation Python REST API

This REST API enhances your Python cloud apps to [import, export & process text & figure annotations](https://products.groupdocs.cloud/annotation/python) within documents for [35+ file formats](https://wiki.groupdocs.cloud/annotationcloud/getting-started/supported-document-formats/).

## Cloud Document Annotation Features

- [Fetch document description](https://wiki.groupdocs.cloud/annotationcloud/developer-guide/document-information/) with meta data and coordinates of text on pages.
- Fetch annotation data from files of supported formats.
- Import annotation information from documents.
- [Export annotation information](https://wiki.groupdocs.cloud/annotationcloud/developer-guide/working-with-annotations/#HExportAnnotation) to a document and fetch it as a stream.
- Remove document annotations.
- Get image representation of the document pages.
- Render documents to PDF format with storage URL or stream output.
- Add or remove document or image annotations of various types.

## Supported Annotation Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF, TXT
**Microsoft Excel:** XLS, XLSX, XLSB, XLSX
**Microsoft PowerPoint:** PPT, PPTX, PPSX
**Microsoft Visio:** VSD, VDX, VSS, VSDM
**OpenOffice:** OTT, ODT, ODP, OTP
**Image:** JPEG, TIFF, BMP, GIF, DJVU
**Metafile:** EMF, WMF
**Email:** EML, EMLX, MSG
**Portable:** PDF
**Medical Imagery:** DICOM
**Markup:** HTML, MHTML
**AutoCAD:** CAD

## Supported Text Annotation Types

**Text annotation** – add comments to selected text.
**Text replacement** – highlight which text should be replaced with what.
**Text redaction** – hide confidential text.
**Strikeout/underline** – highlight text with strikethroughs/underlines.
**Typewriter** – add sticky notes with rich text.

## Supported Figure Annotation Types

**Area annotation** – add notes to an area highlighted with a rectangle.
**Point annotation** – add notes to any point in the document.
**Area redaction** – hide confidential parts of an image or text.
**Polyline** – draw freehand lines and shapes.
**Pointer/arrow** – drop arrows pointing to an object.
**Watermark** – create text-based watermark overlays.
**Distance** – measure the distance between any objects in a document.

## Platform Independence

GroupDocs.Annotation Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Installation

Install `groupdocs-annotation-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

`pip install groupdocs-annotation-cloud`

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

`python setup.py install`

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-python) for other common usage scenarios.

## Getting Started

Please follow the [installation procedure](https://pypi.org/project/groupdocs-annotation-cloud/#installation) and then run following:

```python
# Import module
import groupdocs_annotation_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_annotation_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    print("Supported file-formats:")
    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension))
except groupdocs_annotation_cloud.ApiException as e:
    print("Exception when calling get_supported_file_formats: {0}".format(e.message))
```

## Use Python Cloud SDK to Add Arrow Annotation

```python
# Import modules
from groupdocs_annotation_cloud import *
import groupdocs_annotation_cloud

from Common_Utilities.Utils import Common_Utilities


class Annotation_Python_Add_Area_Annotation:

    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_AnnotateApi_Instance()

        try:
            a1 = groupdocs_annotation_cloud.AnnotationInfo()
            a1.annotation_position = groupdocs_annotation_cloud.Point()
            a1.annotation_position.x = 852
            a1.annotation_position.y = 59.388262910798119
            a1.box = groupdocs_annotation_cloud.Rectangle()
            a1.box.x = 375.89276123046875
            a1.box.y = 59.388263702392578
            a1.box.width = 88.7330551147461
            a1.box.height = 37.7290153503418
            a1.page_number = 2
            a1.pen_color = 1201033
            a1.pen_style = 0
            a1.pen_width = 1
            a1.opacity = 0.7
            a1.type = "Area"
            a1.text = "This is area annotation"
            a1.creator_name = "Anonym A."

            request = PostAnnotationsRequest("annotationdocs\\ten-pages.docx", [a1])
            api.post_annotations(request)

            print("Expected response type is void: Area Annotation added.")
        except ApiException as e:
            print("Exception when calling AnnotateAPI: {0}".format(e.message))
```

## Licensing

GroupDocs.Annotation Cloud Python SDK licensed under [MIT License](http://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-python/LICENSE).

[Product Page](https://products.groupdocs.cloud/annotation/python) | [Documentation](https://wiki.groupdocs.cloud/annotationcloud/) | [API Reference](https://apireference.groupdocs.cloud/annotation/) | [Code Samples](https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/annotation/) | [Free Support](https://forum.groupdocs.cloud/c/annotation) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
