Python Cloud SDK wraps Aspose.Email REST API so you could seamlessly integrate Microsoft Outlook® message generation, manipulation & conversion features into your own Python applications.

[Aspose.Email Cloud SDK for Python](https://products.aspose.cloud/email/python) allows you to create email processing applications that could work with common email file formats in the cloud. You can convert emails to other formats, read message properties and download attachment from messages. Not only that, Aspose.Email Cloud allows to work with [iCalendar (RFC 5545)](https://docs.aspose.cloud/display/emailcloud/iCalendar+Support), [MAPI (X.400 XAPIA)](https://docs.aspose.cloud/display/emailcloud/MAPI+Support) & [VCard](https://docs.aspose.cloud/display/emailcloud/Operate+VCard) via API models. Have a look at the [API Endpoints](https://github.com/aspose-email-cloud/aspose-email-cloud-python/tree/master/sdk) to know all possible functions.

## Email Processing Features

- Convert messages to other formats such as MSG, EML, HTML and MHTL.
- Read message properties such as sender, receiver, message sent date, subject and so on.
- Add or extract attachments to & from email messages.
- Process iCalendar, MAPI & VCard file types.
- Supports AI functionalities:
  - Business card recognition.
  - Parse and handle personal names.

## New Features in Version 20.3

- Ability to determine whether an email address is disposable or not.
- Ability to create virtual multi-account to search, fetch and delete messages from several accounts at the same time.

For the detailed notes, please visit [Aspose.Email Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/emailcloud/Aspose.Email+Cloud+20.3+Release+Notes).

## Read & Write

**Email:** MSG, EML
**Web:** HTML, MHTML

## Getting Started with Aspose.Email Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `pip install aspose-email-cloud` from the command line to install Aspose.Email Cloud SDK for Python via PIP.

### Initialize `EmailApi`

```python
from AsposeEmailCloudSdk import api #EmailApi class is here
from AsposeEmailCloudSdk import models #REST API models are here
from AsposeEmailCloudSdk.models import requests #Request models are here (all API calls use corresponding request model class)

app_sid = 'Your App SID'
app_key = 'Your App Key'
email_api = api.EmailApi(app_key, app_sid)
```

API calls can be synchronous or asynchronous as demonstrated below.

```python
result = email_api.get_calendar(
    requests.GetCalendarRequest(
        calendar_file,
        folder,
        storage))
# or
async_result = email_api.get_calendar_async( #returns multiprocessing.pool.AsyncResult
    requests.GetCalendarRequest(
        calendar_file,
        folder,
        storage))
result = async_result.get()
```

## Create New Email Message via Python

```python
#Instantiate Aspose Storage API SDK
storage_apiClient = asposestoragecloud.ApiClient.ApiClient(apiKey, appSid, True)
storageApi = StorageApi(storage_apiClient)
#Instantiate Aspose Email API SDK
api_client = asposeemailcloud.ApiClient.ApiClient(apiKey, appSid, True)
emailApi = EmailApi(api_client);

#set input file name
name =  "email_test2.eml"

body = EmailDocument.EmailDocument()

emailBody = EmailProperty.EmailProperty()
emailTo = EmailProperty.EmailProperty()
emailFrom = EmailProperty.EmailProperty()

emailBody.Name = "Body"
emailBody.Value = "This is body"

emailTo.Name = "To"
emailTo.Value = "developer@aspose.com"

emailFrom.Name = "From"
emailFrom.Value = "sales@aspose.com"

emailProps = EmailProperties.EmailProperties()
emailProps.List = [emailBody, emailTo, emailFrom]

body.DocumentProperties = emailProps
body.Format = "eml"

try:
    #upload file to aspose cloud storage
    #response = storageApi.PutCreate(name, data_folder + name)

    #invoke Aspose.Email Cloud SDK API to add new email
    response = emailApi.PutCreateNewEmail(name, body)

    if(response.Status == 'OK'):
        #download email from cloud storage
        response = storageApi.GetDownload(Path=name)
        outfilename = "c:/temp/" + name
        with open(outfilename, 'wb') as f:
                    for chunk in response.InputStream:
                        f.write(chunk)
except ApiException as ex:
            print "ApiException:"
            print "Code:" + str(ex.code)
            print "Message:" + ex.message
```

## Getting Started with Business Card API

The following are a few common use-cases. Read more about the [Business Card API](https://docs.aspose.cloud/display/emailcloud/Working+with+Contact+Cards).

### Parse Business Card Images to VCard File with Python

```python
storage = 'First Storage' # Your storage name
file_name = 'some_file_name.png' #Supports different image formats: PNG, JPEG, BMP, TIFF, GIF, etc.
image_file = 'some/business/card/image/file/on/disk.png'
folder = 'some/folder/path/on/storage'
# Upload business card image to storage
storage_location = folder + '/' + file_name
email_api.upload_file(
    requests.UploadFileRequest(storage_location, image_file, storage))

out_folder_path = 'some/other/folder/path/on/storage' # Business card recognition results will be saved here
email_api.create_folder(requests.CreateFolderRequest(out_folder_path, storage))
# Call business card recognition action
result = email_api.ai_bcr_parse_storage(requests.AiBcrParseStorageRequest(
    models.AiBcrParseStorageRq(
        images=[
            models.AiBcrImageStorageFile(
                True, #Flag isSingle determines that image contains single VCard or more.
                      #Only single VCard on image variant is supported in current version.
                models.StorageFileLocation(storage, folder, file_name))],
        out_folder=models.StorageFolderLocation(storage, out_folder_path))))
# Get file name from recognition result
contact_file = result.value[0] # result.value can contain multiple files, if we sent multicard images or multiple images
# You can download the VCard file, which produced by the recognition method ...
downloaded = email_api.download_file(requests.DownloadFileRequest(
    contact_file.folder_path + '/' + contact_file.file_name,
    storage))
# ... and print it to console
with open(downloaded, 'r') as f:
    file_data = f.read()
    print(file_data)
# Also, you can get VCard object properties’ list using Contact API
contact_properties = email_api.get_contact_properties(
    requests.GetContactPropertiesRequest(
        'VCard',
        contact_file.file_name,
        contact_file.folder_path,
        contact_file.storage))
# All VCard’s properties are available as a list. Complex properties are represented as hierarchical structures.
# Let's print all primitive properties’ values:
primitives = (prop for prop in contact_properties.internal_properties
    if  prop.type == 'PrimitiveObject')
for prop in primitives:
    print('Property name: ' + prop.name + ' value: ' + prop.value)
```

### Parse `VCard` Images without using Storage

```python
# Read image from file and convert it to Base64 string
image_file = 'some/business/card/image/file/on/disk.png'
image_data = None
with open(image_file, 'rb') as f:
    file_data = f.read()
    image_data = str(base64.b64encode(file_data), 'utf-8')
result = email_api.ai_bcr_parse(requests.AiBcrParseRequest(
    models.AiBcrBase64Rq(images=[
        models.AiBcrBase64Image(True, image_data)])))
# Result contains all recognized VCard objects (only the one in our case)
contact_properties = result.value[0]
# VCard object is available as a list of properties, without any external calls:
primitives = (prop for prop in contact_properties.internal_properties
    if  prop.type == 'PrimitiveObject')
for prop in primitives:
    print('Property name: ' + prop.name + ' value: ' + prop.value)
```

## Getting Started with the Name API

The following are a few common use-cases. Read more about the [Name API](https://docs.aspose.cloud/display/emailcloud/Working+with+Name+API).

### Detect Person's Gender from Name

```python
result = email_api.ai_name_genderize(
    requests.AiNameGenderizeRequest('John Cane'))
# the result contains a list of hypothesis about a person's gender.
# all hypothesis include score, so you can use the most scored version,
# which will be the first in a list:
print(result.value[0].gender) # prints 'Male'
```

### Expand Person's Name into a List of Alternatives

```python
name = 'Smith Bobby'
result = email_api.ai_name_expand(
    requests.AiNameExpandRequest(name))
expanded_names = list(weighted.name for weighted in result.names)
for (expanded_name in expanded_names):
    print expanded_name # prints 'Mr. Smith', 'B. Smith', etc.
```

[Product Page](https://products.aspose.cloud/email/python) | [Documentation](https://docs.aspose.cloud/display/emailcloud/Home) | [API Reference](https://apireference.aspose.cloud/email/) | [Code Samples](https://github.com/aspose-email-cloud/aspose-email-cloud-python) | [Blog](https://blog.aspose.cloud/category/email/) | [Free Support](https://forum.aspose.cloud/c/email) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
