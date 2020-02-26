This cloud REST API enhances your C#, ASP.NET & other .NET cloud apps to compare two documents, fetch, accept or reject the changes. Supports 90+ file formats.

## Cloud Document Comparison Features

- Compare two documents and fetch changes.
- Fetch document changes based on change category, such as, numeric only.
- Accept or reject the changes that come up after document comparison.
- Get the image stream of resultant document via JsonRequest object.
- Save the resultant document to streams as set of images.
- Get the resultant document path.
- Add summary page to resultant document after comparison.
- Show deleted components in the resultant document.
- Detect style changes.
- Get or set password to the the resultant document.

## Supported Document Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX, XLTM, XLTX, ODS, OTS, CSV, TSV
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POTM, POTX, ODP, OTP
**Microsoft Visio:** VDW, VDX, VSD, VSDML, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Microsoft Project:** MPP, MPT
**Microsoft OneNote:** ONE
**Email:** EML, EMLX, MSG, OST, PST
**Adobe Photoshop:** PSD
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**eBook:** EPUB, MOBI
**Image:** BMP, CGM, DCM, DJVU, DNG, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PNG, SVG, TIF, TIFF, WEBP
**Markup:** HTML, MHT, MHTML, XML
**Portable:** PDF, TEX, XPS
**Metafile:** EMF, WMF
**Other:** PCL, PS

## Platform Independence

GroupDocs.Comparison Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with GroupDocs.Comparison Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Comparison-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Comparison assembly in your project. If you already have GroupDocs.Comparison Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Comparison-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-dotnet) for other common usage scenarios.

## Use C# Code to Compare two DOCX Files and Fetch Changes

```csharp
var configuration = new Configuration
{
    AppSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    AppKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
};

// Initiate API object
var apiInstance = new ChangesApi(configuration);

// Comparison Request
ComparisonRequest comparisonRequest = new ComparisonRequest()
{
    // Comparison Request Settings
    Settings = new ComparisonRequestSettings()
    {
        GenerateSummaryPage = true,
        ShowDeletedContent = true,
        StyleChangeDetection = true,
        UseFramesForDelInsElements = false,
        DetailLevel = "Low",
        DeletedItemsStyle = new StyleSettingsValues()
        {
            BeginSeparatorString = "",
            EndSeparatorString = "",
            Color = new Color().Red
        },
        InsertedItemsStyle = new StyleSettingsValues()
        {
            BeginSeparatorString = "",
            EndSeparatorString = "",
            Color = new Color().Blue
        },
        StyleChangedItemsStyle = new StyleSettingsValues()
        {
            BeginSeparatorString = "",
            EndSeparatorString = "",
            Color = new Color().Green
        },
        CalculateComponentCoordinates = false,
        CloneMetadata = "Source",
        MarkDeletedInsertedContentDeep = false,
        MetaData = new ComparisonMetadataValues()
        {
            Author = "GroupDocs",
            Company = "GroupDocs",
            LastSaveBy = "GroupDocs"
        },
        Password = "",
        PasswordSaveOption = ""
    },
    // Source file
    SourceFile = new ComparisonFileInfo()
    {
        Folder = "comparisons",
        Name = "source.docx",
        Password = ""
    }
};

List<ComparisonFileInfo> targets = new List<ComparisonFileInfo>();
// Target file
targets.Add(new ComparisonFileInfo()
{
    Folder = "comparisons",
    Name = "target.docx",
    Password = ""
});
// Target file - single or multiple target files are allowed.
comparisonRequest.TargetFiles = targets.ToArray();

// Accept or Reject changes
comparisonRequest.Changes = new List<ComparisonChange>();
comparisonRequest.Changes.Add(new ComparisonChange() { Id = 0, Action = "Accept" });
comparisonRequest.Changes.Add(new ComparisonChange() { Id = 1, Action = "Reject" });

// API call for response.
var response = apiInstance.PostChanges(new Model.Requests.PostChangesRequest() { Request = comparisonRequest });

Console.WriteLine(string.Format("{0}: {1}", "response is List<ComparisonChange>", response.Count.ToString()));
```

[Product Page](https://products.groupdocs.cloud/comparison/net) | [Documentation](https://wiki.groupdocs.cloud/comparisoncloud/) | [API Reference](https://apireference.groupdocs.cloud/comparison/) | [Code Samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/comparison/) | [Free Support](https://forum.groupdocs.cloud/c/comparison) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)