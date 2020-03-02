# Text & Document Classification Python REST API

This cloud REST API enables your Python apps to [perform classification of raw text & documents](https://products.groupdocs.cloud/classification/python). Supports [IAB-2 & Documents taxonomies](https://wiki.groupdocs.cloud/classificationcloud/developer-guide/common-resources/taxonomy/).

## Classification Processing Features

- Perform [raw text classification](https://wiki.groupdocs.cloud/classificationcloud/developer-guide/raw-text-classification/).
- Perform [document classification](https://wiki.groupdocs.cloud/classificationcloud/developer-guide/documents-classification/) for the supported file formats.

## Supported Document Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM
**OpenOffice:** ODT, OTT
**Portable:** PDF
**Other:** RTF, TXT

## Supported IAB-2 Taxonomy

'Automotive',
'Books_and_Literature',
'Business_and_Finance',
'Careers',
'Education',
'Events_and_Attractions',
'Family_and_Relationships',
'Fine_Art',
'Food_&_Drink',
'Healthy_Living',
'Hobbies_&_Interests',
'Home_&_Garden',
'Medical_Health',
'Movies',
'Music_and_Audio',
'News_and_Politics',
'Personal_Finance',
'Pets',
'Pop_Culture',
'Real_Estate',
'Religion_&_Spirituality',
'Science',
'Shopping',
'Sports',
'Style_&_Fashion',
'Technology_&_Computing',
'Television',
'Travel',
'Video_Gaming'

## Supported Documents Taxonomy

ADVE - advertisements, brochures.
Email
Form
Letter
Memo - memorandums.
News - articles, including news articles.
Invoice
Report
Resume
Scientific - scientific papers.
Other - the other classes of documents or cases where the classifier is not sure.

## Platform Independence

GroupDocs.Classification Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Installation

If the python package is hosted on [Github](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-python), you can install directly from Github:

`pip install groupdocsclassificationcloud`

(you may need to run `pip` with root permission: `sudo pip install groupdocsclassificationcloud`)

Then import the package:

`import groupdocsclassificationcloud`

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

`python setup.py install --user`

(or `sudo python setup.py install` to install the package for all users)

Then import the package:

`import groupdocsclassificationcloud`

## Getting Started

Please follow the installation procedure and then run the following:

```python
import os
from groupdocsclassificationcloud.configuration import Configuration
from groupdocsclassificationcloud.apis.classification_api import ClassificationApi, classify_request
from groupdocsclassificationcloud.models import BaseRequest


class Classification(object):
    APP_SID = '' # Put your appSid here
    APP_KEY = '' # Put your appKey here

    def __init__(self):
        self.classification_api = ClassificationApi(configuration=Configuration(Classification.APP_SID,
                                                                                Classification.APP_KEY))

    # Classify text with IAB-2 taxonomy (Default)
    def classify_raw_text(self):
        request = classify_request(BaseRequest("Try text classification"))

        result = self.classification_api.classify(request)
        print("Result {}".format(result))


classification = Classification()
classification.classify_raw_text()
```

[Test](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-python/blob/master/test) contain various examples of using the SDK. Please put your credentials into [Configuration](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-python/blob/master/groupdocsclassificationcloud/configuration.py).

## Dependencies

- Python 2.7 and 3.4+
- referenced packages (see [here](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-python/blob/master/setup.py) for more details)

## Get Supported File Formats using Python

```python
kwargs['_return_http_data_only'] = True
    try:
        if kwargs.get('is_async'):
            return self.get_supported_file_formats_with_http_info(request, **kwargs)  # noqa: E501
        (data) = self.get_supported_file_formats_with_http_info(request, **kwargs)  # noqa: E501
        return data
    except ApiException as e:
        if e.status == 401:
            self.__request_token()
            if kwargs.get('is_async'):
                return self.get_supported_file_formats_with_http_info(request, **kwargs)  # noqa: E501
        (data) = self.get_supported_file_formats_with_http_info(request, **kwargs)  # noqa: E501
        return data
```

[Product Page](https://products.groupdocs.cloud/classification/python) | [Documentation](https://wiki.groupdocs.cloud/classificationcloud/) | [API Reference](https://apireference.groupdocs.cloud/classification/) | [Code Samples](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/classification/) | [Free Support](https://forum.groupdocs.cloud/c/classification) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
