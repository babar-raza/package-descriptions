This REST API enables your Python cloud-based apps to process & manipulate PPT, PPTX, ODP, OTP presentations in the cloud.

Aspose.Slides Cloud SDK for Python is a wrapper around Aspose.Slides REST API and is offered under an MIT license. Enhance your Python programs to create presentations in the cloud, pick and merge specific slides, split presentations, extract images from presentation in any of the supported file formats, extract & download slide notes, clone master slide information, and so much more.

## Presentation Processing Features

- [Extract image from presentation](https://docs.aspose.cloud/display/slidescloud/Extract+image+by+a+particular+format+from+a+PowerPoint+Document) in any of the supported file formats.
- Copy layout side or [clone master slide](https://docs.aspose.cloud/display/slidescloud/Clone+MasterSlide+Information+from+a+PowerPoint+Presentation) from the source presentation.
- Process slides shapes, slides notes, placeholders, colors & font theme info.
- Programmatically create presentation from HTML & export it to various formats.
- Merge multiple presentations or [split single presentation](https://docs.aspose.cloud/display/slidescloud/Split+PowerPoint+Presentations) into multiple ones.
- Extract and replace text from specific slide or entire presentation.

## Read & Write Presentation Formats

**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX, PPTM, PPSM, POTX, POTM
**OpenOffice:** ODP, OTP

## Save Presentation As

**Fixed Layout:** PDF, PDF/A, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Web:** HTML
**Other:** SWF (export whole presentations)

## Platform Independence

Aspose.Slides Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.Slides Cloud SDK for Python

You do not need to install anything to get started with Aspose.Slides Cloud SDK for Python. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

You can use it directly in your project via the source code or get its PyPI Package, `pip install aspose-slides-cloud`. The complete source code is available at the [GitHub Repository](https://github.com/aspose-slides-cloud/aspose-slides-cloud-python).

## Use Python Code to Split Presentation Slides

```python
kwargs['_return_http_data_only'] = True
if kwargs.get('is_async'):
    return self.post_slides_split_with_http_info(request, **kwargs)  # noqa: E501
else:
    (data) = self.post_slides_split_with_http_info(request, **kwargs)  # noqa: E501
    return data
```

[Product Page](https://products.aspose.cloud/slides/python) | [Documentation](https://docs.aspose.cloud/display/slidescloud/Home) | [API Reference](https://apireference.aspose.cloud/slides/) | [Code Samples](https://github.com/aspose-slides-cloud/aspose-slides-cloud-python) | [Blog](https://blog.aspose.cloud/category/slides/) | [Free Support](https://forum.aspose.cloud/c/slides) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
