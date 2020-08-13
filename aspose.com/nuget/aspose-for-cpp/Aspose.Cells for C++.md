# C++ Library for Excel File Formats

[Aspose.Cells for C++](https://products.aspose.com/cells/cpp) is a native C++ library to create, manipulate, process and convert Microsoft Excel® files without needing Microsoft Office® or Automation. The Excel C++ API supports Excel 97-2003 (XLS), Excel 2007-2013/2016 (XLSX, XLSM, XLSB), OpenOffice XML and other formats such as CSV, TSV and more.

It allows the developers to work with spreadsheet rows, columns, data, formulas, pivot tables, worksheets, tables, charts, and drawing objects from their own C++ applications.

## Excel File Processing Features

- Open a spreadsheet file without Microsoft Excel.
- [Open an Excel file](https://docs.aspose.com/cells/cpp/opening-files/) via a path on local computer or using a stream.
- [Convert worksheet](https://docs.aspose.com/cells/cpp/converting-worksheet-to-different-image-formats/) to different image formats.
- [Apply conditional formatting](https://docs.aspose.com/cells/cpp/apply-conditional-formatting-in-worksheet/) as per your choice.
- [Manipulate pivot tables](https://docs.aspose.com/cells/cpp/manipulate-pivot-table/) in your spreadsheets.
- [Convert table to range](https://docs.aspose.com/cells/cpp/tables-and-ranges/) without losing formatting.
- Fetch a cell's name by providing the row and column index, similarly, [fetch row and column index of cell](https://docs.aspose.com/cells/cpp/names-and-indices/) from its name.
- Create [Pyramid chart, Line chart, Bubble chart](https://docs.aspose.com/cells/cpp/creating-and-customizing-charts/), or a custom chart.
- [Render](https://docs.aspose.com/cells/cpp/chart-rendering/) supported chart types to images or PDF.
- [Insert an OLE object into the worksheet](https://docs.aspose.com/cells/cpp/inserting-ole-objects-into-the-worksheet/).
- Access all the OLE objects contained in the worksheet for [extraction](https://docs.aspose.com/cells/cpp/extracting-ole-objects-from-worksheet/).

## New Features in Version 20.7

This release offers some enhancements. For the detailed notes, please visit [Aspose.Cells for C++ 20.7 Release Notes Windows](https://docs.aspose.com/cells/cpp/aspose-cells-for-cpp-20-7-release-notes-windows/).

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

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/cells/cpp) | [Docs](https://docs.aspose.com/cells/cpp/) | [Demos](https://products.aspose.app/cells/family) | [API Reference](https://apireference.aspose.com/cells/cpp) | [Examples](https://github.com/aspose-cells/Aspose.Cells-for-C) | [Blog](https://blog.aspose.com/category/cells/) | [Free Support](https://forum.aspose.com/c/cells) |  [Temporary License](https://purchase.aspose.com/temporary-license)
