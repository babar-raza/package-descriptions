# Manipulate Project Files via .NET Cloud REST API

This task management REST API enhances your C#, ASP.NET & other .NET cloud-based apps to [access and manage Microsoft Project & Primavera P6 files](https://products.aspose.cloud/tasks/net) in the cloud.

## MS Project Processing Features

- Add project assignments or delete project assignments along with their references.
- Get project's outline codes by index & get links of all project tasks.
- Import project from Primavera DB formats or from databases with specified connection string.
- Get UIDs of all projects contained in the file & fetch required assignment with the project based on UID.
- Manage project tasks, resource data, calendars & Work Breakdown Structure (WBS).
- Perform risk analysis using Monte Carlo simulation and create report.
- Create and set project document properties & fetch all or specific existing properties.
- Get a project's extended attributes, time scaled data or recurring info of a specific task.
- Reschedule project tasks, dates, and other settings.
- Calculate slacks & recalculate project completion or incompletion work.
- Fetch a project document in the desired format.
- Delete project task with its related references & rebuild task tree.

## New Features in Version 19.12.0

- Imported projects from Project Online (Server) can now be saved as `MPP` file.
- Imported projects from a database can now be saved as `MPP` file.

For the detailed notes, please visit [Aspose.Tasks Cloud 19.12 Release Notes](https://docs.aspose.cloud/display/taskscloud/Aspose.Tasks+Cloud+19.12+Release+Notes).

## Read & Write MS Project Formats

MPP, MPX, XER, XML, PrimaveraP6XML

## Save MS Project As

HTML, BMP, PNG, JPEG, TIFF, SVG, CSV, TXT, XLSX, PDF, XPS

## Read MS Project Formats

MPT

## Platform Independence

Aspose.Tasks Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.Tasks Cloud SDK for .NET

You do not need to install anything to get started with Aspose.Tasks Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.Tasks-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.Tasks assembly in your project. If you already have Aspose.Tasks Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.Tasks-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-tasks-cloud/aspose-tasks-cloud-dotnet) for other common usage scenarios.

## Use C# to Extract a Specific Task from Cloud MPP File

The following C# code sample demonstrates, how to get Microsoft Project MPP file in the cloud and extract a specific task based on its UID:

```csharp
var remoteName = await UploadFileToStorageAsync("Input_Project_File.mpp");

var tasksResponse = await TasksApi.GetTaskAsync(new GetTaskRequest
    {
        TaskUid = 5,
        Name = remoteName,
        Folder = this.DataFolder
    });

Assert.AreEqual((int)HttpStatusCode.OK, tasksResponse.Code);
Assert.IsNotNull(tasksResponse.Task);
Assert.AreEqual(5, tasksResponse.Task.Uid);
CollectionAssert.AreEquivalent(new[] { 1, 2, 3, 4 }, tasksResponse.Task.SubtasksUids);
Assert.AreEqual(new DateTime(2015, 8, 3, 8, 0, 0), tasksResponse.Task.Start);
Assert.AreEqual(new DateTime(2015, 8, 6, 17, 0, 0), tasksResponse.Task.Finish);
Assert.AreEqual(new TimeSpan(1, 8, 0, 0, 0), tasksResponse.Task.RemainingWork);
Assert.AreEqual(1920, tasksResponse.Task.WorkVariance);
```

## Generate Project Risk Analysis Report via C# Code

The following code sample elaborates, how to fetch a cloud-based Microsoft Project MPP file and generate a Risk Analysis Report in the PDF format using C# code:

```csharp
var remoteName = await UploadFileToStorageAsync("Input_Project_File.mpp");
var response = await TasksApi.GetRiskAnalysisReportAsync(new GetRiskAnalysisReportRequest()
    {
        DistributionType = ProbabilityDistributionType.Normal,
        ConfidenceLevel = ConfidenceLevel.CL85,
        Optimistic = 80,
        Pessimistic = 130,
        Iterations = 200,
        TaskUid = 1,
        Name = remoteName,
        Folder = this.DataFolder
    });
Assert.IsTrue(response.Length > 0);
var buffer = new byte[4];
response.Read(buffer, 0, 4);
Assert.AreEqual("%PDF", Encoding.ASCII.GetString(buffer));
```

[Product Page](https://products.aspose.cloud/tasks/net) | [Documentation](https://docs.aspose.cloud/display/taskscloud/Home) | [API Reference](https://apireference.aspose.cloud/tasks/) | [Code Samples](https://github.com/aspose-tasks-cloud/aspose-tasks-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/tasks/) | [Free Support](https://forum.aspose.cloud/c/tasks) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
