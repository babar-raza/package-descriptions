This cloud REST API enhances your Node.js cloud apps to [compare two documents](https://products.groupdocs.cloud/comparison/nodejs), fetch, accept or reject the changes. Supports 90+ file formats.

## Cloud Document Comparison Features

- Compare two documents and fetch changes.
- [Fetch document changes](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-document-changes/) based on change category, such as, numeric only.
- Accept or reject the changes that come up after document comparison.
- [Get the image stream of resultant document](https://wiki.groupdocs.cloud/comparisoncloud/developer-guide/changes-resource/get-stream-of-images-of-result-document-changes/) via JsonRequest object.
- Save the resultant document to streams as set of images.
- Get the resultant document path.
- Add summary page to resultant document after comparison.
- Show deleted components in the resultant document.
- Detect style changes.
- Get or set password of the resultant document.

## Supported Document Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX, ODT, OTT, RTF, TXT
**Microsoft Excel:** XLS, XLSB, XLSM, XLSX, XLTM, XLTX, ODS, OTS, CSV, TSV
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POTM, POTX, ODP, OTP
**Microsoft Visio:** VDW, VDX, VSD, VSDML, VSDX, VSS, VSSM, VSSX, VST, VSTM, VSTX, VSX, VTX
**Microsoft Project:** MPP, MPT
**Microsoft OneNote:** ONE
**Email:** EML, EMLX, MSG, OST, PST
**Adobe Photoshop:** PSD
**AutoCAD:** DGN, DWF, DWG, DXF, IFC, STL
**eBook:** EPUB, MOBI
**Image:** BMP, CGM, DCM, DJVU, DNG, EPS, GIF, ICO, JP2, JPF, JPX, J2K, J2C, JPM, JPG, JPEG, ODG, PNG, SVG, TIF, TIFF, WEBP
**Markup:** HTML, MHT, MHTML, XML
**Portable:** PDF, TEX, XPS
**Metafile:** EMF, WMF
**Other:** PCL, PS

## Platform Independence

GroupDocs.Comparison Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with GroupDocs.Comparison Cloud SDK for Node.js. Just create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-node). You can either directly use it in your project via source code or get nmpjs distribution (recommended).

To install GroupDocs.Annotation for Cloud via NPM, please execute from the command line, `npm install groupdocs-comparison-cloud`.

## Compare Documents using Node.js

```js
public async comparisons(requestObj: model.ComparisonsRequest): Promise<model.Link> {
    if (requestObj === null || requestObj === undefined) {
        throw new Error('Required parameter "requestObj" was null or undefined when calling comparisons.');
    }

    const localVarPath = this.configuration.getServerUrl() + "/comparison/comparisons";
    const queryParameters: any = {};

    // verify required parameter 'requestObj.comparisonOptions' is not null or undefined
    if (requestObj.comparisonOptions === null || requestObj.comparisonOptions === undefined) {
        throw new Error('Required parameter "requestObj.comparisonOptions" was null or undefined when calling comparisons.');
    }

    const requestOptions: request.Options = {
        method: "POST",
        qs: queryParameters,
        uri: localVarPath,
        json: true,
        body: Serializer.serialize(requestObj.comparisonOptions, requestObj.comparisonOptions.constructor.name === "Object" ? "Options" : requestObj.comparisonOptions.constructor.name),
    };

    const response = await invokeApiMethod(requestOptions, this.configuration);
    const result =  Serializer.deserialize(response.body, "Link");
    return Promise.resolve(result);
}
```

[Product Page](https://products.groupdocs.cloud/comparison/nodejs) | [Documentation](https://wiki.groupdocs.cloud/comparisoncloud/) | [API Reference](https://apireference.groupdocs.cloud/comparison/) | [Code Samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-node) | [Blog](https://blog.groupdocs.cloud/category/comparison/) | [Free Support](https://forum.groupdocs.cloud/c/comparison) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)
