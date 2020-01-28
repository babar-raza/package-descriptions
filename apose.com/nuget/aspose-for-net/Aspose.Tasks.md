Aspose.Tasks for .NET API C# library assists you to generate, update, render, & convert project files within your .NET projects without Microsoft Project®.

Aspose.Tasks for .NET on premise API enables you to work with projects, formulas, calendars, calendar exceptions, tasks, task links, task baselines, project resources, resource assignments, currencies, handling exceptions, reporting services, and project risk analysis (Monte Carlo Simulation).

## Project File Processing Features
Some of the Aspose.Tasks for .NET features are as follows:
- Set project schedule type, start date & finish date
- Modify project standard rate, overtime rate, task type, fixed cost accrual etc.
- Manage project extended attributes
- Define project calendar and weekdays
- Task baseline scheduling and duration
- Task constraints
- Apply links among tasks
- Create task milestone, estimated critical or effort driven tasks
- Manage resource cost and variance
- Assignment cost and budget
- Encode MPX files
- Comprehensive project reporting (15+ types of reports)

## Read & Write Project Formats
**Microsoft Project:** MPP, MPT, MPX, XML

## Save Projects As
**Primavera:** P6 XML, PM XER
**Microsoft Excel®:** XLSX, XML
**Fixed Layout:** PDF
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Text:** TXT
**Others:** HTML


## Platform Independence
You can use Aspose.Tasks for .NET to build any type of a 32-bit or 64-bit .NET application including ASP<span>.</span>NET, WCF, WinForms, WPF etc. It is possible to use Aspose.Tasks for .NET via COM Interop from ASP, Perl, PHP and Python. You can also use Aspose.Tasks for .NET to build applications with Mono.

## Getting Started with Aspose.Tasks for .NET
Are you ready to give Aspose.Tasks for .NET a try? Simply execute `Install-Package Aspose.Tasks` from **[Package Manager Console](https://www.nuget.org/packages/Aspose.Tasks/)** in Visual Studio to fetch the NuGet package. If you already have Aspose.Tasks for .NET and want to upgrade the version, please execute `Update-Package Aspose.Tasks` to get the latest version.

### Convert Microsoft Project MPP File to Primavera MPX Format
You can execute below code snippet to see how Aspose.Tasks API performs against your own samples or check the [GitHub Repository](https://github.com/aspose-tasks/Aspose.Tasks-for-.NET) for other common usage scenarios.
```csharp
Project project = new Project(dataDir + "template.mpp");

// Save project in desired format
project.Save(dataDir + "output.xml", SaveFileFormat.MPX);
```

## Create a Project file, a Task and Sub-task within it using C# 
Aspose.Tasks for .NET a lot of C# public classes to define and manage project tasks. Following code sample shows how to create a project file in C# and then create a task and a sub-task within that project:
```csharp
// Create project instance
Project project = new Project();

// Add task, sub task and save project
Task task = project.RootTask.Children.Add("Summary1");
Task subtask = task.Children.Add("Subtask1");
project.Save(dataDir + "CreateTasks_out.xml", SaveFileFormat.XML);
```

[Product Page](https://products.aspose.com/tasks/net) | [Documentation](https://docs.aspose.com/display/tasksnet/Home) | [API Reference](https://apireference.aspose.com/net/tasks) | [Code Examples](https://github.com/aspose-tasks/Aspose.Tasks-for-.NET) | [Blog](https://blog.aspose.com/category/tasks/) | [Free Support](https://forum.aspose.com/c/tasks) |  [Temporary License](https://purchase.aspose.com/temporary-license)