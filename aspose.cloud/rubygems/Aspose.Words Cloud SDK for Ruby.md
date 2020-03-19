# .NET REST API for Cloud Document Processing

This cloud SDK provides seamless integration of [cloud document processing & manipulation features](https://products.aspose.cloud/words/net) into your cloud-based C#, ASP.NET & other .NET apps.

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

## Enhancements in Version 20.1.0

- Moved property `ColorMode` from `SaveOptionsData` to `FixedPageSaveOptionsData`.
- Replaced `MemoryStream` and `byte[]` with `SixLabors.ImageSharp.IImage` in image processing.
- Included support of `ICC` profiles and implement `ICCBased` color space.

For the detailed notes, please visit [Aspose.Words Cloud 20.1 Release Notes](https://docs.aspose.cloud/display/wordscloud/Aspose.Words+Cloud+20.1+Release+Notes).

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

## Getting Started with Aspose.Words Cloud SDK for Ruby

You do not need to install anything to get started with Aspose.Words Cloud SDK for Ruby. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-words-cloud/aspose-words-cloud-ruby).

## How to use the SDK?

The complete source code is available in this repository folder. You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/aspose_words_cloud) (recommended).

## Prerequisites

To use Aspose Words for Cloud Ruby SDK you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://github.com/aspose-words-cloud/aspose-words-cloud-ruby/blob/master/tests).

## Installation

To install this package do the following: 

update your `Gemfile`:

`gem 'aspose_words_cloud', '~> 20.3'`

or install directly

`gem install aspose_words_cloud`

## Sample usage

```ruby
AsposeWordsCloud.configure do |config|
        config.api_key['api_key'] = AppKey
        config.api_key['app_sid'] = AppSid
        config.host = host
request = DeleteWatermarkRequest.new remote_name, remote_test_folder + test_folder
result = @words_api.delete_watermark request

[Tests](https://github.com/aspose-words-cloud/aspose-words-cloud-ruby/blob/master/tests) contain various examples of using the SDK.
```

## Dependencies

- Ruby 2.3 or later
- referenced packages (see [here](https://github.com/aspose-words-cloud/aspose-words-cloud-ruby/blob/master/Gemfile) for more details)

## Licensing

All Aspose.Words Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-words-cloud/aspose-words-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/words/net) | [Documentation](https://docs.aspose.cloud/display/wordscloud/Home) | [API Reference](https://apireference.aspose.cloud/words/) | [Code Samples](https://github.com/aspose-words-cloud/aspose-words-cloud-ruby) | [Blog](https://blog.aspose.cloud/category/words/) | [Free Support](https://forum.aspose.cloud/c/words) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
