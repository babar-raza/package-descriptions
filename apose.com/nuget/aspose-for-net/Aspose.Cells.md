Aspose.Cells for .NET consists of API and GUI controls to create, process, manipulate & convert Microsoft Excel® spreadsheets without needing Office Automation.

Some of the basic tasks developers can perform after integrating the API are management of worksheets, rows, columns & cells, creating spreadsheet contents and styles from scratch, importing data onto the worksheets from different data sources, adding common and complex mathematical, financial and text formulas, manipulation of charts, pictures, comments, drawing objects and much more.

Aspose.Cells for .NET provides a Grid solution with two GUI based .NET controls. One for the desktop applications and the other for .NET based web applications. You can import/export Excel files, manipulate data & formatting, customize grid design and layout, manage multiple worksheets, create and calculate Excel formulas and numerous other Excel-like operations while using these controls. 

## Excel File Processing Features
- Spreadsheet generation & manipulation via API.
- High quality file format conversion & rendering.
- Print Microsoft Excel files to physical or virtual printers.
- Combine, modify, protect or parse Excel sheets.
- Apply worksheet formatting.
- Configure and apply page setup for the worksheets.
- Create, customize & refresh charts, Pivot Tables, conditional formatting rules & spark-lines.
- Convert spreadsheet charts to images & PDF.
- Convert Excel files to various other formats.
- Formula calculation engine that supports all basic and advanced Excel functions.

## Read & Write Spreadsheet Files
**Microsoft Excel:** XLS, XLSX, XLSB, XLT, XLTX, XLTM, XLSM, XML
**OpenOffice:** ODS
**Text:** CSV, TSV
**Web:** HTML, MHTML
**Numbers:** Apple's iWork office suite Numbers app documents

## Save Excel Files As
**Fixed Layout:** PDF, PDF/A, XPS
**Data Interchange:** DIF
**Images:** JPEG, PNG, BMP, SVG, TIFF, EMF, GIF

## Platform Independence
Aspose.Cells for .NET can be used to build ASP.NET, Web Services, WinForms or other .NET applications for framework 2.0 or later on 32-bit and 64-bit operating systems. It also provides dedicated assemblies for Xamarin.Android (for native Android apps), Xamarin.iOS (for native iOS apps), COM (for pre-.NET technologies), Mono, and Windows Azure.

## Getting Started with Aspose.Cells for .NET
Are you ready to give Aspose.Cells for .NET a try? Simply execute `Install-Package Aspose.Cells` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Cells for .NET and want to upgrade the version, please execute `Update-Package Aspose.Cells` to get the latest version.

### Create a New Excel File via C#
You can execute below code snippet to see how Aspose.Cells API performs in your environment or check the [GitHub Repository](https://github.com/aspose-cells/Aspose.Cells-for-.NET) for other common usage scenarios.

```csharp
// initiate an instance of Workbook
var book = new Aspose.Cells.Workbook();
// access first (default) worksheet
var sheet = book.Worksheets[0];
// access CellsCollection of first worksheet
var cells = sheet.Cells;
// write HelloWorld to cells A1
cells["A1"].Value = "Hello World";
// save spreadsheet to disc
book.Save("output.xlsx", SaveFormat.Xlsx);
```
### Convert Excel Files to PDF, XPS & HTML
Aspose.Cells for .NET is capable of converting spreadsheets to numerous other popular formats including PDF, XPS & HTML formats while maintaining the highest visual fidelity. The conversion process is simple, configurable and reliable.

```csharp
// load file to be converted
var workbook = new Aspose.Cells.Workbook(dir + "template.xlsx");
// save in different formats
workbook.Save(dir + "output.pdf", Aspose.Cells.SaveFormat.Pdf);
workbook.Save(dir + "output.xps", Aspose.Cells.SaveFormat.XPS);
workbook.Save(dir + "output.html", Aspose.Cells.SaveFormat.Html);
```

[Product Page](https://products.aspose.com/cells/net) | [Documentation](https://docs.aspose.com/display/cellsnet/Home) | [API Reference](https://apireference.aspose.com/net/cells) | [Code Examples](https://github.com/aspose-cells/Aspose.Cells-for-.NET) | [Blog](https://blog.aspose.com/category/cells/) | [Free Support](https://forum.aspose.com/c/cells) |  [Temporary License](https://purchase.aspose.com/temporary-license)