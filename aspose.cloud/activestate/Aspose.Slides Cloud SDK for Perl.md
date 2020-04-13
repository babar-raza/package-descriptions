# .NET REST API for OMR Processing

This Cloud SDK enables you to [perform Optical Mark Recognition (OMR)](https://products.aspose.cloud/slides/perl) operations on human-marked data from within your cloud-based C#, ASP.NET & other .NET apps.

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

## Getting Started

The complete source code is available at the [GitHub repository](https://github.com/aspose-slides-cloud/aspose-slides-cloud-perl). You can either directly use it in your project via source code or get [CPAN module](https://metacpan.org/release/AsposeSlidesCloud-SlidesApi) (recommended).

## Prerequisites

To use Aspose Slides Cloud SDK for Perl you need to register an account with [Aspose Cloud](https://www.aspose.cloud/) and lookup/create App Key and SID at [Cloud Dashboard](https://dashboard.aspose.cloud/#/apps). There is free quota available. For more details, see [Aspose Cloud Pricing](https://purchase.aspose.cloud/pricing).

## Installation

```console
cpan ASPOSE/AsposeSlidesCloud-SlidesApi-19.1204.tar.gz
```

## Convert a PPTX File to PDF via Aspose.Slides Cloud Perl Library

```perl
use File::Slurp;

use AsposeSlidesCloud::Configuration;
use AsposeSlidesCloud::SlidesApi;

my $config = AsposeSlidesCloud::Configuration->new();
$config->{app_sid} = "MyAppSid";
$config->{app_key} = "MyAppKey";
my $api = AsposeSlidesCloud::SlidesApi->new(config => $config);
my $file = read_file("MyPresentation.pptx", { binmode => ':raw' });
my %params = ('format' => 'pdf', 'document' => $file);
my $result = $api->post_slides_convert(%params);
my $pdf = "MyPresentation.pdf";
open my $fh, '>>', $pdf;
binmode $fh;
print $fh $result;
close $fh;
```

[Product Page](https://products.aspose.cloud/slides/perl) | [Documentation](https://docs.aspose.cloud/display/omrcloud/Home) | [Live Demo](https://products.aspose.app/slides/family) | [API Reference](https://apireference.aspose.cloud/omr/) | [Code Samples](https://github.com/aspose-omr-cloud) | [Blog](https://blog.aspose.cloud/category/omr/) | [Free Support](https://forum.aspose.cloud/c/omr) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
