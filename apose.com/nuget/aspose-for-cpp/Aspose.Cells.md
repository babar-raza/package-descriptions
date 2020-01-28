Aspose.Cells for C++ is a native C++ library to create, manipulate, process and convert Microsoft Excel® files without needing Microsoft Office® or Automation.

Some of the basic tasks developers can perform after integrating Aspose.Cells for C++ are management of worksheets, rows, columns & cells, creating spreadsheet contents and styles from scratch, importing data onto the worksheets from different data sources, adding common and complex mathematical, financial and text formulas, manipulation of charts, pictures, comments, drawing objects and much more.

## Excel File Processing Features
- Spreadsheet generation & manipulation via API.
- High quality file format conversion & rendering.
- Combine, modify, protect or parse Excel sheets.
- Apply worksheet, row, column & cell formatting.
- Configure and apply page setup for the worksheets.
- Create, customize & refresh charts, Pivot Tables, conditional formatting rules & spark-lines.
- Convert spreadsheet charts to images & PDF.
- Convert Excel files to various other formats.
- Formula calculation engine that supports all basic and advanced Excel functions.

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

[Product Page](https://products.aspose.com/cells/cpp) | [Documentation](https://docs.aspose.com/display/cellscpp/Home) | [API Reference](https://apireference.aspose.com/cpp/cells) | [Code Examples](https://github.com/aspose-cells/Aspose.Cells-for-C) | [Blog](https://blog.aspose.com/category/cells/) | [Free Support](https://forum.aspose.com/c/cells) |  [Temporary License](https://purchase.aspose.com/temporary-license)