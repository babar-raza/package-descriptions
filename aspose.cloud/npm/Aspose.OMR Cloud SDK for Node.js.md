Node.js Cloud SDK wraps Aspose.OMR REST API so you could seamlessly integrate OMR (Optical Mark Recognition) features to your own Node.js applications.

# Optical Mark Recognition in the Cloud 

[Aspose.OMR Cloud SDK for Node.js](https://products.aspose.cloud/omr/nodejs) allows to define and generate OMR templates with support for numerous types of elements, such as, text, grid, multi-column answer sheets, and images. Using Aspose.OMR Cloud SDK for Node.js, developers can also define answer grading rules to perform automatic grading of OMR mark sheets, surveys, questionnaires & quizzes while extracting the OMR data to CSV format.

## OMR Features

- Ability to perform OMR on rotated & perspective (within 25 deg) photos.
- Extract & recognize human-marked data from scanned tests, exams, surveys etc.
- Export OMR results to CSV file format.
- Use textual markup to generate OMR templates, generate surveys and test sheets.
- Specify number of OMR based questions & answers in the template.
- Provide JSON rules to perform OMR answer grading.
- Clip an area of interest from an image, save it as JPEG & perform OMR on it.

## Enhancements in Version 20.2

- Minor metadata updates.

## Save OMR Results As

CSV

## Read Formats to Perform OMR

JPEG, PNG, BMP, TIFF, PDF

## Getting Started with Aspose.OMR Cloud SDK for Node.js

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `npm install aspose-omr-cloud-node --save` from the command line to install Aspose.OMR Cloud SDK for Node.js via NPM. The complete source code is available at [GitHub Repository](https://github.com/aspose-omr-cloud/aspose-omr-cloud-nodejs).

## Use Node.js Code to Recognize Questionnaire Scan

```js
recognizeImage(templateId, imagePath) {
        return this.storage.uploadFile(imagePath, "")
            .then(() => {
                let imageFileName = path.basename(imagePath);
                let param = new api.OMRFunctionParam();
                param.functionParam = templateId;
                return this.omrApi.postRunOmrTask(imageFileName, "RecognizeImage", param);
            });
    }
```

[Product Page](https://products.aspose.cloud/omr/nodejs) | [Documentation](https://docs.aspose.cloud/display/omrcloud/Home) | [Demo](https://products.aspose.app/omr/family) | [API Reference](https://apireference.aspose.cloud/omr/) | [Examples](https://github.com/aspose-omr-cloud/aspose-omr-cloud-nodejs) | [Blog](https://blog.aspose.cloud/category/omr/) | [Free Support](https://forum.aspose.cloud/c/omr) | [Free Trial](https://dashboard.aspose.cloud)
