# Image Processing in Cloud via .NET REST API

This cloud SDK assists to [process & manipulate images](https://products.aspose.cloud/imaging/net) from within your C#, ASP.NET & other .NET based cloud applications, without installing any 3rd party tool.

## Image Processing Features

- Fetch or update properties of cloud hosted images.
- Scale, flip, crop and export an image with a single API call.
- Resize, crop, flip, convert and export an image to other supported formats.
- Update image parameters of JPEG2000 & WEBP images.
- Access and multi-frame TIFF image and extract the desired frames from it.
- Rotate, flip, crop, resize or fetch properties of the selected TIFF frame.
- Merge multiple TIFF images.

## New Features in Version 20.2

- Support for image grayscale feature.

For the detailed notes, please visit [Aspose.Imaging Cloud 20.2 - Release Notes](https://docs.aspose.cloud/display/imagingcloud/Aspose.Imaging+Cloud+20.2+-+Release+Notes).

## Read & Write Image Formats

BMP, GIF, JPEG, JPEG2000, PSD, TIFF, WEBP, PNG, WMF, EMF, SVG

## Save Image As

PDF

## Read Image Formats

DJVU, DICOM, CDR, CMX, ODG, DNG

## Getting Started with Aspose.Imaging Cloud SDK for Ruby

The complete source code is available at the [GitHub Repository](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/aspose_imaging_cloud) (recommended).

- Sign Up. Before you begin, you need to sign up for an account on our [Dashboard](https://dashboard.aspose.cloud/) and retrieve your [credentials](https://dashboard.aspose.cloud/#/apps).
- Minimum requirements. This SDK requires [Ruby](https://www.ruby-lang.org/en/downloads/).
- Install Aspose.Imaging Cloud Python SDK.
    Please, install the following [Ruby gem](https://rubygems.org/gems/aspose-imaging-cloud/) using command line.
    `gem install aspose_imaging_cloud`
    Import the dependencies to your code as follows.
    `require 'aspose_imaging_cloud'`
- Using the SDK. The best way to become familiar with how to use the SDK is to read the [Developer Guide](https://docs.aspose.cloud/display/imagingcloud/Developer+Guide). The [Getting Started Guide](https://docs.aspose.cloud/display/imagingcloud/Getting+Started) will help you to become familiar with the common concepts.

## Quick Examples

Please, look at [Examples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-ruby/blob/master/EXAMPLES.md) document for basic usage or use the [Examples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-ruby/blob/master/Examples) folder for more sophisticated scenarios.

## Convert Image from Request Stream to another Format using Ruby Code

```ruby
# optional parameters are base URL, API version and debug mode
imaging_api = ImagingApi.new('yourAppKey', 'yourAppSid')

begin
  # convert image from request stream to JPEG and save it to storage
  # please, use outPath parameter for saving the result to storage
  imaging_api.create_saved_image_as(AsposeImagingCloud::CreateSavedImageAsRequest.new(File.open(local_input_image), 'jpg', remote_result_image, test_storage))

  # download saved image from storage
  saved_file = imaging_api.download_file(AsposeImagingCloud::DownloadFileRequest.new(remote_result_image, test_storage))
  # process resulting image from storage

  # convert image from request stream to JPEG and read it from
  # resulting stream
  image_stream = imaging_api.create_saved_image_as(AsposeImagingCloud::CreateSavedImageAsRequest.new(File.open(local_input_image), 'jpg', nil, test_storage))
  # process resulting image from response stream
ensure
  imaging_api.delete_file(AsposeImagingCloud::DeleteFileRequest.new(remote_result_image, test_storage))
end
```

## Aspose Cloud-hosted service VS on-premise deployment (experimental feature)

Starting from v19.7, you can choose either to use Aspose Cloud-hosted image processing service (the standard way) or the Docker image from Docker Hub deployed on-premise to serve the requests. The details about key differences and deployment process will be described on the dedicated Docker Hub page as soon as it's released.

To succeed with your on-premise service usage by the SDK, you need to:

- Use the API class constructor with base URL required parameter, API version and debug mode optional parameters, skipping the credentials parameters.
    `ImagingApi.new(nil, nil, 'yourServiceUrl')`
- Set storage or storageName parameters for each request where they're present (mandatory!).

## Dependencies

- Ruby 2.5 or later

## Licensing

All Aspose.Imaging Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/imaging/ruby) | [Documentation](https://docs.aspose.cloud/display/imagingcloud/Home) | [Live Demo](https://products.aspose.app/imaging/family) | [API Reference](https://apireference.aspose.cloud/imaging/) | [Code Samples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-ruby) | [Blog](https://blog.aspose.cloud/category/imaging/) | [Free Support](https://forum.aspose.cloud/c/imaging) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
