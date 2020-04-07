# .NET REST API for OMR Processing

This Cloud SDK enables you to [perform Optical Mark Recognition (OMR)](https://products.aspose.cloud/omr/net) operations on human-marked data from within your cloud-based C#, ASP.NET & other .NET apps.

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

## Getting Started with Aspose.OMR Cloud SDK for .NET

You do not need to install anything to get started with Aspose.OMR Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.OMR-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.OMR assembly in your project. If you already have Aspose.OMR Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.OMR-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-omr-cloud) for other common usage scenarios.

## Use C# to Perform Optical Mark Recognition (OMR) on PNG Images

The following code sample demonstrates, how to perform Optical Mark Recognition (OMR) operation on an PNG image file using C# code:

```csharp
// Please visit https://dashboard.aspose.cloud/#/apps to get your APIKEY & APPSID.
StorageApi storageApi = new StorageApi(APIKEY, APPSID);
OmrApi omrApi = new OmrApi(APIKEY, APPSID, BASEPATH);

string name = "AnswerSheet.png";

OMRFunctionParam param = new OMRFunctionParam();

param.FunctionParam = packedTemplateJson;

string versionId = "";
string storage = "";
storageApi.PutCreate(name, versionId, storage, System.IO.File.ReadAllBytes(pathToTheImage + name));

string folder = null;
Com.Aspose.OMR.Model.OMRResponse response = omrApi.PostRunOmrTask(name, "CorrectTemplate", param, storage, folder);
FileInfo[] resultFiles = response.Payload.Result.ResponseFiles;
```

## Limitations

- Recognition process works well with the bubbles which are at least 75% filled.
- Works on perspective (side viewed/out of focus) & rotated images under certain conditions, e.g., rotation angle within 25 degrees.
- OMR operation will show results only in text format.
- Performing OCR operation is not supported for now.

[Product Page](https://products.aspose.cloud/omr/net) | [Documentation](https://docs.aspose.cloud/display/omrcloud/Home) | [Live Demo](https://products.aspose.app/diagram/family) | [API Reference](https://apireference.aspose.cloud/omr/) | [Code Samples](https://github.com/aspose-omr-cloud) | [Blog](https://blog.aspose.cloud/category/omr/) | [Free Support](https://forum.aspose.cloud/c/omr) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
