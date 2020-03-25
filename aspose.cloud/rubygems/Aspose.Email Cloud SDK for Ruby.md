# Manage & Convert Email in Cloud via .NET REST API

This cloud SDK enhances your C#, ASP.NET & other .NET cloud-based apps to work with, [manage & convert email](https://products.aspose.cloud/email/net) format files in the cloud without a 3rd party tool.

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

## Platform Independence

Aspose.Email Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.Email Cloud SDK for Ruby

You do not need to install anything to get started with Aspose.Email Cloud SDK for Ruby. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet).

## Prerequisites

To use this SDK, you need an App SID and an App Key; they can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) (it requires free registration in Aspose Cloud for this).

## Installation

You can either directly use it in your project via source code or get [gem](https://rubygems.org/gems/aspose_email_cloud).

## Usage examples

To use the API, you should create an `EmailApi` object:

```ruby
api = EmailApi.new('Your App Key', 'Your App Sid')
```

## Business cards recognition API

See examples below:

### Parse business card images to VCard contact files

```ruby
# Upload a business card image to storage
storage = 'First Storage'
image = File.new('path/to/image')
image_file_name = 'someFileName.png' # Supports different image formats: PNG, JPEG, BMP, TIFF, GIF, etc.
api.upload_file(
    UploadFileRequestData.new(image_file_name, image, storage))
out_folder = 'some/folder/on/storage' # Business card recognition results will be saved here
api.create_folder(CreateFolderRequestData.new(out_folder, storage))
# Call business card recognition action
result = api.ai_bcr_parse_storage(AiBcrParseStorageRequestData.new(
    AiBcrParseStorageRq.new(
        nil,
        [AiBcrImageStorageFile.new(true, StorageFileLocation.new(storage, '', fileName))],
        StorageFolderLocation.new(storage, out_folder))))
# Get file name from a recognition result
contact_file = result.value[0] # result.value can contain multiple files, if we sent multicard images or multiple images
# You can download the VCard file, which produced by the recognition method
downloaded = api.download_file(DownloadFileRequestData.new(
    "#{contact_file.folder_path}/#{contact_file.file_name}", contact_file.storage))
# Let's print file contents:
content = IO.read(downloaded)
puts content
# Also, you can get VCard object properties’ list using Contact API
contact_properties = api.get_contact_properties(
    GetContactPropertiesRequestData.new(
        'vcard',
        contact_file.file_name,
        contact_file.folder_path,
        contact_file.storage))
# All VCard’s properties are available as a list. Complex properties are represented as hierarchical structures.
# Let's print all primitive properties’ values:
contact_properties.internal_properties
    .filter {|property| property.type == 'PrimitiveObject'}
    .each {|property| puts "Property name:#{property.name}, value:#{property.value}"}
```

## Name API

See examples below:

### Detect a person's gender by name

```ruby
result = api.ai_name_genderize(
    AiNameGenderizeRequestData.new('John Cane'))
# the result contains a list of hypothesis about a person's gender.
# all hypothesis include score, so you can use the most scored version, which will be the first in a list:
puts result.value[0].gender # prints 'Male'
```

### Format person's name using defined format

```ruby
result = api.ai_name_format(
    AiNameFormatRequestData.new('Mr. John Michael Cane', nil, nil, nil, nil, '%t%L%f%m'))
puts result.name # prints 'Mr. Cane J. M.'
```

[Product Page](https://products.aspose.cloud/email/net) | [Documentation](https://docs.aspose.cloud/display/emailcloud/Home) | [API Reference](https://apireference.aspose.cloud/email/) | [Code Samples](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/email/) | [Free Support](https://forum.aspose.cloud/c/email) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
