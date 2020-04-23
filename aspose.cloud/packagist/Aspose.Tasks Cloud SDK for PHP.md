# Manipulate Project Files via PHP Cloud REST API

This task management REST API enhances your PHP cloud-based apps to [access and manage Microsoft Project & Primavera P6 files](https://products.aspose.cloud/tasks/net) in the cloud.

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

## New Features in Version 19.12

- Imported projects from Project Online (Server) can now be saved as `MPP` file.
- Imported projects from a database can now be saved as `MPP` file.

For the detailed notes, please visit [Aspose.Tasks Cloud 19.12 Release Notes](https://docs.aspose.cloud/display/taskscloud/Aspose.Tasks+Cloud+19.12+Release+Notes).

## Read & Write MS Project Formats

MPP, MPX, XER, XML, PrimaveraP6XML

## Save MS Project As

HTML, BMP, PNG, JPEG, TIFF, SVG, CSV, TXT, XLSX, PDF, XPS

## Read MS Project Formats

MPT

## Getting Started with Aspose.Tasks Cloud SDK for PHP

This repository contains Aspose.Tasks Cloud SDK for PHP source code. To use these SDKs, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) ([free registration](https://id.containerize.com/signup?clientId=prod.discourse.aspose&redirectUrl=https://forum.aspose.cloud/session/sso) is required).

Please check the [GitHub Repository](https://github.com/aspose-Tasks-cloud/aspose-Tass-cloud-php) for the source code and examples.

## How to use the SDK

You can either directly use it in your project via source code or get [Packagist distribution](https://packagist.org/packages/aspose/tasks-sdk-php) (recommended).

## Installation via Composer

Aspose.Tasks Cloud SDK for PHP is available on `Packagist` as the `tasks-sdk-php` package. Run the following command:

```console
composer require aspose/tasks-sdk-php
```

To use the SDK, use Composer's [autoload](https://getcomposer.org/doc/00-intro.md#autoloading):

```php
require __DIR__ . '/vendor/autoload.php';
```

### Using PHP Code to Add Calendar to MPP Project

```php
require_once realpath(__DIR__ . '/..') . '/vendor/autoload.php';
require_once realpath(__DIR__ . '/..') . '/Utils.php';

use Aspose\Tasks\TasksApi;
use Aspose\Tasks\AsposeApp;

class Calendars {

    public $tasksApi;

    public function __construct() {
        AsposeApp::$appSID = Utils::appSID;
        AsposeApp::$apiKey = Utils::apiKey;
        $this->tasksApi = new TasksApi();
    }

    public function postProjectCalendar() {
        $body = '{"Name": "TestCalender", "Uid": 0}';
        $name = 'sample-project.mpp';
        Utils::uploadFile($name);
        $result = $this->tasksApi->PostProjectCalendar($name, $fileName = null, $storage = null, $folder = null, $body);
        print_r($result);
    }
}

$calendars = new Calendars();
$calendars->postProjectCalendar();
```

[Product Page](https://products.aspose.cloud/tasks/php) | [Documentation](https://docs.aspose.cloud/display/taskscloud/Home) | [Demo](https://products.aspose.app/tasks/family) | [API Reference](https://apireference.aspose.cloud/tasks/) | [Examples](https://github.com/aspose-tasks-cloud/aspose-tasks-cloud-php) | [Blog](https://blog.aspose.cloud/category/tasks/) | [Free Support](https://forum.aspose.cloud/c/tasks) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
