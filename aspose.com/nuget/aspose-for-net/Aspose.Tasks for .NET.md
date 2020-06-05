# .NET API to Manipulate Project Files

[Aspose.Tasks for .NET](https://products.aspose.com/tasks/net) is a C# library that assists developers in generating, editing, rendering & conversion of Project files without needing Microsoft Project®.

Aspose.Tasks for .NET on premise API enables you to work with projects, formulas, calendars, calendar exceptions, tasks, task links, task baselines, project resources, resource assignments, currencies, handling exceptions, reporting services, and project risk analysis (Monte Carlo Simulation).

## Project File Processing Features

- Set project schedule type, start date & finish date.
- Modify project standard rate, overtime rate, task type, fixed cost accrual etc.
- Manage [project extended attributes](https://docs.aspose.com/display/tasksnet/Working+with+Extended+Attributes+of+a+Project).
- Define [project calendar](https://docs.aspose.com/display/tasksnet/Working+with+Calendars) and weekdays.
- Task baseline scheduling and duration.
- Work with task constraints.
- Apply links among tasks.
- Create task milestone, estimated critical or effort driven tasks.
- Manage resource cost and variance.
- Assignment [cost](https://docs.aspose.com/display/tasksnet/Managing+Task+Costs) and [budget](https://docs.aspose.com/display/tasksnet/Assignment+Budget).
- Encode MPX files.
- Comprehensive project reporting (15+ types of reports).

## Enhancements in Version 20.6

- Improved performance of timephased data calculation.
- Added rendering of customized Gridlines for `Middleopottom Tier Column` in Gantt chart view.
- Added the ability to render 3 and 1 tier(s) on timescale.

For the detailed notes, please visit [Aspose.Tasks for .NET 20.6 Release Notes](https://docs.aspose.com/display/tasksnet/Aspose.Tasks+for+.NET+20.6+Release+Notes).

## Read & Write Project Formats

**Microsoft Project:** MPP, MPT, MPX, XML

## Save Projects As

**Primavera:** P6 XML, PM XER
**Microsoft Office:** XLSX
**Fixed Layout:** PDF
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Text:** TXT
**Others:** HTML

## Platform Independence

You can use Aspose.Tasks for .NET to build any type of a 32-bit or 64-bit .NET application including ASP.NET, WCF, WinForms, WPF etc. It is possible to use Aspose.Tasks for .NET via COM Interop from ASP, Perl, PHP and Python. You can also use Aspose.Tasks for .NET to build applications with Mono.

## Getting Started with Aspose.Tasks for .NET

Are you ready to give Aspose.Tasks for .NET a try? Simply execute `Install-Package Aspose.Tasks` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Tasks for .NET and want to upgrade the version, please execute `Update-Package Aspose.Tasks` to get the latest version.

## Convert Microsoft Project MPP File to Primavera MPX Format

You can execute below code snippet to see how Aspose.Tasks API performs against your own samples or check the [GitHub Repository](https://github.com/aspose-tasks/Aspose.Tasks-for-.NET) for other common usage scenarios.

```csharp
Project project = new Project(dir + "template.mpp");

// Save project in desired format
project.Save(dir + "output.xml", SaveFileFormat.MPX);
```

## Use C# to Create a Project file, a Task and Sub-task within it

Aspose.Tasks for .NET a lot of C# public classes to define and manage project tasks. Following code sample shows how to create a project file in C# and then create a task and a sub-task within that project:

```csharp
// Create project instance
Project project = new Project();

// Add task, sub task and save project
Task task = project.RootTask.Children.Add("Summary1");
Task subtask = task.Children.Add("Subtask1");
project.Save(dir + "output.xml", SaveFileFormat.XML);
```

[Product Page](https://products.aspose.com/tasks/net) | [Docs](https://docs.aspose.com/display/tasksnet/Home) | [Demos](https://products.aspose.app/tasks/family) | [API Reference](https://apireference.aspose.com/tasks/net) | [Examples](https://github.com/aspose-tasks/Aspose.Tasks-for-.NET) | [Blog](https://blog.aspose.com/category/tasks/) | [Free Support](https://forum.aspose.com/c/tasks) |  [Temporary License](https://purchase.aspose.com/temporary-license)
