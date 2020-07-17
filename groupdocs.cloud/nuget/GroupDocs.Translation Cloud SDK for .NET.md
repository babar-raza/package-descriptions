# .NET SDK for Translating Cloud Documents

[GroupDocs.Translation Cloud](https://products.groupdocs.cloud/translation) is a simple SDK used to add translation of Microsoft Word documents, Microsoft Excel workbooks and plain text to your app with merely a few lines of code.

GroupDocs.Translation Cloud SDK for .NET is a simple SDK used to add the translation features into your NET cloud-based Apps. It currently supports translaton of `DOC`, `DOCX`, `DOCM`, `XLS`, `XLSX`, `XLSM` files. Just pass a specific file or text to the GroupDocs.Translation Cloud API, and it will translate and save translated file in the Cloud or will return translated text.


## Cloud Document Translation Features

- Translation of Microsoft Word and Microsoft Excel documents.
- Support for nine (9) languages and sixteen (16) language pair support.
- Translation of tables, headers, footers, footnotes / endnotes, image captions in Word documents.
- Translation of cells, charts, tables, pivot tables in Excel documents.
- Translation of plain text.
- Supports managing your files and folders in the Cloud.

## Supported Document Formats

- **Microsoft Word:** DOC, DOCX, DOCM
- **Microsoft Excel:** XLS, XLSX, XLSM

## New Features in Version 20.7

- Made the `English-Polish` language pair support available.

For the detailed notes, please visit [GroupDocs.Translation for Cloud 20.7 Release Notes](https://wiki.groupdocs.cloud/translationcloud/release-notes/release-notes-2020/groupdocs-translation-for-cloud-20-7-release-notes/).

## How to use the SDK

Our API is completely independent of your operating system, database system, or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone, and time-consuming. Therefore, we have provided support [SDKs](https://products.groupdocs.cloud/translation/family) in many development languages to make it easier to integrate with us.

## Getting Started

It is easy to get started with GroupDocs.Translation Cloud, and there is nothing to install. Create an account at [GroupDocs Cloud](https://dashboard.aspose.cloud/#/) and get your application information, then you are ready to use [SDKs](https://github.com/groupdocs-translation-cloud).

## Example

```csharp
public TranslationResponse TranslateDocument(Configuration conf)
{
    NET.Model.FileInfo fileInfo = new NET.Model.FileInfo();

    fileInfo.Name = "test.docx";
    fileInfo.Folder = "";
    fileInfo.Storage = "First Storage";
    fileInfo.SaveFile = "translation.docx";
    fileInfo.SavePath = "";
    fileInfo.Format = "docx";
    fileInfo.Pair = "en-fr";

    tring userRequest = String.Format("'[{0}]'", JsonConvert.SerializeObject(fileInfo));

    TranslationApi api = new TranslationApi(conf);
    TranslateDocumentRequest request = new TranslateDocumentRequest(userRequest);
    TranslationResponse response = api.RunTranslationTask(request);
    return response;
}

public TextResponse TranslateText(Configuration conf)
{
    TextInfo textInfo = new TextInfo();

    textInfo.Pair = "en-fr";
    textInfo.Text = "Welcome to Paris";

    string userRequest = String.Format("'[{0}]'", JsonConvert.SerializeObject(textInfo));

    TranslationApi api = new TranslationApi(conf);
    TranslateTextRequest request = new TranslateTextRequest(userRequest);
    TextResponse response = api.RunTranslationTextTask(request);
    return response;
}
```

## Quickstart

Make your solution using [SDK](https://github.com/groupdocs-translation-cloud), follow these steps:

### 1. Get API keys if you haven't

Make a personal account on [GroupDocs Cloud Dashboard](https://dashboard.groupdocs.cloud/#/) and click _Get Keys_. These keys are useful for all GroupDocs Cloud products. If you have any trouble, look at this [detailed manual](https://wiki.groupdocs.cloud/translationcloud/getting-started/create-new-app-and-get-app-key-and-sid/).

### 2. Run Demo

- Checkout the SDK.
- Open .NET core demo project.
- Set Your `AppSid` & `AppKey`.
- Run.

## Resources

[Product Page](https://products.groupdocs.cloud/translation/net) | [Docs](https://wiki.groupdocs.cloud/translationcloud/) | [Demos](https://products.groupdocs.app/viewer/family) | [API Reference](https://apireference.groupdocs.cloud/translation/) | [Examples](https://github.com/groupdocs-translation-cloud/groupdocs-translation-cloud-dotnet) | [Blog](https://blog.groupdocs.cloud/category/translation/) | [Free Support](https://forum.groupdocs.cloud/c/translation) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
