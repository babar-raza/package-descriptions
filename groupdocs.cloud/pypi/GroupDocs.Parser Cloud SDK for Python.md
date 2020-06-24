# Document Parser Python Cloud REST API

This [document parser & data extraction REST API](https://products.groupdocs.cloud/parser/python) can be used to enhance your Python cloud-based applications to perform parsing operations.

## Cloud Document Parser Features

- Create easy to define templates with data field and table definitions.
- Parse documents with pre-defined templates.
- Extract data from invoices or from other sort of documents.
- Supports extracting text and images.
- Extract data from regular documents as well as from email or archive containers.
- Obtain data from PDF portfolios.
- Fetch text fields, numbers and tables from common documents.
- Save your templates in the storage and parse your documents with them.
- Ability to extract HTML or Markdown (MD) text for a quick preview.
- Fetch specific pages of plain as well as formatted text.
- Extract formatted (bold, italic, hyperlink etc.) text in the MD format.
- Support for extracting text in HTML formatting (paragraph, hyperlinks, lists etc.).
- Retrieve all images from a document and save them.
- Obtain basic information about documents, archives, emails, and attachments etc.
- Extract data from a document contained inside a ZIP archive, email or PDF portfolio.

## New Features & Enhancements in Version 20.6

- Added `Node.js`, `PHP`, `Python`, and `Ruby` SDK for GroupDocs.Parser Cloud.
- Implemented extraction of encoding.
- Implemented additional image information extraction.

For the detailed notes, pelase visit [GroupDocs.Parser for Cloud 20.6 Release Notes](https://wiki.groupdocs.cloud/parsercloud/release-notes/release-notes-2020/groupdocs-parser-for-cloud-20-6-release-notes).

## Parse Document By Template Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF

## Extract Text Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Emails:** EML, EMLX, MSG
**Notes:** ONE

## Extract Document Info Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Emails:** PST, OST, EML, EMLX, MSG
**Notes:** ONE
**Archives:** ZIP

## Extract Images Supported Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, ODS, OTS, CSV, XLA, XLAM, NUMBERS
**Presentation:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP, OTP
**Portable:** PDF
**Emails:** EML, EMLX, MSG
**Archives:** ZIP

## Extract Container Items Info Supported Formats

**Portable:** PDF
**Emails:** PST, OST, EML, EMLX, MSG
**Archives:** ZIP

## Getting Started

You do not need to install anything to get started with GroupDocs.Parser Cloud SDK for Python. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Please check the [GitHub Repository](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-python-samples) for other common usage scenarios.

## Requirements

Python 2.7 or 3.4+

## Installation

Install `groupdocs-parser-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

```shell
pip install groupdocs-parser-cloud
```

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

```shell
python setup.py install
```

Please follow the [installation procedure](#installation) and then run following:

```python
# Import module
import groupdocs_parser_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_parser_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    print("Supported file-formats:")
    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension)) 
except groupdocs_parser_cloud.ApiException as e:
    print("Exception when calling get_supported_file_formats: {0}".format(e.message))
```

## Prerequisites

- Python with PIP installed
- Get your `AppSID` and `AppKey` at [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud) (free registration is required).

## How to Run the Examples

The package contains Python examples. Follow the given steps to proceed run:

- Extract the downloaded project..
- Go to "Examples" directory of the project.
- Edit `RunExamples.py` and put there `appSid` and `appKey`, obtained from [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud).
- Execute `pip install groupdocs_parser_cloud` command.
- Run examples using `python RunExamples.py` command.

For more details, please visit [Getting Started](https://docs.groupdocs.cloud/display/parsercloud/Getting+Started).

[Product Page](https://products.groupdocs.cloud/parser/python) | [Documentation](https://wiki.groupdocs.cloud/parsercloud/) | [Demo](https://products.groupdocs.app/parser/family) | [API Reference](https://apireference.groupdocs.cloud/parser/) | [Examples](https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-python-samples) | [Blog](https://blog.groupdocs.cloud/category/parser/) | [Free Support](https://forum.groupdocs.cloud/c/parser) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
