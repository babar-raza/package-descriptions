# .NET REST API to Process PDF in Cloud

This Cloud SDK allows you to [easily build cloud-based PDF creator](https://products.aspose.cloud/pdf/net), editor & converter apps in C#, ASP.NET or other .NET languages for various cloud platforms.

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

## New Features in Version 20.3

- Prepared Aspose.PDF Cloud using the latest version of Aspose.PDF for .NET.

For the detailed notes, please visit [Aspose.PDF Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/pdfcloud/Aspose.PDF+Cloud+20.3+Release+Notes).

## Read & Write PDF Formats

PDF, EPUB, HTML, TeX, SVG, XML, XPS, FDF, XFDF

## Save PDF As

XLS, XLSX, PPTX, DOC, DOCX, MobiXML, JPEG, EMF, PNG, BMP, GIF, TIFF, Text

## Read PDF Formats

MHT, PCL, PS, XSLFO, MD

## Getting Started with Aspose.PDF Cloud SDK for Ruby

You do not need to install anything to get started with Aspose.PDF Cloud SDK for Ruby. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Please check the [GitHub Repository](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-dotnet) for other common usage scenarios.

## Installation

### Build a gem

To build the Ruby code into a gem:

`gem build aspose_pdf_cloud.gemspec`

Then either install the gem locally:

`gem install ./aspose_pdf_cloud-20.2.0.gem`

(for development, run `gem install --dev ./aspose_pdf_cloud-20.2.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the `Gemfile`:

`gem 'aspose_pdf_cloud', '~> 20.2.0'`

### Install from Git

Please access the Aspose.OMR Cloud SDK for Ruby [GitHub Repository](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-ruby) and add the following in the `Gemfile`:

`gem 'aspose_pdf_cloud', :git => 'https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-ruby.git'`

## Usage

APIs of this SDK can be called as follows:

```ruby
require 'aspose_pdf_cloud'

class AsposePDFUsage
  
  include AsposePDFCloud

  def initialize
    #Get App key and App SID from https://cloud.aspose.com
    @pdf_api = PdfApi.new("APP_KEY", "APP_SID")
  end
  
  def get_page_annotations
      file_name = 'PdfWithAnnotations.pdf'
  
      page_number = 2
      opts = {
          :folder => 'tempFolder'
      }
  
      response = @pdf_api.get_page_annotations(file_name, page_number, opts)
    end  
end
```

## Fetch PDF Document Annotations using Ruby Code

```ruby
require 'aspose_pdf_cloud'
include AsposePdfCloud

app_key=""
app_sid=""
@pdf_api = PdfApi.new(app_key,app_sid)
file_name = 'PdfWithAnnotations.pdf'
# Upload the File
@pdf_api.put_create(file_name, ::File.open("example_data/" +file_name, 'r') { |io| io.read(io.size)})
puts "Uploaded the File"
opts = {
    :folder => @temp_folder
}
response = @pdf_api.get_document_annotations(file_name, opts)
puts response
```

## Unit Tests

Aspose PDF SDK includes a suite of unit tests within the [test](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-ruby/tree/master/test) subdirectory. These Unit Tests also serves as examples of how to use the Aspose PDF SDK.

## Licensing

All Aspose.PDF Cloud SDKs are licensed under [MIT License](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/pdf/ruby) | [Documentation](https://docs.aspose.cloud/display/pdfcloud/Home) | [API Reference](https://apireference.aspose.cloud/pdf/) | [Code Samples](https://github.com/aspose-pdf-cloud/aspose-pdf-cloud-ruby) | [Blog](https://blog.aspose.cloud/category/pdf/) | [Free Support](https://forum.aspose.cloud/c/pdf) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
