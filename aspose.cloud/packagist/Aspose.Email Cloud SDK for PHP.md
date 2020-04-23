# Manage & Convert Email in Cloud via PHP REST API

This cloud SDK enhances your PHP cloud-based apps to work with, [manage & convert email](https://products.aspose.cloud/email/net) format files in the cloud without a 3rd party tool.

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

- Check whether an email address is disposable or not.
- Create virtual multi-account to search, fetch and delete messages from several accounts at the same time.

For the detailed notes, please visit [Aspose.Email Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/emailcloud/Aspose.Email+Cloud+20.3+Release+Notes).

## Read & Write Email Formats

**Microsoft Outlook:** MSG
**Email:** EML

## How to use the SDK

You can either directly use it in your project via [source code](https://github.com/aspose-email-cloud/aspose-email-cloud-php) or get [Packagist distribution](https://packagist.org/packages/aspose/aspose-email-cloud) (recommended).

## Prerequisites

To use this SDK, you need an App SID and an App Key; they can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) (it requires free registration in Aspose Cloud for this).

## Installation via Composer

Aspose.Email Cloud SDK for PHP is available on [Packagist](https://packagist.org/packages/aspose/aspose-email-cloud) as the `aspose-email-cloud` package. Run the following command:

```console
composer require aspose/aspose-email-cloud
```

To use the SDK, use Composer's [autoload](https://getcomposer.org/doc/00-intro.md#autoloading):

```php
require __DIR__ . '/vendor/autoload.php';
```

### Sample usage

To use the API, you should create an `EmailApi` object:

```php
$configuration = new Configuration(); // Aspose\Email\Configuration
$configuration
    ->setAppKey($_ENV["Your App Key"])
    ->setAppSid($_ENV["Your App SID"]);
$api = new EmailApi(
    null, //GuzzleHttp client, will be created automatically if parameter is null
    $configuration);
```

API calls can be synchronous or asynchronous (GuzzleHttp\Promise is used):

```php
$file = "iCalendarFileName.ics"; //iCalendar file name on storage
$folder = "path/to/iCalendar/file/on/storage";
$storage = "First Storage"; //Storage name

$result = $api->getCalendar(new GetCalendarRequest($file, $folder, $storage));
// or
$promise = $api->getCalendarAsync(new GetCalendarRequest($file, $folder, $storage));
$result = $promise->wait();
```

## Detect a person's gender by name

```php
$result = $api->aiNameGenderize(new AiNameGenderizeRequest("John Cane"));
// the result contains a list of hypothesis about a person's gender.
// all hypothesis include score, so you can use the most scored version,
// which will be the first in a list:
echo $result->getValue()[0]->getGender(); //prints "Male"
```

## Licensing

All Aspose.Email for Cloud SDKs, helper scripts and templates are licensed under [MIT License](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/HEAD/LICENSE).

[Product Page](https://products.aspose.cloud/email/php) | [Documentation](https://docs.aspose.cloud/display/emailcloud/Home) | [Live Demo](https://products.aspose.app/email/family) | [API Reference](https://apireference.aspose.cloud/email/) | [Examples](https://github.com/aspose-email-cloud/aspose-email-cloud-php) | [Blog](https://blog.aspose.cloud/category/email/) | [Free Support](https://forum.aspose.cloud/c/email) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
