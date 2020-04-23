# Manage & Convert Email in Cloud via .NET REST API

This cloud SDK enhances your C#, ASP.NET & other .NET cloud-based apps to work with, [manage & convert email](https://products.aspose.cloud/email/net) format files in the cloud without a 3rd party tool.

## Email Processing Features

- Supports OAuth feature.
- Send or append MIME or simple email messages.
- Fetch list of email messages.
- Mark specific email messages with a red flag.
- Set or download email attachments.
- Supports email file format conversion among popular email formats.
- Get email properties.
- Create, list or delete email folders.

## New Features in Version 20.3

- Ability to determine whether an email address is disposable or not.
- Ability to create virtual multi-account to search, fetch and delete messages from several accounts at the same time.

For the detailed notes, please visit [Aspose.Email Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/emailcloud/Aspose.Email+Cloud+20.3+Release+Notes).

## Read & Write Email Formats

**Microsoft Outlook:** MSG
**Email:** EML

## Getting Started with Aspose.Email Cloud SDK for .NET

You do not need to install anything to get started with Aspose.Email Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information. 

Simply execute `Install-Package Aspose.Email-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.Email assembly in your project. If you already have Aspose.Email Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.Email-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet) for other common usage scenarios.

## Convert an Email EML File to MSG Format via C# Code

The following code sample demonstrates, how to fetch Microsoft Outlook, Apple Mail or Mozilla Thunderbird emails in the EML format and convert them into MSG format using simple call to Aspose.Email Cloud SDK for .NET in C# code:

```csharp
// Please get your APP_KEY & APP_ID by signing up for free at https://dashboard.aspose.cloud/#/apps.
EmailApi emailApi = new EmailApi(Common.APP_KEY, Common.APP_SID, Common.BASEPATH);
StorageApi storageApi = new StorageApi(Common.APP_KEY, Common.APP_SID, Common.BASEPATH);

String name = "email_test";
String fileName = name + ".eml";
String format = "msg";
String storage = "";
String folder = "";
String outPath = "";

// Upload source file to aspose cloud storage
storageApi.PutCreate(fileName, "", "", System.IO.File.ReadAllBytes(Common.GetDataDir() + fileName));

// Invoke Aspose.Email Cloud SDK API to convert email to other formats
ResponseMessage apiResponse = emailApi.GetDocumentWithFormat(fileName, format, storage, folder, outPath);

System.IO.File.WriteAllBytes(Common.GetDataDir() + fileName, apiResponse.ResponseStream);
Console.WriteLine("Convert Emails to Other Formats, Done!");
```

[Product Page](https://products.aspose.cloud/email/net) | [Documentation](https://docs.aspose.cloud/display/emailcloud/Home) | [Live Demo](https://products.aspose.app/email/family) | [API Reference](https://apireference.aspose.cloud/email/) | [Examples](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/email/) | [Free Support](https://forum.aspose.cloud/c/email) | [Free Trial](https://dashboard.aspose.cloud/#/apps)