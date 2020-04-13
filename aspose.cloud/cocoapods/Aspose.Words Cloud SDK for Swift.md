# .NET REST API for Spreadsheet Processing in Cloud

This Cloud SDK enhances your Swift cloud-based apps to [process & manipulate Microsoft Excel spreadsheets](https://products.aspose.cloud/words/swift) in the cloud, without MS Office.

## Spreadsheet Processing Features

- Add, update or delete charts, worksheet pictures, shapes, hyperlinks & validations.
- Add or remove cells area for conditional formatting, or OleObjects from Excel worksheets.
- Insert or delete, horizontal or vertical page breaks
- Add ListObject at a specific place within an Excel file & convert them to a range of cells.
- Delete specific or all ListObjects in a worksheet or summarize its data with pivot table.
- Apply custom criteria to list filters of various types.
- Get, update, show or hide chart legend & titles.
- Manipulate page setup, header & footer.
- Create, update, fetch or delete document properties.
- Fetch the required shape from worksheet.
- Load & Process Excel Spreadsheets via Cloud SDK.
- Cloud SDK to Read & Process Excel Worksheets.
- Leverage the Power of Pivot Tables & Ranges.

## Enhancements in Version 20.2

- Automatically refresh authorization Token in SDK.

## Read & Write Spreadsheet Formats

**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**OpenOffice:** ODS
**SpreadsheetML:** XML
**Text:** CSV, TSV, TXT (TabDelimited)
**Web:** HTML, MHTML

## Save Spreadsheet As

DIF, PDF, XPS, TIFF, SVG, MD (Markdown)

## Read Spreadsheet Formats

SXC, FODS

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

[Product Page](https://products.aspose.cloud/words/swift) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [Live Demo](https://products.aspose.app/words/family) | [API Reference](https://apireference.aspose.cloud/words/) | [Code Samples](https://github.com/aspose-words-cloud/aspose-words-cloud-swift) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
