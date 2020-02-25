This task management REST API enhances your Node.js cloud-based apps to access and manage Microsoft Project & Primavera P6 files in the cloud.

Aspose.Tasks Cloud SDK for Node.js is available to you under an MIT license. Enable your cloud-based app users to retrieve project tasks and documents from cloud hosted storage to process & manipulate them within your cloud-based apps without installing Microsoft Project or Primavera P6. Aspose.Tasks Cloud SDK for Node.js allows your to fetch existing assignments, add new project assignments, change task parent, change position of the tasks within the project hierarchy, add a project calendar along with calendar exceptions, get VBA project, get time-scaled data of project, get a collection of all work weeks belonging to a project, and so much more.

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

## Read & Write MS Project Formats

MPP, MPX, XER, XML, PrimaveraP6XML

## Save MS Project As

HTML, BMP, PNG, JPEG, TIFF, SVG, CSV, TXT, XLSX, PDF, XPS

## Read MS Project Formats

MPT

## Platform Independence

Aspose.Tasks Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.Tasks Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-tasks-cloud/aspose-tasks-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.Tasks for Cloud via NPM, please execute from the command line, `npm install aspose-tasks-cloud-node --save`.

## Use Node.js to Fetch all Tasks of a Project Document

```js
const tasksApi = new TasksApi("Youre AppSid here", "Youre AppKey here");

const request: GetTasksRequest = { name: "ProjectFile.mpp", folder: "documents", storage: ""}

tasksApi.getTasks(request)
    .then((result) => {
        // Deal with a result
        console.log(result.response.statusCode);
        console.log(result.body);
    })
    .catch(function(err) {
        // Deal with an error
        console.log(err.reponse.statusCode);
        console.log(err.body);
    });
```

[Product Page](https://products.aspose.cloud/tasks/nodejs) | [Documentation](https://docs.aspose.cloud/display/taskscloud/Home) | [API Reference](https://apireference.aspose.cloud/tasks/) | [Code Samples](https://github.com/aspose-tasks-cloud/aspose-tasks-cloud-node) | [Blog](https://blog.aspose.cloud/category/tasks/) | [Free Support](https://forum.aspose.cloud/c/tasks) | [Free Trial](https://dashboard.aspose.cloud/#/apps)