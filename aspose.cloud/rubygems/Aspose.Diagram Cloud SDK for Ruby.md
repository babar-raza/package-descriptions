# Ruby Cloud REST API for Visio Processing

This cloud SDK enables your Ruby cloud apps to [create & process Visio diagrams](https://products.aspose.cloud/diagram/ruby) from within your apps without installing Microsoft Visio.

## Visio Processing Features

- Retrieve document information of a Visio diagram.
- Programmatically create a new Microsoft Visio diagram file.
- Convert Visio flow-charts to other supported formats.
- Upload your business oriented Visio diagrams to cloud storage.
- Export Visio files to raster images, fixed-layout and HTML formats.

## New Features in Version 19.10

- General enhancements to the Aspose.Diagram Cloud REST API.
- Added `SaveOption` parameter for `saveAs` API.
- Enhancement in the `Convert` API.
- Added support for multiple files exports that convert files to `HTML`.
- Integrated Aspose.Storage Cloud feature into Aspose.Diagram Cloud.

For the detailed notes, please visit [Aspose.Diagram Cloud 19.10 Release Notes](https://docs.aspose.cloud/display/diagramcloud/Aspose.Diagram+Cloud+19.10+Release+Notes).

## Read & Write Visio Formats

**Microsoft Visio:** VSDX, VSX, VTX, VDX, VSSX, VSTX, VSDM, VSSM, VSTM

## Save Visio As

**Fixed Layout:** PDF, XPS
**Images:** JPEG, PNG, BMP, TIFF, SVG, EMF
**Web:** HTML
**Other:** XAML, SWF

## Read Visio Formats

**Microsoft Visio:** VDW, VSD, VSS, VST

## Getting Started with Aspose.Diagram Cloud SDK for Ruby

You do not need to install anything to get started with Aspose.Diagram Cloud SDK for Ruby. All you need to do is create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Please check the [GitHub Repository](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-dotnet) for other common usage scenarios.

## Usage

Please, add the following [gem](https://rubygems.org/gems/aspose_diagram_cloud) to your project.

```ruby
gem install aspose_diagram_cloud
```

### Aspose Cloud-hosted service VS on-premise deployment (experimental feature)

Starting from v19.10, you can choose either to use Aspose Cloud-hosted image processing service (the standard way) or the Docker image from Docker Hub deployed on-premise to serve the requests. The details about key differences and deployment process will be described on the dedicated Docker Hub page as soon as it's released.

To succeed with your on-premise service usage by the SDK, you need to:

- Use the new API class constructor with grantType parameter, clientId and clientSecret parameters.

    ```ruby
    $diagramApi = AsposeDiagramCloud::DiagramApi.new($grant_type,$client_id,$client_secret)
    ```

- Set storage or storageName parameters for each request where they're present (mandatory!).

## Licensing

All Aspose.Diagram Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-ruby/blob/master/LICENSE).

[Product Page](https://products.aspose.cloud/diagram/net) | [Documentation](https://docs.aspose.cloud/display/diagramcloud/Home) | [API Reference](https://apireference.aspose.cloud/diagram/) | [Code Samples](https://github.com/aspose-diagram-cloud/aspose-diagram-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/diagram/) | [Free Support](https://forum.aspose.cloud/c/diagram) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
