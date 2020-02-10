This cloud SDK assists to develop cloud-based HTML page rendering, processing, translation & conversion apps in C#, ASP.NET & other .NET languages via REST API.

Aspose.HTML Cloud SDK for .NET lets you access your desired HTML document from the cloud storage, or fetch the HTML page with all its linked resources as a ZIP archive via page URL.

## HTML Processing Features

- Fetch HTML page along with its resources as a ZIP archive by providing page URL.
- Based on page URL, retrieve all images of an HTML page as a ZIP package.
- Load data from local file to populate HTML document template.
- Use request body to populate HTML document template.
- Convert HTML page to numerous other file formats.

## Read & Write HTML Formats

HTML, XHTML, zipped HTML, zipped XHTML, MHTML, HTML containing SVG markup, Markdown, JSON

## Save HTML As

**Fixed Layout:** PDF, XPS
**Images:** TIFF, JPEG, PNG, BMP, GIF
**Other:** TXT, ZIP (images)

## Read HTML Formats
**eBook:** EPUB
**Other:** XML, SVG

## Platform Independence

Aspose.HTML Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.HTML Cloud SDK for .NET

You do not need to install anything to get started with Aspose.HTML Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.HTML-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.HTML assembly in your project. If you already have Aspose.HTML Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.HTML-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-html-cloud/aspose-html-cloud-dotnet) for other common usage scenarios.

## Convert HTML Page to PDF based on its URL

The following code sample demonstrates, how to programmatically fetch an HTML web page via its URL and convert it into a PDF file using C# code:

```csharp
string appSID = "xxxxxxxx";
string appKey = "xxxxxxxx";
string basePath = "https://api.aspose.cloud/v3.0";

string sourceUrl = @"https://stallman.org/articles/anonymous-payments-thru-phones.html";

Aspose.Html.Cloud.Sdk.Api.ConversionApi conversionApi = new Aspose.Html.Cloud.Sdk.Api.ConversionApi(appKey, appSID, basePath);
var response = conversionApi.GetConvertDocumentToPdfByUrl(sourceUrl, 800, 1200);
```

## Extract all Images from a Web-based HTML Page using API

The following C# code sample elaborates, how to programmatically extract all images of an HTML web page by providing its URL:

```csharp
var url = @"http://www.sukidog.com/jpierre/strings/why.htm";
Stream stream = DocumentApi.GetDocumentImagesByUrl(url);
```

[Product Page](https://products.aspose.cloud/html/net) | [Documentation](https://docs.aspose.cloud/display/htmlcloud/Home) | [API Reference](https://apireference.aspose.cloud/html/) | [Code Samples](https://github.com/aspose-html-cloud/aspose-html-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/html/) | [Free Support](https://forum.aspose.cloud/c/html) | [Free Trial](https://dashboard.aspose.cloud/#/apps)