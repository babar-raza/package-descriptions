This Cloud SDK enhances your Python cloud-based apps to process & manipulate Microsoft Excel spreadsheets in the cloud, without MS Office.

It enables your Python cloud-based programs to process workbooks, worksheets, spreadsheets, columns, rows, and individual cells. You can also work with Microsoft Excel OleObjects, pivot tables, ListObjects, shapes, tasks, hyperlinks and comments from within your your cloud-based applications. Aspose.Cells Cloud SDK for Python also lets you apply auto-filtering or perform conditional formatting on the spreadsheet level. Aspose.Cells Cloud SDK for Python is a wrapper around Aspose.Cells REST API and is available for use under an MIT license.

## Spreadsheet Processing Features

- Built-in email client.
- Supports Artificial Intelligence (AI), such as, Business card recognition.
- Add, update or delete charts, worksheet pictures, shapes, hyperlinks & validations.
- Add or remove cells area for conditional formatting, or OleObjects from Excel worksheets.
- Insert or delete, horizontal or vertical page breaks.
- Add ListObject at a specific place within an Excel file & convert them to a range of cells.
- Delete specific or all ListObjects in a worksheet or summarize its data with pivot table.
- Apply custom criteria to list filters of various types.
- Get, update, show or hide chart legend & titles.
- Manipulate page setup, header & footer.
- Create, update, fetch or delete document properties.
- Fetch the required shape from worksheet.
- Load & Process Excel Spreadsheets via Cloud SDK.
- Cloud SDK to Read & Process Excel Worksheets.
- Leverage the Power of Pivot Tables & Ranges.

## Read & Write Spreadsheet Formats

**Microsoft Excel:** XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
**OpenOffice:** ODS
**SpreadsheetML:** XML
**Text:** CSV, TSV, TXT (TabDelimited)
**Web:** HTML, MHTML

## Save Spreadsheet As

DIF, PDF, XPS, TIFF, SVG, MD (Markdown)

## Read Spreadsheet Formats

SXC, FODS

## Platform Independence

Aspose.Cells Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started

You do not need to install anything to get started with Aspose.Cells Cloud SDK for Python. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

You can use it directly in your project via the source code or get its PyPI Package, `pip install aspose-cells-cloud`. The complete source code is available at the [GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python).

## Process Email through Synchronous/Asynchronous API Calls via Python

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

## Using Python to Add an attachment to Email document  

```python
http_request = request.to_http_info(self.api_client.configuration)
return self.__make_request(http_request, 'POST', 'EmailDocumentResponse')
```

[Product Page](https://products.aspose.cloud/cells/python) | [Documentation](https://docs.aspose.cloud/display/cellscloud/Home) | [API Reference](https://apireference.aspose.cloud/cells/) | [Code Samples](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) | [Blog](https://blog.aspose.cloud/category/cells/) | [Free Support](https://forum.aspose.cloud/c/cells) | [Free Trial](https://dashboard.aspose.cloud/#/apps)