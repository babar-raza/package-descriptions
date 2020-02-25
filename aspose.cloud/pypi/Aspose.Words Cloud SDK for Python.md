This cloud SDK provides seamless integration of cloud document processing & manipulation features into your cloud-based Python apps.

Aspose.Words Cloud SDK for Python is built on top of Aspose.Words REST API and is provided to you under an MIT license. Using Aspose.Words Cloud SDK for Python, you can work with document comparison, headers, footers, page numbering, tables, sections, document comments, drawing objects, FormFields, fonts, hyperlinks, ranges, paragraphs, math objects, watermarks, track changes and document protection. Aspose.Words Cloud SDK for Python also assists you in appending documents, splitting documents as well as converting document into other supported file formats.

## Document Processing Features

- Programmatically create new documents of various file formats.
- Fetch a web page via its URL and save it in Microsoft Word file format.
- Get document information, by default, in JSON/XML representation.
- [Fetch statistical data](https://docs.aspose.cloud/display/wordscloud/Get+Document+Statistics) of a document.
- Render complex elements (table, DrawingObject etc.) of the document in supported formats.
- [Remove all macros](https://docs.aspose.cloud/display/wordscloud/Remove+all+Macros+from+Document) contained in a specific document.
- [Convert a document to desired file format](https://docs.aspose.cloud/display/wordscloud/Convert+Document+to+Destination+Format+with+Detailed+Settings+and+Save+Result+to+Storage) along with detailed settings.
- Convert an encrypted PDF document into MS Word document format.
- So many more features.

## Read & Write Document Formats

**Microsoft Word:** DOC, DOCX, RTF, DOT, DOTX, DOTM, FlatOPC (XML)
**OpenOffice:** ODT, OTT
**WordprocessingML:** XML
**Web:** HTML, MHTML, HtmlFixed
**Text:** TXT
**Fixed Layout:** PDF

## Save Document As

**Fixed Layout:** PDF/A, XPS, OpenXPS, PS
**Images:** JPEG, PNG, BMP, SVG, TIFF, EMF
**Others:** PCL

## Platform Independence

Aspose.Words Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.Words Cloud SDK for Python

You do not need to install anything to get started with Aspose.Words Cloud SDK for Python. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

You can use it directly in your project via the source code or get its PyPI Package, `pip install aspose-words-cloud`. The complete source code is available at the [GitHub Repository](https://github.com/aspose-words-cloud/aspose-words-cloud-python).

## Convert document to the specified format via Python

```python
kwargs['_return_http_data_only'] = True
    try:
        if kwargs.get('is_async'):
            return self.convert_document_with_http_info(request, **kwargs)  # noqa: E501
        (data) = self.convert_document_with_http_info(request, **kwargs)  # noqa: E501
        return data
    except ApiException as e:
        if e.status == 401:
            self.__request_token()
            if kwargs.get('is_async'):
                return self.convert_document_with_http_info(request, **kwargs)  # noqa: E501
        (data) = self.convert_document_with_http_info(request, **kwargs)  # noqa: E501
        return data
```

[Product Page](https://products.aspose.cloud/words/python) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [API Reference](https://apireference.aspose.cloud/words/) | [Code Samples](https://github.com/aspose-words-cloud/aspose-words-cloud-python) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
