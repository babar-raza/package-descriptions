Python Cloud SDK wraps Aspose.HTML REST API so you could seamlessly integrate markup-based file creation, manipulation & conversion features into your own Node.js applications.

[Aspose.HTML Cloud SDK for Python](https://products.aspose.cloud/html/python) offers its consumers to load markup of HTML, MHTML, XHTML, EPUB, XML & SVG formats from file, cloud storage or URL. The loaded document can be traversed or inspected via CSS selector & XPath query or can be converted to images, PDF as well as other supported markup formats. The HTML REST API also alows to extract images from the HTML and populate HTML template with data from JSON or XML. Feel free to explore the [Developer's Guide](https://docs.aspose.cloud/display/htmlcloud/Developer+Guide) for all usage scenarios. 

## HTML Processing Features

- Fetch HTML page along with its resources as a ZIP archive by providing page URL.
- Based on page URL, [retrieve all images of an HTML page as a ZIP package](https://docs.aspose.cloud/display/htmlcloud/Get+Images+from+HTML+document).
- Load data from local file to populate HTML document template.
- Use request body to [populate HTML document template](https://docs.aspose.cloud/display/htmlcloud/Populate+HTML+Document+Template+with+Data).
- Convert HTML page to numerous other file formats.

## New Features in Version 19.11

- Added following SEO analysis points in the current version:
  - detection of broken links.
  - validation of e-mail addresses.
  - checking of `IMG` tags for the absence of `ALT` attribute.
  - checking for duplicated `H1` elements.

For the detailed notes, please visit [Aspose.HTML Cloud 19.11 Release Notes](https://docs.aspose.cloud/display/htmlcloud/Aspose.HTML+Cloud+19.11+Release+Notes).

## Read & Write HTML Formats

HTML, XHTML, zipped HTML, zipped XHTML, MHTML, HTML containing SVG markup, Markdown, JSON

## Save HTML As

**Fixed Layout:** PDF, XPS
**Images:** TIFF, JPEG, PNG, BMP, GIF
**Other:** TXT, ZIP (images)

## Read Common Formats

**eBook:** EPUB
**Other:** XML, SVG

## Getting Started with Aspose.HTML Cloud SDK for Python

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `pip install aspose-html-cloud` from the command line to install Aspose.Email Cloud SDK for Python via PIP. 

## Convert HTML to Image from URL using Python

```python
import os
from asposehtmlcloud.configuration import Configuration
from asposehtmlcloud.api.html_api import HtmlApi
from asposehtmlcloud.rest import ApiException
from shutil import copy2
configuration = Configuration(apiKey="XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
                              appSid="XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
                              basePath="https://api.aspose.cloud/v3.0",
                              authPath="https://api.aspose.cloud/connect/token",
                              debug=True)
api = HtmlApi(configuration)

source_url = "https://stallman.org/articles/anonymous-payments-thru-phones.html"
try:

    # Convert url to image
    res = api.get_convert_document_to_image_by_url(
        source_url, out_format="jpeg", width=800, height=1000, left_margin=50, right_margin=100,
        top_margin=150, bottom_margin=200, resolution=300, folder="MY_REMOTE_FOLDER", storage=""
    )

    src = str(res)
    # Move to test folder
    if os.path.isfile(src):
        copy2(src, '/home/user/testfolder/')
        os.remove(src)
except ApiException as ex:
    print("Exception")
    print("Info: " + str(ex))
    raise ex
```

[Product Page](https://products.aspose.cloud/html/python) | [Documentation](https://docs.aspose.cloud/display/htmlcloud/Home) | [Demo](https://products.aspose.app/html/family) | [API Reference](https://apireference.aspose.cloud/html/) | [Examples](https://github.com/aspose-html-cloud/aspose-html-cloud-python) | [Blog](https://blog.aspose.cloud/category/html/) | [Free Support](https://forum.aspose.cloud/c/html) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
