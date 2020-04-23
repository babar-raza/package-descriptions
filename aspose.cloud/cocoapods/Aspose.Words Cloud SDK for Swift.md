# Swift REST API for Cloud Document Processing

This cloud SDK provides seamless integration of [cloud document processing & manipulation features](https://products.aspose.cloud/words/swift) into your cloud-based Swift apps.

## Document Processing Features

- Programmatically create new documents of various file formats.
- Fetch a web page via its URL and save it in Microsoft Word file format.
- Get document information, by default, in JSON/XML representation.
- Fetch statistical data of a document.
- Render complex elements (table, DrawingObject etc.) of the document in supported formats.
- Remove all macros contained in a specific document.
- Convert a document to desired file format along with detailed settings.
- Convert an encrypted PDF document into MS Word document format.
- So many more features.

## New Features in Version 20.4

- Added `UseTargetMachineFonts` option to `HtmlFixedSaveOptions` Data.
- Added `Password` option to `OdtSaveOptions`.
- Provision of Compare Options in Aspose.Words Cloud.
- Added new `SaveOptionsData.UpdateLastPrintedProperty`.
- Added new Saveoption Dml3DEffectsRenderingMode.
- Added new PdfSaveOption "InterpolateImages".

For the detailed notes, please visit [Aspose.Words Cloud 20.4 Release Notes](https://docs.aspose.cloud/display/wordscloud/Aspose.Words+Cloud+20.4+Release+Notes).

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

## How to use the SDK

The complete source code is available in this repository folder. You can either directly use it in your project via source code or add this repository as dependency (recommended). For more details, please visit our [documentation website](https://docs.aspose.cloud/display/wordscloud/Available+SDKs).

## Prerequisites

To use Aspose Words Cloud SDK for Swift you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://dashboard.aspose.cloud/#/apps).

## Installation & Usage

Add link to this repository as dependency to your Package.swift:

```swift
dependencies: [
    // Dependencies declare other packages that this package depends on.
    .package(url: "https://github.com/aspose-words-cloud/aspose-words-cloud-swift", from: "20.4"),
],
targets: [
    // Targets are the basic building blocks of a package. A target can define a module or a test suite.
    // Targets can depend on other targets in this package, and on products in packages which this package depends on.
    .target(
        name: "YourTargetName",
        dependencies: ["AsposeWordsCloud"]
    ),
]
```

## Getting Started

```swift
import Foundation;
import AsposeWordsCloud;

let wordsApi = WordsAPI(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY");
let fileName = "TestCreateDocument.doc";
let request = CreateDocumentRequest(fileName: fileName);
let response = try wordsApi.createDocument(request: request);
```

## Tests

[Tests](https://github.com/aspose-words-cloud/aspose-words-cloud-swift/blob/master/Tests/AsposeWordsCloudTests) contain various examples of using the SDK. Please put your credentials into "Settings/servercreds.json" for run tests.

## Dependencies

- Swift 4.2+
- referenced packages (see [here](https://github.com/aspose-words-cloud/aspose-words-cloud-swift/blob/master/Tests/AsposeWordsCloudTests) for more details)

## Licensing

All Aspose.Words Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-words-cloud/aspose-words-cloud-swift/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/words/swift) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [Demo](https://products.aspose.app/words/family) | [API Reference](https://apireference.aspose.cloud/words/) | [Examples](https://github.com/aspose-words-cloud/aspose-words-cloud-swift) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
