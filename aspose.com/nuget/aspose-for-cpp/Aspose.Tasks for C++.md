# C++ API to Process Project Files

A standalone C++ library that enables the C++ developers to [generate, update, render, & convert project files](https://products.aspose.com/tasks/cpp) from within C++ projects without Microsoft Project®.

## Project File Processing Features

- [Create an empty project file](https://docs.aspose.com/tasks/cpp/creating-and-saving/) and save it as XML, to stream or to Microsoft MPP file.
- Supports encoding of the `MPX` files.
- [Read and write default properties of projects](https://docs.aspose.com/tasks/cpp/default-project-properties/) to speed up the project setup.
- [Set the project calculation mode](https://docs.aspose.com/tasks/cpp/project-calculation-modes/) to be manual, automatic or none.
- Read and write [project calendar properties](https://docs.aspose.com/tasks/cpp/calendar-properties/), such as, fiscal year and weekday properties.
- Read and write [project currency properties](https://docs.aspose.com/tasks/cpp/currency-properties/).
- [Perform project rescheduling](https://docs.aspose.com/tasks/cpp/project-rescheduling/) from start, finish date or reschedule only the incomplete tasks.
- Offers various [project utility features](https://docs.aspose.com/tasks/cpp/utility-features/), such as, calculate critical path, read filter data, extract embedded objects etc.
- Use Task, Resource and Project fields as a [formula in expressions](https://docs.aspose.com/tasks/cpp/formula-expressions/).
- Identify [Cross Project Tasks](https://docs.aspose.com/tasks/cpp/cross-project-predecessors/), get [predecessor tasks](https://docs.aspose.com/tasks/cpp/cross-project-predecessors/) and cross project predecessor tasks.
- Supports working with [task links](https://docs.aspose.com/tasks/cpp/creating-task-links/), baselines, project resources, and VBA.
- Convert project data to other [supported file formats](https://docs.aspose.com/tasks/cpp/supported-file-formats/).

## New Features & Enhancements in Version 20.7

- Aspose.Tasks for C++ is based on the .NET version of the API and provides strictly the same functionality as Aspose.Tasks for .NET provides, excluding printing, database I/O operations, and `EMF`/`WMF` format support.
- Added the ability to specify the non-default path for Project Server's PWA URL.

## Breaking change in Project Server credential usage

In Aspose.Tasks for .NET 20.7 the requirements to a site URL for Project Server credentials have been changed.

Users now should specify the full URL of *PWA* endpoint when using `ProjectServerCredentials`:

Before Aspose.Tasks for .NET 20.7:

```c#
var windowsCredentials = ...
var projectServerCredentials = new ProjectServerCredentials("http://project_server_instance.local", windowsCredentials);
```

Since Aspose.Tasks for .NET 20.7:

```c#
var windowsCredentials = ...
var projectServerCredentials = new ProjectServerCredentials("http://project_server_instance.local/sites/pwa", windowsCredentials);
```

## Read & Write Project Files

**Microsoft Project®:** MPP, MPT, MPX, XML

## Save Project Data As

**Primavera:** P6 XML, PM XER
**Microsoft Excel®:** XLSX
**Fixed Layout:** PDF
**Images:** JPEG, PNG, TIF, SVG
**Text:** TXT
**Others:** HTML

## Getting Started with Aspose.Tasks for C++

Are you ready to give Aspose.Tasks for C++ a try? Simply execute `Install-Package Aspose.Tasks.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Tasks for C++ and want to upgrade the version, please execute `Update-Package Aspose.Tasks.Cpp` to get the latest version.

### Convert Microsoft Project MPP Data to HTML

Try executing the below code to see how Aspose.Tasks for C++ performs in your environment. You may also check the [GitHub Repository](https://github.com/aspose-tasks/Aspose.Tasks-for-C) for other common usage scenarios. 

```c++
System::SharedPtr<Project> project = System::MakeObject<Project>(u"template.mpp");
System::SharedPtr<HtmlSaveOptions> option = System::MakeObject<HtmlSaveOptions>();
project->Save(u"output.html", option);
```

### Create Project from Scratch using C++

Following code sample shows how to create a project file using C++ and then create a task and a sub-task within that project:

```c++
// Create project instance
System::SharedPtr<Project> project = System::MakeObject<Project>();

// Add task, sub task and save project
System::SharedPtr<Task> task = project->get_RootTask()->get_Children()->Add(u"Summary1");
System::SharedPtr<Task> subtask = task->get_Children()->Add(u"Subtask1");
project->Save(u"output.xml", Aspose::Tasks::Saving::SaveFileFormat::XML);
```

## Limitations

- No support for printing of any kind.
- No support for Project Online (PWA).
- No support for the database I/O access of any kind.
- No support for EMF/WMF format, neither itself nor as Project file inclusions.

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/tasks/cpp) | [Docs](https://docs.aspose.com/tasks/cpp/) | [Demos](https://products.aspose.app/tasks/family) | [API Reference](https://apireference.aspose.com/tasks/cpp) | [Examples](https://github.com/aspose-tasks/Aspose.Tasks-for-C) | [Blog](https://blog.aspose.com/category/tasks/) | [Free Support](https://forum.aspose.com/c/tasks) | [Temporary License](https://purchase.aspose.com/temporary-license)
