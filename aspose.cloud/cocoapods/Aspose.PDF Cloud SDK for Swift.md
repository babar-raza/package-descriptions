# Swift REST API to Process PDF in Cloud

This Cloud SDK allows you to [easily build cloud-based PDF creator](https://products.aspose.cloud/pdf/swift), editor & converter apps in Swift language for various cloud platforms.

## PDF Processing Features

- Add PDF document's header & footer in text or image format.
- Add tables & stamps (text or image) to PDF documents.
- Append multiple PDF documents to an existing file.
- Work with PDF attachments, annotations, & form fields.
- Apply encryption or decryption to PDF documents & set password.
- Delete all stamps & tables from a page or entire PDF document.
- Delete a specific stamp or table from the PDF document by its ID.
- Replace a single or multiple instances of a text on a PDF page or from entire document.
- Extensive support for converting PDF documents to various other file formats.
- Extract various elements of PDF file & make PDF document optimized.

## New Features & Enhancements in Version 20.7

- Added Support for `PDF_A_3A` Format.
- Added Support of `MaxResolution` option in `OptimizeOption`.
- Added Support of `ImageCompressionOptions` in `OptimizeOptions`.
- Implemented Info action.

For the detailed notes, please visit [Aspose.PDF Cloud 20.7 Release Notes](https://docs.aspose.cloud/display/pdfcloud/Aspose.PDF+Cloud+20.7+Release+Notes).

## Read & Write PDF Formats

PDF, EPUB, HTML, TeX, SVG, XML, XPS, FDF, XFDF

## Save PDF As

XLS, XLSX, PPTX, DOC, DOCX, MobiXML, JPEG, EMF, PNG, BMP, GIF, TIFF, Text

## Read PDF Formats

MHT, PCL, PS, XSLFO, MD

## Installation via CocoaPods

[CocoaPods](https://cocoapods.org/) is a dependency manager for Cocoa projects. You can install it with the following command:

```console
$ gem install cocoapods
```

- *CocoaPods 1.1+ is required to build AsposePdfCloud 20.2+.*

To integrate AsposePdfCloud into your Xcode project using CocoaPods, specify it in your `Podfile`:

```swift
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '10.0'
use_frameworks!

target '<Your Target Name>' do
    pod 'AsposePdfCloud', '~> 20.2'
end
```

Then, run the following command:

`$ pod install`

## Getting Started

Please follow the installation instructions and execute the following Java code:

```java
func testGetPageAnnotations() {
    let name = "PdfWithAnnotations.pdf"

    let pageNumber = 2
    PdfAPI.getPageAnnotations(name: name, pageNumber: pageNumber, folder: self.tempFolder) {
        (response, error) in
        guard error == nil else {
            // errror handle
            return
        }
        if let response = response {
            // do
        }
    }
}
```

## Unit Tests

Aspose PDF SDK includes a suite of unit tests within the "test" subdirectory. These Unit Tests also serves as examples of how to use the Aspose PDF SDK.

## Licensing

All Aspose.PDF Cloud SDKs are licensed under [MIT License](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-swift/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/pdf/swift) | [Documentation](https://docs.aspose.cloud/display/pdfcloud/Home) | [Demo](https://products.aspose.app/pdf/family) | [API Reference](https://apireference.aspose.cloud/pdf/) | [Examples](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-swift) | [Blog](https://blog.aspose.cloud/category/pdf/) | [Free Support](https://forum.aspose.cloud/c/pdf) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
