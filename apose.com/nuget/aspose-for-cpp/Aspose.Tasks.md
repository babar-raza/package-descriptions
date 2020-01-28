A standalone C++ library that enables the C++ developers to generate, update, render, & convert project files from within C++ projects without Microsoft Project®.

The component provides an easy to use API for manipulating Microsoft Project files, saving time and money compared to developing similar features from scratch. Developers can process  projects, formulas, calendars, calendar exceptions, tasks, task links, task baselines, project resources, resource assignments & currencies as well as handling exceptions, reporting services, and project risk analysis (Monte Carlo Simulation).

## Project File Processing Features
- Generate projects via API.
- Read Microsoft Project files for manipulation or just examining.
- Create & modify XML project format.
- Set project schedule type, start data & finish date.
- Modify project standard rate, overtime rate, fixed cost accrual and more.
- Manage project extended attributes.
- Define weekdays, calendar & calendar exceptions.
- Manage task baseline scheduling & duration.
- Handle task constraints.
- Create & manage links among tasks.
- Work with tasks, milestones, estimated critical, & effort driven tasks.
- Manage task resource costs & variances.
- Access task assignment costs and budget.
- Implementation of resource prefix for nested resources.
- Set CSS prefix for HTML export.
- Set custom date format while exporting to PDF.

## Read & Write Project Files
**Microsoft Project®:** MPP, MPT, MPX, XML


## Save Project Data As
**Primavera:** P6 XML, PM XER
**Microsoft Excel®:** XLSX, XML
**Fixed Layout:** PDF
**Images:** JPEG, PNG, BMP, TIFF, SVG
**Text:** TXT
**Others:** HTML


## Getting Started with Aspose.Tasks for C++
Are you ready to give Aspose.Tasks for C++ a try? Simply execute `Install-Package Aspose.Tasks.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Tasks for C++ and want to upgrade the version, please execute `Update-Package Aspose.Tasks.Cpp` to get the latest version.

Try executing the below code to see how Aspose.Tasks for C++ performs in your environment. You may also check the [GitHub Repository](https://github.com/aspose-tasks/Aspose.Tasks-for-C) for other common usage scenarios. 

### Convert Microsoft Project MPP Data to HTML
```c++
System::SharedPtr<Project> project = System::MakeObject<Project>(dataDir + u"template.mpp");
System::SharedPtr<HtmlSaveOptions> option = System::MakeObject<HtmlSaveOptions>();
project->Save(dataDir + u"output.html", option);
```

### Create Project from Scratch using C++
Following code sample shows how to create a project file using C++ and then create a task and a sub-task within that project.
```c++
// Create project instance
System::SharedPtr<Project> project = System::MakeObject<Project>();
        
// Add task, sub task and save project
System::SharedPtr<Task> task = project->get_RootTask()->get_Children()->Add(u"Summary1");
System::SharedPtr<Task> subtask = task->get_Children()->Add(u"Subtask1");
project->Save(dataDir + u"output.xml", Aspose::Tasks::Saving::SaveFileFormat::XML);
```

## Limitations
- No support for printing of any kind.
- No support for Project Online (PWA).
- No support for the database I/O access of any kind.
- No support for EMF/WMF format, neither itself nor as Project file inclusions.

[Product Page](https://products.aspose.com/tasks/cpp) | [Documentation](https://docs.aspose.com/display/taskscpp/Home) | [API Reference](https://apireference.aspose.com/cpp/tasks) | [Code Examples](https://github.com/aspose-tasks/Aspose.Tasks-for-C) | [Blog](https://blog.aspose.com/category/tasks/) | [Free Support](https://forum.aspose.com/c/tasks) | [Temporary License](https://purchase.aspose.com/temporary-license)