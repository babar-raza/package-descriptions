Python Cloud SDK wraps Aspose.PDF REST API so you could seamlessly integrate PDF file creation, manipulation & conversion features to your own Python applications.

[Aspose.PDF Cloud SDK for Python](https://products.aspose.cloud/pdf/python) allows the developers to generate new PDF documents & pages, delete pages from existing PDF files as well as manage PDF bookmarks, annotations, signatures, stamps, watermarks, attachments, header, footer, hyperlinks, form fields, text items and images via simple REST API calls. Please feel free to explore the [Developer's Guide](https://docs.aspose.cloud/display/pdfcloud/Developer+Guide) for all possible usage scenarios. 

## PDF Processing Features

- Add PDF document's header & footer in text or image format.
- Add tables & stamps (text or image) to PDF documents.
- [Append multiple PDF documents](https://docs.aspose.cloud/display/pdfcloud/Append+PDF+Files) to an existing file.
- Work with PDF attachments, annotations, & form fields.
- Apply [encryption or decryption to PDF documents](https://docs.aspose.cloud/display/pdfcloud/Encrypting+and+Decrypting+PDF+Documents) & set password.
- Delete all stamps & tables from a page or entire PDF document.
- Delete a specific stamp or table from the PDF document by its ID.
- Replace a single or multiple instances of a text on a PDF page or from entire document.
- Extensive support for [converting PDF documents](https://docs.aspose.cloud/display/pdfcloud/Convert+PDF+to+Other+File+Formats) to various other file formats.
- Extract various elements of PDF file & make PDF document optimized.

## New Features & Enhancements in Version 20.7

- Added Support for `PDF_A_3A` Format.
- Added Support of `MaxResolution` option in `OptimizeOption`.
- Added Support of `ImageCompressionOptions` in `OptimizeOptions`.
- Implemented Info action.

For the detailed notes, please visit [Aspose.PDF Cloud 20.7 Release Notes](https://docs.aspose.cloud/display/pdfcloud/Aspose.PDF+Cloud+20.7+Release+Notes).

## Read & Write Formats

PDF, EPUB, HTML, TeX, SVG, XML, XPS, FDF, XFDF

## Save PDF Documents As

XLS, XLSX, PPTX, DOC, DOCX, MobiXML, JPEG, EMF, PNG, BMP, GIF, TIFF, Text

## Read Formats

MHT, PCL, PS, XSLFO, MD

## Getting Started with Aspose.PDF Cloud SDK for Python

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `pip install aspose-pdf-cloud` from the command line to fetch the SDK. The complete source code is available at [GitHub Repository](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-python).

## Convert PDF to HTML Zipped Archive using Python

```python
from configuration import *
file_name = 'template.pdf'
result_file_name = "output.zip"

opts = {
    "file": test_data_path + file_name
}

response = pdf_api.put_pdf_in_request_to_html(
    temp_folder + '/' + result_file_name, **opts)

pprint(response)
```

[Product Page](https://products.aspose.cloud/pdf/python) | [Documentation](https://docs.aspose.cloud/display/pdfcloud/Home) | [Demo](https://products.aspose.app/pdf/family) | [API Reference](https://apireference.aspose.cloud/pdf/) | [Examples](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-python) | [Blog](https://blog.aspose.cloud/category/pdf/) | [Free Support](https://forum.aspose.cloud/c/pdf) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
