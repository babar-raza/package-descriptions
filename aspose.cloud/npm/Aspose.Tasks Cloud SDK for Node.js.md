Node.js Cloud SDK wraps Aspose.Tasks REST API so you could seamlessly integrate Microsoft Project® & Primavera® P6 document generation, manipulation, conversion & inspection features into your own Node.js applications.

# Project Processing in the Cloud

[Aspose.Tasks Cloud SDK for Node.js](https://products.aspose.cloud/tasks/nodejs) allows to retrieve project tasks and documents to process & manipulate without installing Microsoft Project or Primavera P6. Aspose.Tasks Cloud SDK for Node.js allows your to fetch existing assignments, add new project assignments, change task parent, change position of the tasks within the project hierarchy, add a project calendar along with calendar exceptions, get VBA project, get time-scaled data of project, get a collection of all work weeks belonging to a project, and more. 

Feel free to explore the [Developer's Guide](https://docs.aspose.cloud/display/taskscloud/Developer+Guide) & [API Reference](https://apireference.aspose.cloud/tasks/) to know all about Aspose.Tasks Cloud API. 

## Microsoft Project Processing Features

- Add project assignments or delete project assignments along with their references.
- Get project's outline codes by index & get links of all project tasks.
- Import project from Primavera DB formats or from databases with specified connection string.
- Get UIDs of all projects contained in the file & fetch required assignment with the project based on UID.
- Manage project tasks, resource data, calendars & Work Breakdown Structure (WBS).
- Perform risk analysis using Monte Carlo simulation and create report.
- Create and set project document properties & fetch all or specific existing properties.
- Get a project's extended attributes, time scaled data or recurring info of a specific task.
- Reschedule project tasks, dates, and other settings.
- Calculate slacks & recalculate project completion.
- Fetch a project document in the desired format.
- Delete project task with its related references & rebuild task tree.

## Enhancements in Version 19.12

- Imported projects from Project Online (Server) now can be saved as `MPP` file.
- Imported projects from a database now can be saved as `MPP` file.

For the detailed notes, please visit [Aspose.Tasks Cloud 19.12 Release Notes](https://docs.aspose.cloud/display/taskscloud/Aspose.Tasks+Cloud+19.12+Release+Notes).

## Read & Write Project Formats

MPP, MPX, XER, XML, PrimaveraP6XML

## Save Project Data As

HTML, BMP, PNG, JPEG, TIFF, SVG, CSV, TXT, XLSX, PDF, XPS

## Read Project Data From

MPT

## Getting Started with Aspose.Tasks Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install @asposecloud/aspose-tasks-cloud --save` from the command line to install Aspose.Tasks Cloud SDK for Node.js via NPM.

The complete source code is available at [GitHub Repository](https://github.com/aspose-words-cloud/aspose-tasks-cloud-node).

## Use Node.js to Fetch all Tasks of a Project Document

```js
const tasksApi = new TasksApi("Your AppSid here", "Your AppKey here");

const request: GetTasksRequest = { name: "template.mpp", folder: "documents", storage: ""}

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

[Product Page](https://products.aspose.cloud/tasks/nodejs) | [Documentation](https://docs.aspose.cloud/display/taskscloud/Home) | [Live Demo](https://products.aspose.app/tasks/family) | [API Reference](https://apireference.aspose.cloud/tasks/) | [Examples](https://github.com/aspose-tasks-cloud/aspose-tasks-cloud-node) | [Blog](https://blog.aspose.cloud/category/tasks/) | [Free Support](https://forum.aspose.cloud/c/tasks) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
