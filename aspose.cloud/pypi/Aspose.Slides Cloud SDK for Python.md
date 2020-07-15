Python Cloud SDK wraps Aspose.Slides REST API so you could seamlessly integrate PowerPoint® file generation, manipulation, conversion & inspection features into your own python applications.

[Aspose.Slides Cloud SDK for Python](https://products.aspose.cloud/slides/python) enhance your Node.js programs to create presentations in the cloud, pick and merge specific slides, split presentations, extract images from presentation in any of the supported file formats, extract & download slide notes, clone master slide information, and more. Please feel free to explore the [Developer's Guide](https://docs.aspose.cloud/display/slidescloud/Developer+Guide) for all possible usage scenarios. 

## Presentation Processing Features

- [Extract image from presentation](https://docs.aspose.cloud/display/slidescloud/Extract+image+by+a+particular+format+from+a+PowerPoint+Document) in any of the supported file formats.
- Copy layout side or [clone master slide](https://docs.aspose.cloud/display/slidescloud/Clone+MasterSlide+Information+from+a+PowerPoint+Presentation) from the source presentation.
- Process slides shapes, slides notes, placeholders, colors & font theme info.
- Programmatically create presentation from HTML & export it to various formats.
- Merge multiple presentations or [split single presentation](https://docs.aspose.cloud/display/slidescloud/Split+PowerPoint+Presentations) into multiple ones.
- Extract and replace text from specific slide or entire presentation.
- Full read & write access to Document Object Model, including slides, shapes, paragraphs, portions & more.
- Access presentation's metadata.

## New Features & Enhancements in Version 20.6

- Added method to check if the `NotesSilde` exists.
- Created separate endpoints for shape resources with empty `subshape` paths.
- Support for `FODP` save & load format.
- Support `PDF/A-1a` and `PDF/UA` options for `PdfCompliance` enumeration.

For the detailed notes, please visit [Aspose.Slides Cloud 20.6 Release Notes](https://docs.aspose.cloud/display/slidescloud/Aspose.Slides+Cloud+20.6+Release+Notes).

## Read & Write Presentation Formats

**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX, PPTM, PPSM, POTX, POTM
**OpenOffice:** ODP, OTP

## Save Presentations As

**Fixed Layout:** PDF, PDF/A, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Web:** HTML
**Other:** SWF (export whole presentations)

## Getting Started with Aspose.Slides Cloud SDK for Python

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `pip install aspose-slides-cloud` from the command line to fetch the SDK. The complete source code is available at [GitHub Repository](https://github.com/aspose-slides-cloud/aspose-slides-cloud-python).

## Convert PowerPoint to PDF via Python

```python
import asposeslidescloud

from asposeslidescloud.configuration import Configuration
from asposeslidescloud.apis.slides_api import SlidesApi
from asposeslidescloud.models.export_format import ExportFormat
from asposeslidescloud.models.requests.slides_api_requests import PostSlidesConvertRequest

configuration = Configuration()
configuration.app_sid = 'MyAppSid'
configuration.app_key = 'MyAppKey'
api = SlidesApi(configuration)

with open("MyPresentation.pptx", 'rb') as f:
	document = f.read()

request = PostSlidesConvertRequest(ExportFormat.PDF, document)
response = api.post_slides_convert(request)
print('My PDF was saved to ' + response)
```

[Product Page](https://products.aspose.cloud/slides/python) | [Documentation](https://docs.aspose.cloud/display/slidescloud/Home) | [Demo](https://products.aspose.app/slides/family) | [API Reference](https://apireference.aspose.cloud/slides/) | [Examples](https://github.com/aspose-slides-cloud/aspose-slides-cloud-python) | [Blog](https://blog.aspose.cloud/category/slides/) | [Free Support](https://forum.aspose.cloud/c/slides) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
