# .NET REST API for OMR Processing

This Cloud SDK enables you to [perform Optical Mark Recognition (OMR)](https://products.aspose.cloud/omr/net) operations on human-marked data from within your cloud-based C#, ASP.NET & other .NET apps.

## OMR Processing Features

- Perform recognition of scanned photos and images for OMR operations.
- Ability to perform OMR on rotated & perspective (within 25 deg) photos.
- Extract & recognize human-marked data from scanned tests, exams, surveys etc.
- Supports the export of OMR results to CSV file format.
- Use textual markup to generate OMR templates, generate surveys and test sheets.
- Availability of GUI application for managing OMR templates.
- Specify number of OMR based questions & answers in the template.
- Availability of GUI OMR editor as a cloud client.
- Provide JSON rules to perform OMR answer grading.
- Clip an area of interest from an image, save it as JPEG & perform OMR on it.
- Perform highly accurate optical mark recognition (OMR).

## Save OMR As

CSV

## Read OMR Formats

JPEG, PNG, BMP, TIFF, PDF

## Platform Independence

Aspose.OMR Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.OMR Cloud SDK for Ruby

The complete source code is available at the [GitHub Repository](https://github.com/aspose-omr-cloud/aspose-omr-cloud-ruby). You can either directly use it in your project via source code or get [RubyGem](https://rubygems.org/gems/aspose_omr_cloud) (recommended).

## Requirements

- Ruby 2.3 and later

## Installation

### Clone repository

Clone `aspose-omr-cloud` with submodules:

`git clone https://github.com/aspose-omr-cloud/aspose-omr-cloud-ruby.git --recurse-submodules`

### Build a gem

To build the Ruby code into a gem:

`gem build aspose_omr_cloud.gemspec`

Then either install the gem locally:

`gem install ./aspose_omr_cloud-18.8.0.gem`

(for development, `run gem install --dev ./aspose_omr_cloud-18.8.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

`gem 'aspose_omr_cloud', '~> 18.8.0'`

### Install from Git

Please access the Aspose.OMR Cloud SDK for Ruby [GitHub Repository](https://github.com/aspose-omr-cloud/aspose-omr-cloud-ruby) and add the following in the `Gemfile`:

`gem 'aspose_omr_cloud', :git => 'https://github.com/aspose-omr-cloud/aspose-omr-cloud-ruby.git'`

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

`ruby -Ilib script.rb`

## Optional requirements

To take full advantage of Aspose.OMR for Cloud, `aspose/storage-sdk-ruby` is required. Just run `gem install aspose_storage_cloud`. You may refer to official [Aspose Storage SDK](https://github.com/aspose-storage-cloud/aspose-storage-cloud-ruby) to get more information.

## Usage

### Receive Cloud Keys

Aspose.Cloud credentials are required to use Aspose.OMR for Cloud API. You can acquire App SID and App Key by registering at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/). It will take only a couple of minutes.

### Update submodule

Make sure you've cloned [aspose-omr-cloud-demo-data](https://dashboard.aspose.cloud/) submodule, that contains all data required to run demo. In case you are missing submodules use the following git commands to initialize and update them:

```console
git submodule init
git submodule update --remote --merge
```

## Authentication

- Library uses `OAUTH2` internally

## OMR Demo

You can check out [OMR Demo](https://github.com/aspose-omr-cloud/aspose-omr-cloud-ruby/blob/master/demo) project to get started with Aspose.OMR for Cloud.

## Limitations

- Recognition process works well with the bubbles which are at least 75% filled.
- Works on perspective (side viewed/out of focus) & rotated images under certain conditions, e.g., rotation angle within 25 degrees.
- OMR operation will show results only in text format.
- Performing OCR operation is not supported for now.

[Product Page](https://products.aspose.cloud/omr/ruby) | [Documentation](https://docs.aspose.cloud/display/omrcloud/Home) | [API Reference](https://apireference.aspose.cloud/omr/) | [Code Samples](https://github.com/aspose-omr-cloud/aspose-omr-cloud-ruby) | [Blog](https://blog.aspose.cloud/category/omr/) | [Free Support](https://forum.aspose.cloud/c/omr) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
