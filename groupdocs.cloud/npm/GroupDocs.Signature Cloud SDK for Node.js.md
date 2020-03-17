Node.js Cloud SDK wraps GroupDocs.Signature Cloud API so you could seamlessly integrate Document Signing features into your own Node.js apps.

# e-Sign Documents in the Cloud

[GroupDocs.Signature Cloud SDK for Node.js](https://products.groupdocs.cloud/signature/nodejs) helps developers implement document merging for over 40 file formats from diverse categories. It allows to load Microsoft Office®, OpenOffice, Adobe & image file formats to search, verify or add digital signatures. 

Check out the [API Reference](https://apireference.groupdocs.cloud/signature/) to know all about the GroupDocs.Signature REST API. Get your application information from [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) first so you could try different functions from Swagger UI.

## Supported Signature Types

- Text
- Image
- Barcode
- QR-code
- Digital
- Stamp

## Document Signing Features

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

## Supported File Formats

GroupDocs.Signature Cloud API [supports 35+ file formats](https://wiki.groupdocs.cloud/signaturecloud/getting-started/supported-document-formats/) that it can load & add barcode, image, QR-code, stamp or text signatures.

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP
**Image:** BMP, GIF, JPG, JPEG, PNG, SVG, TIF, TIFF, WEBP, DJVU
**Metafile:** WMF
**CorelDraw:** CDR, CMX
**Adobe Photoshop:** PSD
**Adobe Acrobat:** PDF

## Digital Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**OpenOffice:** ODS, OTS
**Adobe Acrobat:** PDF

## FormField Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**OpenOffice:** ODS, OTS, ODP
**Adobe Acrobat:** PDF

## Metadata Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP
**Image:** JPG, JPEG, PNG, SVG, TIF, TIFF
**Adobe Photoshop:** PSD
**Adobe Acrobat:** PDF

## Getting Started with GroupDocs.Signature Cloud SDK for Node.js

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-node). You can either directly use it in your project via source code or get NPM distribution via `npm install groupdocs-signature-cloud`.

Execute following snippet to load supported document formats.

```js
// load the module
var GroupDocs = require('groupdocs-signature-cloud');

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct SignatureApi
var config = new GroupDocs.Configuration(appSid, appKey);
config.apiBaseUrl = "https://api.groupdocs.cloud";

var infoApi = GroupDocs.InfoApi.fromConfig(config);

// retrieve supported file-formats
infoApi.getSupportedFileFormats()
    .then(function (response) {
        console.log("Supported file-formats:")
        response.formats.forEach(function (format) {
            console.log(format.fileFormat + " (" + format.extension + ")");
        });
    })
    .catch(function (error) {
        console.log("Error: " + error.message)
    });
```

Or compile and run same written in TypeScript:

```js
// load the module
import { InfoApi, Configuration } from "groupdocs-signature-cloud";

// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
const appSid: string = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
const appKey: string = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

// construct Api
const config = new Configuration(appSid, appKey);
config.apiBaseUrl = "https://api.groupdocs.cloud";

const infoApi = InfoApi.fromConfig(config);

// retrieve supported file-formats
infoApi.getSupportedFileFormats()
    .then((result) => {
        console.log("Supported file-formats:");
        result.formats.forEach((format) => {
            console.log(format.fileFormat + " (" + format.extension + ")");
        });
    })
    .catch((error) => {
        console.log("Error: " + error.message);
    });
```

## Use Node.js to Create New Signature in the Document

```js
public async createSignatures(requestObj: model.CreateSignaturesRequest): Promise<model.SignResult> {
        if (requestObj === null || requestObj === undefined) {
            throw new Error('Required parameter "requestObj" was null or undefined when calling createSignatures.');
        }

        const localVarPath = this.configuration.getServerUrl() + "/signature/create";
        const queryParameters: any = {};

        // verify required parameter 'requestObj.signSettings' is not null or undefined
        if (requestObj.signSettings === null || requestObj.signSettings === undefined) {
            throw new Error('Required parameter "requestObj.signSettings" was null or undefined when calling createSignatures.');
        }

        const requestOptions: request.Options = {
            method: "POST",
            qs: queryParameters,
            uri: localVarPath,
            json: true,
            body: Serializer.serialize(requestObj.signSettings, requestObj.signSettings.constructor.name === "Object" ? "SignSettings" : requestObj.signSettings.constructor.name),
        };

        const response = await invokeApiMethod(requestOptions, this.configuration);
        const result =  Serializer.deserialize(response.body, "SignResult");
        return Promise.resolve(result);
    }
```

## Licensing

GroupDocs.Signature Cloud Node.js SDK licensed under [MIT License](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-node/blob/HEAD/LICENSE).

[Product Page](https://products.groupdocs.cloud/signature/nodejs) | [Documentation](https://wiki.groupdocs.cloud/signaturecloud/) | [API Reference](https://apireference.groupdocs.cloud/signature/) | [Code Samples](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/signature/) | [Free Support](https://forum.groupdocs.cloud/c/signature) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
