This cloud SDK enhances your Node.js cloud-based apps to work with, manage & convert email format files in the cloud without a 3rd party tool.

Aspose.Email Cloud SDK for Node.js is a wrapper around Aspose.Email REST API and is available for use under an MIT license. It supports common email file formats, such as, MSG and EML.

## Email Processing Features

- Supports OAuth feature.
- Send or append MIME or simple email messages.
- Fetch list of email messages.
- Mark specific email messages with a red flag.
- Set or download email attachments.
- Supports email file format conversion among popular email formats.
- Get email properties.
- Create, list or delete email folders.

## Read & Write Email Formats

**Microsoft Outlook:** MSG
**Email:** EML

## Platform Independence

Aspose.Email Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.Email Cloud SDK for Node.js. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/aspose-email-cloud/aspose-email-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install Aspose.Email for Cloud via NPM, please execute from the command line, `npm install aspose-email-cloud-node --save`.

## Get Email Attachment by Name using Node.js

```js
public async getEmailAttachment(requestObj: requestModels.GetEmailAttachmentRequest): Promise<{response: request.RequestResponse, body: Buffer}> {
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

[Product Page](https://products.aspose.cloud/email/nodejs) | [Documentation](https://docs.aspose.cloud/display/emailcloud/Home) | [API Reference](https://apireference.aspose.cloud/email/) | [Code Samples](https://github.com/aspose-email-cloud/aspose-email-cloud-node) | [Blog](https://blog.aspose.cloud/category/email/) | [Free Support](https://forum.aspose.cloud/c/email) | [Free Trial](https://dashboard.aspose.cloud/#/apps)