Use this REST API to enhance your C#, ASP.NET & other .NET apps to edit documents, spreadsheets, presentations of 40+ file formats from within your cloud apps.

## Cloud Document Editor Features

- Edit word processing documents in flow or paged mode.
- Extract font information for a consistent look and feel of the edited documents.
- Support for the editing of multi-tabbed spreadsheets.
- Ability to specify the index of the currently edited worksheet.
- Works with DSV (Delimiter Separated Values) files.
- Specify the separator for the CSV and TSV files.
- Flexible conversion options for dates and numbers in TSV, CSV files.
- Optimize memory usage of large CSV, TSV files.
- Fix incorrect document structure of the XML files.
- Recognize email addresses and URIs in the XML files.
- Support for highlighting and formatting options for XML files.
- Ability to extract basic information about the document.
- Support to work with files and folders in the cloud.

## Supported File Formats

**Word Processing:** DOC, DOCX, DOCM, DOT, DOTM, DOTX, FlatOPC, ODT, OTT, RTF, WordML
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLTX, XLTM, XLSB, XLAM, SXC, SpreadsheetML, ODS, FODS, DIF, DSV, CSV, TSV
**Presentation:** PPT (95), PPT (97-2003), PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, POTM, ODP, OTP
**Markup:** HTML, XML
**Other:** TXT

## Platform Independence

GroupDocs.Editor Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with GroupDocs.Editor Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Editor-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Editor assembly in your project. If you already have GroupDocs.Editor Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Editor-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-dotnet) for other common usage scenarios.

## Edit a cloud-based PPTX Presentation via C# Code

```csharp
var configuration = new Configuration(MyAppSid, MyAppKey);

var editApi = new EditApi(configuration );
var fileApi = new FileApi(configuration );

// The document already uploaded into the storage.
// Load it into editable state
var loadOptions = new PresentationLoadOptions
{
    FileInfo = new FileInfo
    {
        FilePath = "Presentation/with-notes.pptx"
    },
    OutputPath = "output",
    SlideNumber = 0
};
var loadResult = editApi.Load(new LoadRequest(loadOptions));

// Download html document
var stream = fileApi.DownloadFile(new DownloadFileRequest(loadResult.HtmlPath));
var htmlString = new StreamReader(stream, Encoding.UTF8).ReadToEnd();

// Edit something...
htmlString = htmlString.Replace("Slide sub-heading", "Hello world!");

// Upload html back to storage
fileApi.UploadFile(new UploadFileRequest(loadResult.HtmlPath,
    new MemoryStream(Encoding.UTF8.GetBytes(htmlString))));

// Save html back to pptx
var saveOptions = new PresentationSaveOptions
{
    FileInfo = loadOptions.FileInfo,
    OutputPath = "output/edited.pptx",
    HtmlPath = loadResult.HtmlPath,
    ResourcesPath = loadResult.ResourcesPath
};
var saveResult = editApi.Save(new SaveRequest(saveOptions));
```

[Product Page](https://products.groupdocs.cloud/editor/net) | [Documentation](https://wiki.groupdocs.cloud/editorcloud/) | [API Reference](https://apireference.groupdocs.cloud/editor/) | [Code Samples](https://github.com/groupdocs-editor-cloud/groupdocs-editor-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/) | [Free Support](https://forum.groupdocs.cloud/c/editor) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)