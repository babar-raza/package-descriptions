Python Cloud SDK wraps GroupDocs.Classification Cloud API so you could seamlessly integrate Document Classification features into your own Python apps.

[GroupDocs.Classification Cloud SDK for Python](https://products.groupdocs.cloud/classification/python) helps developers implement document classification for over 10 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, PDF & text files to classify based on IAB-2 & document taxonomies. 

Check out the [API Reference](https://apireference.groupdocs.cloud/classification/) to know all about the GroupDocs.Classification REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## Classification Processing Features

- Perform [raw text classification](https://wiki.groupdocs.cloud/classificationcloud/developer-guide/raw-text-classification/).
- Perform [document classification](https://wiki.groupdocs.cloud/classificationcloud/developer-guide/documents-classification/) for the supported file formats.

## Supported Document Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM
**OpenOffice:** ODT, OTT
**Portable:** PDF
**Other:** RTF, TXT

## Supported IAB-2 Taxonomies

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

## Supported Document Taxonomies

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

## Getting Started with GroupDocs.Classification Cloud SDK for Python

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-python). You can either directly use the source code or get PIP distribution via `pip install groupdocsclassificationcloud`.

Execute following snippet to get started.

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

## Classify Document using Python

```python
from __future__ import absolute_import

from os.path import join
import unittest

from groupdocsclassificationcloud import BaseRequest, ClassifyRequest, FileInfo
from test import BaseTestContext

filename = 'test_multi_pages.docx'
file_path = join(self.local_common_folder, filename)
    with open(file_path, 'rb') as f:
        file_data = f.read()

file_upload_response = self.storage_api.put_create(self.remote_test_folder + '/' + filename, file_data)
# Check if file uploaded successfully to Cloud Storage
if (file_upload_response["code"] == 200 and file_upload_response["status"] == "OK"):
    request = ClassifyRequest(BaseRequest(document=FileInfo(name=filename, folder=self.remote_test_folder)))
    result = self.classification_api.classify(request)
    print("Result {}".format(result))

request = ClassifyRequest(BaseRequest("Try text classification"), 3)
result = self.classification_api.classify(request)
print(result)
```

[Product Page](https://products.groupdocs.cloud/classification/python) | [Documentation](https://wiki.groupdocs.cloud/classificationcloud/) | [API Reference](https://apireference.groupdocs.cloud/classification/) | [Examples](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/classification/) | [Free Support](https://forum.groupdocs.cloud/c/classification) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
