# C++ Library for Excel File Formats
[Aspose.Cells for C++]() is a native C++ library to create, manipulate, process and convert Microsoft Excel® files without needing Microsoft Office® or Automation. The Excel C++ API supports Excel 97-2003 (XLS), Excel 2007-2013/2016 (XLSX, XLSM, XLSB), OpenOffice XML and other formats such as CSV, TSV and more. 

It allows the developers to manage worksheets, rows, columns & cells, create spreadsheet contents and styles from scratch, import data onto the worksheets from different data sources, add common, complex mathematical, financial and text formulas to calculate results on runtime, create & manipulate charts & Pivot Tables, manage pictures, comments, drawing objects from their own C++ applications.

## Excel File Processing Features
- Spreadsheet generation & manipulation via API.
- High quality file format conversion & rendering.
- Combine, modify, protect or parse Excel sheets.
- Apply worksheet, row, column & cell formatting.
- Configure and apply page setup for the worksheets.
- Create, customize & refresh [Excel charts](https://docs.aspose.com/display/cellscpp/Creating+and+Customizing+Charts), [Pivot Tables](https://docs.aspose.com/display/cellscpp/Create+Pivot+Table), & Named Ranges.
- Convert spreadsheet charts to images & PDF.
- Convert Excel files to various other formats.
- [Formula Calculation Engine](https://docs.aspose.com/display/cellscpp/Formulas) that supports all basic and advanced Excel functions.

## Read & Write Formats
**Microsoft Excel:** XLS, XLSX, XLSB
**Text:** CSV, TSV
**OpenDocument:** ODS
**Others:** HTML, MHTML 

## Save Spreadsheet Documents As
**Microsoft Excel:** XLSM, XLTX, XLTM, XLAM
**Fixed Layout:** PDF, XPS
**Images:** JPEG, PNG, BMP, TIFF, GIF, EMF, SVG

## Getting Started with Aspose.Cells for C++
Are you ready to give Aspose.Cells for C++ a try? Simply execute `Install-Package Aspose.Cells.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Cells for C++ and want to upgrade the version, please execute `Update-Package Aspose.Cells.Cpp` to get the latest version.


### Convert XLS to XLSX, XLSB & CSV using C++
Try executing below snippet to see how API works in your environment or check the [GitHub Repository](https://github.com/aspose-cells/Aspose.Cells-for-C) for other common usage scenarios. 

```c++
// load the file to be converted
intrusive_ptr<IWorkbook> book = Factory::CreateIWorkbook(dir->StringAppend(new String("template.xls")));
// save in different formats
book->Save(dir->StringAppend(new String("output.xlsx")), SaveFormat_Xlsx);
book->Save(dir->StringAppend(new String("output.xlsb")), SaveFormat_Xlsb);
book->Save(dir->StringAppend(new String("output.csv")), SaveFormat_CSV);
```

### Create a Custom Excel Chart with C++

```c++
// create a new workbook
intrusive_ptr<IWorkbook> workbook = Factory::CreateIWorkbook();

// get first worksheet which is created by default
intrusive_ptr<IWorksheet> worksheet = workbook->GetIWorksheets()->GetObjectByIndex(0);

// add sample data
worksheet->GetICells()->GetObjectByIndex(new String("A1"))->PutValue(50);
worksheet->GetICells()->GetObjectByIndex(new String("A2"))->PutValue(100);
worksheet->GetICells()->GetObjectByIndex(new String("A3"))->PutValue(150);
worksheet->GetICells()->GetObjectByIndex(new String("A4"))->PutValue(110);
worksheet->GetICells()->GetObjectByIndex(new String("B1"))->PutValue(260);
worksheet->GetICells()->GetObjectByIndex(new String("B2"))->PutValue(12);
worksheet->GetICells()->GetObjectByIndex(new String("B3"))->PutValue(50);
worksheet->GetICells()->GetObjectByIndex(new String("B4"))->PutValue(100);

// add a chart to the worksheet
int chartIndex = worksheet->GetICharts()->Add(Aspose::Cells::Charts::ChartType::ChartType_Column, 5, 0, 20, 8);

// access the instance of the newly added chart
intrusive_ptr<Aspose::Cells::Charts::IChart> chart = worksheet->GetICharts()->GetObjectByIndex(chartIndex);

// add SeriesCollection (chart data source) to the chart ranging from A1 to B4
chart->GetNISeries()->Add(new String("A1:B4"), true);

// set the chart type of 2nd NSeries to display as line chart
chart->GetNISeries()->GetObjectByIndex(1)->SetType(Aspose::Cells::Charts::ChartType::ChartType_Line);

// save the Excel file
workbook->Save(new String("output.xlsx")));
```

[Product Page](https://products.aspose.com/cells/cpp) | [Documentation](https://docs.aspose.com/display/cellscpp/Home) | [API Reference](https://apireference.aspose.com/cpp/cells) | [Code Examples](https://github.com/aspose-cells/Aspose.Cells-for-C) | [Blog](https://blog.aspose.com/category/cells/) | [Free Support](https://forum.aspose.com/c/cells) |  [Temporary License](https://purchase.aspose.com/temporary-license)