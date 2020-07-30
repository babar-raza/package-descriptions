Python Cloud SDK wraps GroupDocs.Signature Cloud API so you could seamlessly integrate Document Signing features into your own Python apps.

[GroupDocs.Signature Cloud SDK for Python](https://products.groupdocs.cloud/signature/python) helps developers implement document merging for over 40 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe & image file formats to search, verify or add digital signatures. 

Check out the [API Reference](https://apireference.groupdocs.cloud/signature/) to know all about the GroupDocs.Signature REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## e-Sign Documents in the Cloud

- Specify pages (even, odd, specific etc.) to apply the signature.
- Configure page padding options.
- Specify font, color, alignment & other appearance settings for the signature.
- Apply crop settings for the signature background.
- Setting to repeat the signature string to fill the specified area.
- Supports `CryptoApi` & `XmlDsig` methods of digital signatures.
- Configure alignment of text string along the barcode type signature.
- Support for various types of brushes to perform signature formatting.
- Apply signature to password-protected documents.
- Perform document signature verification.
- Get or set the time at which the document was digitally signed.
- Option to search some type of signatures from the document.

## New Features & Enhancements in Version 20.7

- Added support for new file formats.
- Implemented `Z-Order` for Text Signature.
- Implemented border for Image Signature.
- Ability to set up additional properties for digital signatures.
- `Opacity` option has been renamed to `Transparency`.
- `Border` options replaced with `BorderLine` class.

For the detailed notes, please visit [GroupDocs.Signature Cloud 20.7 Release Notes](https://wiki.groupdocs.cloud/signaturecloud/release-notes/release-notes-2020/groupdocs-signature-cloud-20-7-release-notes/).

## Signature Supported File Formats

The following file formats are supported for the image, stamp and text type of signatures:

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POT, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, ODP
**Image:** JPG, PNG, BMP, GIF, TIFF, CDR
**Rich Text:** RTF
**Adobe Acrobat:** PDF

## Digital Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** PPTM, PPTX
**OpenOffice:** ODT
**Adobe Acrobat:** PDF

## Barcode Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLT, XLTX, XLTM
**Microsoft PowerPoint:** POT, POTM, PPSX, PPTX
**OpenOffice:** ODT, ODP, ODS, OTT
**Image:** JPG, PNG, BMP, GIF, TIFF, CDR
**Rich Text:** RTF
**Adobe Acrobat:** PDF

## QR-Code Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSM, XLT, XLTX, XLTM
**OpenOffice:** OTT
**Image:** JPG, PNG, BMP, GIF, TIFF, CDR
**Rich Text:** RTF
**Adobe Acrobat:** PDF

## Supported Signature Types

- Text
- Image
- Barcode
- QR-code
- Digital
- Stamp

## Getting Started with GroupDocs.Signature Cloud SDK for Python

The complete source code is available at the [GitHub Repository](hhttps://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-python). You can either directly use the source code or get PIP distribution via `pip install groupdocs-signature-cloud`.

Execute following snippet to load supported document formats.

```python
# Import module
import groupdocs_signature_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_signature_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    print("Supported file-formats:")
    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension)) 
except groupdocs_signature_cloud.ApiException as e:
    print("Exception when calling get_supported_file_formats: {0}".format(e.message))
```

## Use Python SDK to Search Barcode Signature in a Spreadsheet

```python
# Import module
from groupdocs_signature_cloud.rest import ApiException
from Common_Utilities.Utils import Common_Utilities
from groupdocs_signature_cloud.models.cells_search_barcode_options_data import CellsSearchBarcodeOptionsData
from groupdocs_signature_cloud.models.requests.post_search_barcode_from_url_request import PostSearchBarcodeFromUrlRequest

class Search_Signature_Barcode_From_Url:

    @staticmethod
    def Post_Search_Signature_Barcode_From_Url():

        try:
            # Getting instance of the API
            api = Common_Utilities.Get_SignatureApi_Instance();

            Url = "https://www.dropbox.com/s/o9k7gweapq8k15l/SignedForVerificationAll.xlsx?dl=1"
            password = ""

            options = CellsSearchBarcodeOptionsData()

            # set barcode properties
            options.barcode_type_name ="Code39Standard"
            options.text = "12345678"
            # set match type
            options.match_type ="Contains"
            #set pages for search
            options.document_page_number = 1

            request = PostSearchBarcodeFromUrlRequest(Url, options, password, Common_Utilities.storage_name)

            response = api.post_search_barcode_from_url(request)

            print("Searched Count: " + str(len(response.signatures)));

        except ApiException as e:
            print("Exception when calling SignatureApi: {0}".format(e.message))
```

## Licensing

GroupDocs.Signature Cloud Python SDK licensed under [MIT License](http://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-python/LICENSE).

[Product Page](https://products.groupdocs.cloud/signature/python) | [Documentation](https://wiki.groupdocs.cloud/signaturecloud/) | [Demo](https://products.groupdocs.app/signature/family) | [API Reference](https://apireference.groupdocs.cloud/signature/) | [Examples](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/signature/) | [Free Support](https://forum.groupdocs.cloud/c/signature) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
