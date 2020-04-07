Python Cloud SDK wraps Aspose.Cells REST API so you could seamlessly integrate Microsoft Excel® spreadsheet generation, manipulation, conversion & inspection features into your own Python applications.

[Aspose.Cells Cloud SDK for Python](https://products.aspose.cloud/cells/python) offers Excel® file creation, manipulation, conversion, & rendering. Developers can format worksheets, rows, columns or cells to the most granular level, create & manipulate chart & pivot tables, render worksheets, charts and specific data ranges to PDF & images, add & calculate Excel's built-in and custom formulas and much more. Feel free to explore the [Developer's Guide](https://docs.aspose.cloud/display/cellscloud/Developer+Guide) for all usage scenarios. 

## Manipulate Excel Files in the Cloud with Python

- Create Excel files via API.
- Create & refresh Pivot Tables & charts.
- Create & manipulate spark-lines & conditional formatting.
- Convert charts, worksheets or data ranges to images or PDF.
- Manage comments & hyperlinks.
- Set complex formulas & calculate results via API.
- Set protection on workbook, worksheet, cell, column or row.
- Create & manipulate named ranges.
- Populate worksheets through Smart Markers.
- Convert worksheets to PDF, XPS & SVG formats.
- Inter-convert files to popular Excel formats.

## New Features in Version 20.3

- Support to export area or page of sheet to `JPEG`.
- Support to add background for workbook.

For the detailed notes, please visit [Aspose.Cells Cloud 20.3 Release Notes](https://docs.aspose.cloud/display/cellscloud/Aspose.Cells+Cloud+20.3+Release+Notes).

## Read & Write Spreadsheet Formats

**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**OpenOffice:** ODS
**SpreadsheetML:** XML
**Text:** CSV, TSV, TXT (TabDelimited)
**Web:** HTML, MHTML

## Save Spreadsheets As

DIF, PDF, XPS, TIFF, SVG, MD (Markdown)

## Read Spreadsheet Formats

SXC, FODS

## Getting Started with Aspose.Cells Cloud SDK for Python

Firstly, create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) to get your application information and free quota to use the API. Now execute `pip install asposecellscloud` from the command line to get the get the SDK from PIP. The complete source code is available at [GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python).

## Create Spreadsheet from a Template in the Cloud via Python

```python
#Instantiate Aspose Storage API SDK
storage_apiClient = asposestoragecloud.ApiClient.ApiClient(apiKey, appSid, True)
storageApi = StorageApi(storage_apiClient)
#Instantiate Aspose Cells API SDK
api_client = asposecellscloud.ApiClient.ApiClient(apiKey, appSid, True)
cellsApi = CellsApi(api_client);

#set input file name
filename = ''.join(random.choice(string.ascii_uppercase + string.digits) for _ in range(8)) + ".xls"

#The template file, if the data not provided default workbook is created.
templatefile = "Sample_SmartMarker.xlsx"

#Smart marker data file, if the data not provided the request content is checked for the data.
datafile = "Sample_SmartMarker_Data.xml"

#upload SmartMarker template file to aspose cloud storage
storageApi.PutCreate(Path=templatefile, file=data_folder + templatefile)

#upload SmartMarker template data file to aspose cloud storage
storageApi.PutCreate(Path=datafile, file=data_folder + datafile)

try:
    #invoke Aspose.Cells Cloud SDK API to create a workbook from a SmartMarker template
    response = cellsApi.PutWorkbookCreate(name=filename, file=None, templateFile=templatefile, dataFile=datafile)

    if response.Status == "OK":

        outputfilename = response.Workbook.FileName
        print "FileName: " + outputfilename
        #download Workbook from storage server
        response = storageApi.GetDownload(Path=outputfilename)
        outfilename = "c:/temp/" +  outputfilename
        with open(outfilename, 'wb') as f:
                    for chunk in response.InputStream:
                        f.write(chunk)

except ApiException as ex:
            print "ApiException:"
            print "Code:" + str(ex.code)
            print "Message:" + ex.message
```

## Convert Excel to PDF via Python 

```python
#Instantiate Aspose Storage API SDK
storage_apiClient = asposestoragecloud.ApiClient.ApiClient(apiKey, appSid, True)
storageApi = StorageApi(storage_apiClient)
#Instantiate Aspose Cells API SDK
api_client = asposecellscloud.ApiClient.ApiClient(apiKey, appSid, True)
cellsApi = CellsApi(api_client);

#set input file name
name = "Sample_Test_Book"
filename = name + ".xls"
format = "pdf"
outputfilename = name + "." + format

body = SaveOptions.SaveOptions()

#upload file to aspose cloud storage
storageApi.PutCreate(Path=filename, file=data_folder + filename)

try:
    #invoke Aspose.Cells Cloud SDK API to convert workbook to different file formats using cloud storage
    response = cellsApi.PostDocumentSaveAs(name=filename, body=body, newfilename=outputfilename)

    if response.Status == "OK":

        destfilename = response.SaveResult.DestDocument.Href
        print "FileName: " + destfilename
        #download Workbook from storage server
        response = storageApi.GetDownload(Path=destfilename)
        outfilename = "c:/temp/" +  destfilename
        with open(outfilename, 'wb') as f:
                    for chunk in response.InputStream:
                        f.write(chunk)

except ApiException as ex:
            print "ApiException:"
            print "Code:" + str(ex.code)
            print "Message:" + ex.message
```

[Product Page](https://products.aspose.cloud/cells/python) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [Live Demo](https://products.aspose.app/cells/family) | [API Reference](https://apireference.aspose.cloud/cells/) | [Code Samples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)
