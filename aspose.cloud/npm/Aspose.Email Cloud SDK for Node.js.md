Node.js Cloud SDK wraps Aspose.Email REST API so you could seamlessly integrate Microsoft Outlook® email generation, manipulation, conversion & inspection features into your own Node.js applications.

# Process Emails in the Cloud

[Aspose.Email Cloud SDK for Node.js](https://products.aspose.cloud/email/nodejs) allows you to create email processing applications that could work with common email file formats in the cloud. You can convert email to other formats, read message properties and download attachment from messages your Node.js applications. Not only that, Aspose.Email Cloud allows you to work with [iCalendar (RFC 5545)](https://docs.aspose.cloud/display/emailcloud/iCalendar+Support), [MAPI (X.400 XAPIA)](https://docs.aspose.cloud/display/emailcloud/MAPI+Support) & [VCard](https://docs.aspose.cloud/display/emailcloud/Operate+VCard) via API models. Have a look at the [API Endpoints](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/master/doc/README.md) to know all possible functions.

## Email Processing Features

- Convert messages to other formats such as MSG, EML, HTML and MHTL.
- Read message properties such as sender, receiver, message sent date, subject and so on.
- Add or extract attachments to & from email messages.
- Process iCalendar, MAPI & VCard file types.
- Supports AI functionalities:
  - Business card recognition.
  - Parse and handle personal names.

## New Features & Enhancements in Version 20.7

- New models for representing `MAPI` message files have been added to Aspose Email Cloud.
- All these models can be converted to corresponding `DTO` objects.
- The methods to save these models to `MSG` files are also provided.
- A new `Recurrence` property has been added, so there is a better way to set recurrence patterns.

For the detailed notes, please visit [Aspose.Email Cloud 20.7 Release Notes](https://docs.aspose.cloud/display/emailcloud/Aspose.Email+Cloud+20.7+Release+Notes).

## Read & Write

**Email:** MSG, EML
**Web:** HTML, MHTML

## Getting Started with Aspose.Email Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install @asposecloud/aspose-email-cloud --save` from the command line to install Aspose.Email Cloud SDK for Node.js via NPM. The complete source code is available at [GitHub Repository](https://github.com/aspose-email-cloud/aspose-email-cloud-node).

### Initialize EmailApi

You should create an `EmailApi` object to use the API.

```js
var appKey = "Your App Key";
var appSid = "Your App SID";
var api = new EmailApi(appSid, appKey);
```

## Get Email Attachment by Name using Node.js

```js
public async getEmailAttachment(requestObj: requestModels.GetEmailAttachmentRequest): Promise<{response: request.RequestResponse, body: Buffer}> 
{
	const localVarPath = this.configuration.getApiBaseUrl() + "/email/{fileName}/attachments/{attachment}"
		.replace("{" + "attachment" + "}", String(requestObj.attachment))
		.replace("{" + "fileName" + "}", String(requestObj.fileName));
	const queryParameters: any = {};
	const headerParams: any = {};
	const formParams: any = {};

	// verify required parameter 'requestObj.attachment' is not null or undefined
	if (requestObj.attachment === null || requestObj.attachment === undefined) {
		throw new Error('Required parameter "requestObj.attachment" was null or undefined when calling getEmailAttachment.');
	}

	// verify required parameter 'requestObj.fileName' is not null or undefined
	if (requestObj.fileName === null || requestObj.fileName === undefined) {
		throw new Error('Required parameter "requestObj.fileName" was null or undefined when calling getEmailAttachment.');
	}

	if (requestObj.storage !== undefined) {
		queryParameters.storage = ObjectSerializer.serialize(requestObj.storage, "string");
	}

	if (requestObj.folder !== undefined) {
		queryParameters.folder = ObjectSerializer.serialize(requestObj.folder, "string");
	}

	// tslint:disable-next-line:prefer-const
	let useFormData = false;

	const requestOptions: request.Options = {
		method: "GET",
		qs: queryParameters,
		headers: headerParams,
		uri: localVarPath,
		encoding: null,
	};

	if (Object.keys(formParams).length) {
		if (useFormData) {
			(requestOptions as any).formData = formParams;
		} else {
			requestOptions.form = formParams;
		}
	}

	const response = await invokeApiMethod(requestOptions, this.configuration);
	const result =  ObjectSerializer.deserialize(response.body, "Buffer");
	return Promise.resolve({body: result, response});
}
```

## Getting Started with Business Card API

The following are a few common use-cases. Read more about the [Business Card API](https://docs.aspose.cloud/display/emailcloud/Working+with+Contact+Cards).

### Parse Business Card Images to VCard File with Node.js

```js
var folder = 'some/folder/on/storage';
var storage = 'First Storage'; //Your storage name
var imageData = fs.readFileSync('some/business/card/image/file/on/disk');
var storageFileName = 'someFileName.png'; //Supports different image formats: PNG, JPEG, BMP, TIFF, GIF, etc.
// Upload business card image to storage
await api.uploadFile(new requests.UploadFileRequest(folder + '/' + storageFileName, imageData, storage));
var outFolder = 'some/other/folder/on/storage'; //Business card recognition results will be saved here
await api.createFolder(new requests.CreateFolderRequest(outFolder, storage));
// Call business card recognition action
var result = await api.aiBcrParseStorage(
    new requests.AiBcrParseStorageRequest(new models.AiBcrParseStorageRq(
        null,
        [new models.AiBcrImageStorageFile( //We can process multiple images in one request
            true, //the image contains only one business card (you can upload image with multiple cards on it)
            new models.StorageFileLocation(storage, folder, storageFileName))],
        new models.StorageFolderLocation(storage, outFolder))));
// Get file name from recognition result
var contactFile = result.body.value[0]; //result.body.value can contain multiple files, if we sent multicard images or multiple images
// You can download the VCard file, which produced by the recognition method ...
var contactBinary = await api.downloadFile(new requests.DownloadFileRequest(
    contactFile.folderPath + '/' + contactFile.fileName, storage));
// ... and print it to console
console.log(contactBinary.body.toString());
// Also, you can get VCard object properties’ list using Contact API
var contactProperties = await api.getContactProperties(new requests.GetContactPropertiesRequest(
    'vcard', contactFile.fileName, contactFile.folderPath, contactFile.storage));
//All VCard’s properties are available as a list. Complex properties are represented as hierarchical structures.
//Let's print all primitive properties’ values:
contactProperties.body.internalProperties
    .filter(property => property.type == 'PrimitiveObject')
    .map(property => property as models.PrimitiveObject)
    .forEach(property =>
        console.log('Property name:' + property.name + ' value:' + property.value));
```

### Parse VCard Images without using Storage

```js
//Read image from file and convert it to Base64 string
var imageData = fs.readFileSync('some/business/card/image/file/on/disk').toString('base64');
var result = await api.aiBcrParse(new requests.AiBcrParseRequest(
    new models.AiBcrBase64Rq(undefined, [new models.AiBcrBase64Image(true, imageData)])));
//Result contains all recognized VCard objects (only the one in our case)
var contactProperties = result.body.value[0];
//VCard object is available as a list of properties, without any external calls:
contactProperties.internalProperties
    .filter(property => property.type == 'PrimitiveObject')
    .map(property => property as models.PrimitiveObject)
    .forEach(property =>
        console.log('Property name:' + property.name + ' value:' + property.value));
```

## Getting Started with the Name API

The following are a few common use-cases. Read more about the [Name API](https://docs.aspose.cloud/display/emailcloud/Working+with+Name+API).

### Detect Person's Gender from Name

```js
var result = await api.aiNameGenderize(new requests.AiNameGenderizeRequest('John Cane'));
//the result contains a list of hypothesis about a person's gender.
//all hypothesis include score, so you can use the most scored version, which will be the first in a list:
console.log(result.body.value[0].gender); //prints 'Male'
```

### Expand Person's Name into a List of Alternatives

```js

var result = await api.aiNameExpand(new requests.AiNameExpandRequest(
    'Smith Bobby'));
var names = result.body.names
    .map(weighted => weighted.name)
    .forEach(name => console.log(name)); //prints 'Mr. Smith', 'B. Smith', etc.
```

[Product Page](https://products.aspose.cloud/email/nodejs) | [Documentation](https://docs.aspose.cloud/display/emailcloud/Home) | [Demo](https://products.aspose.app/email/family) | [API Reference](https://apireference.aspose.cloud/email/) | [Examples](https://github.com/aspose-email-cloud/aspose-email-cloud-node) | [Blog](https://blog.aspose.cloud/category/email/) | [Free Support](https://forum.aspose.cloud/c/email) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
