# Document Metadata .NET Cloud REST API

This REST API enables your C#, ASP.NET, & other .NET apps to [read & write metadata](https://products.groupdocs.cloud/metadata/net) of documents, images, diagrams, video, audio, & various other file formats.

## Cloud Document Metadata Features

- Add metadata.
- Extract Metadata.
- Remove Metadata.
- Set Metadata.
- Get document information.
- Get metadata tag information.
- Get supported file formats.

## Read & Write File Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX
**Microsoft Excel:** XLS, XLSX, XLSM, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POTX, PPTM
**Microsoft Visio:** VSD, VSDX, VDX, VSS, VSX
**Microsoft Project:** MPP
**Microsoft OneNote:** ONE
**OpenOffice:** ODS, ODT, OTC
**Email:** EML, MSG, VCF, VCR
**AutoCAD:** DWG, DXF
**Photoshop:** PSD
**Images:** BMP, GIF, JPG, JPEG, JPE, JP2, PNG, TIFF, WEBP, DICOM
**Audio:** MP3, WAV
**Video:** AVI, MOV, QT, FLV, ASF
**Archives:** ZIP
**Metafiles:** EMF, WMF
**Fonts:** OTF, TTF, TTC
**Fixed Layout:** PDF
**eBook:** EPUB, DJVU, DJV
**Other:** TORRENT

## Getting Started

You do not need to install anything to get started with GroupDocs.Metadata Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Metadata-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Metadata assembly in your project. If you already have GroupDocs.Metadata Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Metadata-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-dotnet) for other common usage scenarios.

## Get Supported File Formats to Fetch Metadata using C# Code

```csharp
namespace Example
{
    public class Example
    {
        public void Main()
        {
            //TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud (free registration is required).
            var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
            var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

            var api = new MetadataApi(appSid, appKey);

            try
            {
                // Get supported file formats
                var response = api.GetSupportedFileFormats();

                foreach (var format in response.Formats)
                {
                    Debug.Print(format.ToString());
                }
            }
            catch (Exception e)
            {
                Debug.Print("Something went wrong: " + e.Message);
            }
        }
    }
}
```

## Using C# to Extract DOCX Metadata By Possible Tag Name

```csharp
string MyAppKey = ""; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
string MyAppSid = ""; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud

var configuration = new Configuration(MyAppSid, MyAppKey);
var apiInstance = new MetadataApi(configuration);
var fileInfo = new FileInfo
{
    FilePath = "documents/input.docx"
};

var options = new ExtractOptions
{
    FileInfo = fileInfo,
    SearchCriteria = new SearchCriteria
    {
        TagOptions = new TagOptions
        {
            PossibleName = "creator"
        }
    }
};

var request = new ExtractRequest(options);

var response = apiInstance.Extract(request);
```

[Product Page](https://products.groupdocs.cloud/metadata/net) | [Documentation](https://wiki.groupdocs.cloud/metadatacloud/) | [Live Demo](https://products.groupdocs.app/metadata/family) | [API Reference](https://apireference.groupdocs.cloud/metadata/) | [Code Samples](https://github.com/groupdocs-metadata-cloud/groupdocs-metadata-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/metadata/) | [Free Support](https://forum.groupdocs.cloud/c/metadata) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
