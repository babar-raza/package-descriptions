# HTML Rendering & Conversion Ruby Cloud REST API

This cloud SDK assists to develop cloud-based [HTML page rendering, processing, translation & conversion](https://products.aspose.cloud/html/ruby) apps in Ruby languages via REST API.

## HTML Processing Features

- Fetch HTML page along with its resources as a ZIP archive by providing page URL.
- Based on page URL, retrieve all images of an HTML page as a ZIP package.
- Load data from local file to populate HTML document template.
- Use request body to populate HTML document template.
- Convert HTML page to numerous other file formats.

## New Features in Version 20.5

- Added `Configuration.AddDefaultHeader`. It provides ability to specify custom headers which will be added to each `HTTP` request beneath API calls.

For the detailed notes, please visit [Release Notes - 2020](https://docs.aspose.cloud/display/htmlcloud/Release+Notes+-+2020).

## Read & Write HTML Formats

HTML, XHTML, zipped HTML, zipped XHTML, MHTML, HTML containing SVG markup, Markdown, JSON

## Save HTML As

**Fixed Layout:** PDF, XPS
**Images:** TIFF, JPEG, PNG, BMP, GIF
**Other:** TXT, ZIP (images)

## Read HTML Formats

**eBook:** EPUB
**Other:** XML, SVG

## Getting Started with Aspose.HTML Cloud SDK for Ruby

You do not need to install anything to get started with Aspose.HTML Cloud SDK for Ruby. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.HTML-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.HTML assembly in your project. If you already have Aspose.HTML Cloud SDK for Ruby and want to upgrade it, please execute `Update-Package Aspose.HTML-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-html-cloud/aspose-html-cloud-dotnet) for other common usage scenarios.

## Requirements

- Ruby >= 1.9
- libcurl.dll (libcurl.so)

## Installation

```console
bundle install --jobs 4
```

## Build a gem

To build the Ruby code into a gem:

```console
gem build aspose_html_cloud.gemspec
```

Then either install the gem locally:

```console
gem install ./aspose_html_cloud-19.6.0.gem
```

(for development, run `gem install --dev ./aspose_html_cloud-19.6.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the `Gemfile`:

```console
gem 'aspose_html_cloud', '~> 19.6.0'
```

## Load from git

```console
git clone https://github.com/aspose-html-cloud/aspose-html-cloud-ruby.git
cd aspose-html-cloud-ruby
```

## Install from Git

If the Ruby gem is hosted at a [GitHub repository](https://github.com/aspose-html-cloud/aspose-html-cloud-ruby.git), then add the following in the `Gemfile`:

```console
gem 'aspose_html_cloud', :git => 'https://github.com/aspose-html-cloud/aspose-html-cloud-ruby.git'
```

## Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```console
ruby -Ilib aspose_html_cloud.rb
```

## OAuth

Type: OAuth
Flow: application
Authorization URL: "https://api.aspose.cloud/connect/token"
Scopes: N/A

## Convert from HTML to PNG Format using Ruby Code

```ruby
# Load the gem
require 'aspose_html_cloud'

CONFIG = {
    "basePath":"https://api.aspose.cloud/v3.0",
    "authPath":"https://api.aspose.cloud/connect/token",
    "apiKey":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
    "appSID":"XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    "debug":true
}

api_instance = AsposeHtml::HtmlApi.new CONFIG

name = "test.html" # String | Document name.

out_format = "png" # String | Resulting image format.

opts = { 
  width: 800, # Integer | Resulting image width. 
  height: 1000, # Integer | Resulting image height. 
  left_margin: 10, # Integer | Left resulting image margin.
  right_margin: 10, # Integer | Right resulting image margin.
  top_margin: 20, # Integer | Top resulting image margin.
  bottom_margin: 20, # Integer | Bottom resulting image margin.
  resolution: 300, # Integer | Resolution of resulting image.
  folder: "/", # String | The source document folder.
  storage: nil # String | The source document storage.
}

begin
  #Convert the HTML document from the storage by its name to the specified image format.
  result = api_instance.get_convert_document_to_image(name, out_format, opts)
  p result
rescue AsposeHtml::ApiError => e
  puts "Exception when calling HtmlApi->get_convert_document_to_image: #{e}"
end
```

[Tests](https://github.com/aspose-html-cloud/aspose-html-cloud-ruby/blob/master/spec/api/html_api_spec.rb) contain various examples of using the Aspose.HTML SDK.

## Convert the HTML, EPUB, SVG document to PDF and uploads resulting file to storage

```ruby
def put_convert_document_to_pdf(name, out_path, opts = {})
      data, _status_code, _headers = put_convert_document_to_pdf_with_http_info(name, out_path, opts)
      return {file: data, status: _status_code, headers: _headers}
    end
```

[Product Page](https://products.aspose.cloud/html/ruby) | [Documentation](https://docs.aspose.cloud/display/htmlcloud/Home) | [Demo](https://products.aspose.app/html/family) | [API Reference](https://apireference.aspose.cloud/html/) | [Examples](https://github.com/aspose-html-cloud/aspose-html-cloud-ruby) | [Blog](https://blog.aspose.cloud/category/html/) | [Free Support](https://forum.aspose.cloud/c/html) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
