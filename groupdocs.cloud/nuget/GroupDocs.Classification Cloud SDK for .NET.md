# Data Classification .NET Cloud REST API

This cloud REST API enables your C#, ASP.NET & other .NET apps to [perform classification of raw text & documents](https://products.groupdocs.cloud/classification/net). Supports IAB-2 & Documents taxonomies.

## Classification Processing Features

- Perform raw text classification.
- Perform document classification for the supported file formats.

## Supported Document Formats

**Microsoft Word:** DOC, DOCX, DOCM, DOT, DOTX, DOTM
**OpenOffice:** ODT, OTT
**Portable:** PDF
**Other:** RTF, TXT

## Supported IAB-2 Taxonomy

'Automotive',
'Books_and_Literature',
'Business_and_Finance',
'Careers',
'Education',
'Events_and_Attractions',
'Family_and_Relationships',
'Fine_Art',
'Food_&_Drink',
'Healthy_Living',
'Hobbies_&_Interests',
'Home_&_Garden',
'Medical_Health',
'Movies',
'Music_and_Audio',
'News_and_Politics',
'Personal_Finance',
'Pets',
'Pop_Culture',
'Real_Estate',
'Religion_&_Spirituality',
'Science',
'Shopping',
'Sports',
'Style_&_Fashion',
'Technology_&_Computing',
'Television',
'Travel',
'Video_Gaming'

## Supported Documents Taxonomy

ADVE - advertisements, brochures.
Email
Form
Letter
Memo - memorandums.
News - articles, including news articles.
Invoice
Report
Resume
Scientific - scientific papers.
Other - the other classes of documents or cases where the classifier is not sure.

## Getting Started

You do not need to install anything to get started with GroupDocs.Classification Cloud SDK for .Net. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

Simply execute `Install-Package GroupDocs.Classification-Cloud` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Classification assembly in your project. If you already have GroupDocs.Classification Cloud SDK for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Classification-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-dotnet) for other common usage scenarios.

## Use C# to Classify Document from Storage

```csharp
var apiInstance = new ClassificationApi(configuration);
var request = new ClassifyRequest(new BaseRequest()
{
    Document = new FileInfo()
    {
        Name = "input.docx",
        Folder = ""
    },
},
bestClassesCount: "3");

// get classification results
ClassificationResponse response = apiInstance.Classify(request);
Console.WriteLine(response.ToString());
```

[Product Page](https://products.groupdocs.cloud/classification/net) | [Documentation](https://wiki.groupdocs.cloud/classificationcloud/) | [Live Demo](https://products.groupdocs.app/classification/family) | [API Reference](https://apireference.groupdocs.cloud/classification/) | [Examples](https://github.com/groupdocs-classification-cloud/groupdocs-classification-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/classification/) | [Free Support](https://forum.groupdocs.cloud/c/classification) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
