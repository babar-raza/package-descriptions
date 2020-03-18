# AutoCAD File Processing Ruby Cloud REST API

This Cloud SDK helps you perform [AutoCAD drawing conversion, processing & manipulation](https://products.aspose.cloud/cad/ruby) from within your Ruby cloud apps without AutoCAD.

## CAD Processing Features

- Export CAD drawings to other file formats.
- Get image properties of a CAD drawing.
- Change scale of an AutoCAD sketch.
- Flip and rotate a CAD image.
- Upload or download CAD drawings to the cloud storage.
- Copy, move, delete CAD files from the cloud storage.

## Read & Write CAD Formats

DXF (R12/2007/2010)

## Save CAD As

**Fixed Layout:** PDF (as a vector and as a raster)
**Images:** BMP, PNG, JPG, JPEG, JPEG2000, TIF, TIFF, PSD, GIF, WMF

## Read CAD Formats

DWG (13, 14, 2000, 2004), DWG (2010, 2013, 2014), DWG (2015, 2017, 2018), DWT (13, 14, 2000, 2004), DWT (2010, 2013, 2014), DWT (2015, 2017, 2018), DWF, DGN v7, IGES (IGS), PLT, Industry Foundation Classes (IFC), STereoLithography (STL)

## Platform Independence

Aspose.CAD Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.CAD Cloud SDK for Ruby

The complete source code is available at the [GitHub Repository](https://github.com/aspose-cad-cloud/aspose-cad-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/aspose_CAD_cloud) (recommended). For more details, please visit our documentation website.

## Prerequisites

To use Aspose CAD for Cloud Ruby SDK you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Dependencies

- Ruby 2.3 or later
- referenced packages (see [here](https://github.com/aspose-cad-cloud/aspose-cad-cloud-ruby/blob/master/Gemfile) for more details.)

## Installation

To install this package do the following: update your `Gemfile`:

```console
gem 'aspose_CAD_cloud', '~> 18.7'
```

or install directly:

```console
gem install aspose_CAD_cloud
```

## Sample usage

```ruby
@config = Configuration.new
@config.api_key['api_key'] = '' # Put your's api_key and app_sid
@config.api_key['app_sid'] = ''
@api_client = ApiClient.new @config
@CAD_api = CADApi.new @api_client
AsposeApp.app_key_and_sid(@config.api_key['api_key'], @config.api_key['app_sid'])
@storage_api = StorageApi.new
request = DeleteDocumentWatermarkRequest.new remote_name, remote_test_folder + test_folder
result = @CAD_api.delete_document_watermark request
```

## Rotate & Flip Drawing using Ruby Cloud REST API

```ruby
module AsposeCadCloud
  require_relative 'base_test_context'
  class RotateFlipDrawingTests < BaseTestContext
    def test_folder
      ''
    end

    #
    # Test for drawing rotation 270 degrees and flip across X axis with specified format and fetch result through response
    #
    def test_post_rotate_flip_drawing_tests
      filename = '01.026.385.01.0.I SOPORTE ENFRIADOR.dwg'
      remote_name = filename
      output_format = 'pdf'
      dest_name = remote_test_out + remote_name + '.' + output_format

      st_request = PutCreateRequest.new remote_test_folder + remote_name, File.open(local_test_folder + filename, "r").read
      @storage_api.put_create st_request

      request = PostDrawingRotateFlipRequest.new File.open(local_test_folder + filename, "r"), output_format, "Rotate270FlipX", remote_test_folder
      result = @Cad_api.post_drawing_rotate_flip_with_http_info request
      assert_equal 200, result[1]
    end
  end
end
```

[Tests](https://github.com/aspose-cad-cloud/aspose-cad-cloud-ruby/blob/master/tests) contain various examples of using the SDK. Please put your credentials into [Configuration](https://github.com/aspose-cad-cloud/aspose-cad-cloud-ruby/blob/master/lib/configuration.rb).

[Product Page](https://products.aspose.cloud/cad/ruby) | [Documentation](https://docs.aspose.cloud/display/cadcloud/Home) | [API Reference](https://apireference.aspose.cloud/cad/) | [Code Samples](https://github.com/aspose-cad-cloud/aspose-cad-cloud-ruby) | [Blog](https://blog.aspose.cloud/category/cad/) | [Free Support](https://forum.aspose.cloud/c/cad) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
