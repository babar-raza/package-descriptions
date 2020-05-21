# Perl REST API to Process Presentation in Cloud

This REST API enables your Perl cloud-based apps to [process & manipulate PPT, PPTX, ODP, OTP presentations](https://products.aspose.cloud/slides/perl) in the cloud.

## Presentation Processing Features

- Fetch presentation images in any of the supported file formats.
- Copy layout side or clone master slide from the source presentation.
- Process slides shapes, slides notes, placeholders, colors & font theme info.
- Programmatically create presentation from HTML & export it to various formats.
- Merge multiple presentations or split single presentation into multiple ones.
- Extract and replace text from specific slide or entire presentation.

## Enhancements  in Version 20.4

- Supports ViewProperties.
- Supports new Powerpoint 2016 Chart types.

## Public API Changes

- Added `viewproperties` resource. It allows to GET and set (PUT) view properties of a document (`LastView`, `HorizontalBarState`, `VerticalBarState` etc.)
- Added `Treemap`, `Sunburst`, `Histogram`, `ParetoLine`, `BoxAndWhisker`, `Waterfall`, and `Funnel` chart types.

For the detailed notes, please visit [Aspose.Slides Cloud 20.4 Release Notes](https://docs.aspose.cloud/display/slidescloud/Aspose.Slides+Cloud+20.4+Release+Notes).

## Read & Write Presentation Formats

**Microsoft PowerPoint:** PPT, PPTX, PPS, PPSX, PPTM, PPSM, POTX, POTM
**OpenOffice:** ODP, OTP

## Save Presentation As

**Fixed Layout:** PDF, PDF/A, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Web:** HTML
**Other:** SWF (export whole presentations)

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

[Product Page](https://products.aspose.cloud/slides/perl) | [Documentation](https://docs.aspose.cloud/display/slidescloud/Home) | [Demo](https://products.aspose.app/slides/family) | [API Reference](https://apireference.aspose.cloud/slides/) | [Examples](https://github.com/aspose-slides-cloud/aspose-slides-cloud-perl) | [Blog](https://blog.aspose.cloud/category/slides/) | [Free Support](https://forum.aspose.cloud/c/slides) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
