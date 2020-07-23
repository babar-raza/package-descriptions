# Aspose.Cells for Java

[Aspose.Cells for Java](https://products.aspose.com/cells/java) is an award-winning Excel Spreadsheet Processing API that allows Java developers to embed the ability to read, write and manipulate Excel® spreadsheets (XLS, XLSX, XLSM, XLSB, XLTX, SpreadsheetML, CSV, ODS), HTML, MHTML, PDF, and image file formats into their own Java applications without needing to rely on Microsoft Excel®.

This repository contains [Examples](Examples), [Examples.GridWeb](Examples.GridWeb) and [Plugins](Plugins) for [Aspose.Cells for Java](https://products.aspose.com/cells/java)

<p align="center">
  <a title="Download ZIP" href="https://github.com/aspose-cells/Aspose.Cells-for-Java/archive/master.zip">
    <img src="http://i.imgur.com/hwNhrGZ.png" alt="Download Aspose.Cells for Java Examples, Plugins and Showcases" />
  </a>
</p>

## Java API for Excel File Formats

[Aspose.Cells for Java](https://products.aspose.com/cells/java) is an Excel Spreadsheet Programming API to speed up spreadsheet management and processing tasks. Excel .NET API supports to build cross-platform applications having the ability to generate, modify, convert, render and print spreadsheets. It allows developers to manage worksheets, rows, columns & cells, create spreadsheet contents and styles from scratch, import data onto the worksheets from different data sources, add common and complex mathematical, financial and text formulas, create & manipulate pivot tables, charts, hyperlinks, comments, drawing objects and much more.

## Excel File Processing Features

### Document Features

- Open Plain or Encrypted Excel files (Excel97, Excel2007/2010/2013) from different sources.
- Save Excel files (Excel97- Excel2007/2010/2013) in various supported formats.
- Convert Excel files & spreadsheets to various supported formats.
- Convert to Tagged Image File Format (`TIFF`).
- Read and Write OpenDocument Spreadsheet (`ODS`) format.
- Modify the document properties of Excel files.
- many more.

### Worksheet Features

- Make Worksheet visible or hidden.
- Ability to show or hide worksheet tabs, scroll bars, gridlines & headers.
- Apply worksheet zoom level.
- Keep the selected data visible while scrolling in freeze panes.
- Ability to preview worksheet page breaks.
- Protection support for worksheet content, objects as well as scenarios.
- Perform and apply page setup configuration to worksheets.
- Perform various actions on individual or group of rows and columns.
- many more.

### Data Management Features

- Insert data in specific cells at runtime.
- Fetch data from various data soures and import into worksheets.
- Retrieve data from cells based on their datatype.
- Get data from worksheet cells and export to array.
- Apply conditional formatting.
- Perform numerous formatting actions on data, such as, font setting.
- many more.

### Charting & Graphics Features

- Supports creating various kinds of charts.
- Add custom charts to the worksheet.
- Add pictures to worksheets at the runtime.
- Ability to print worksheets.
- many more.

### Advanced Features

- Use robust Formula Calculation Engine to support formula calculation.
- Manipulate VBA code or Macros.
- Create pivot tables as well as change its source data at runtime.

## Read & Write Spreadsheet Formats

**Microsoft Excel:** XLS, XLSX, XLSB, XLT, XLTX, XLTM, XLSM, XML
**OpenOffice:** ODS
**Text:** CSV, TSV
**Web:** HTML, MHTML
**Numbers:** Apple's iWork office suite Numbers app documents

## Save Excel Files As

**Fixed Layout:** PDF, PDF/A, XPS
**Data Interchange:** DIF
**Images:** JPEG, PNG, BMP, SVG, TIFF, EMF, GIF

## Supported Platforms

- Enterprise Web Application
- Linux
- Unix.

## Get Started with Aspose.Cells for Java

Aspose hosts all Java APIs at the [Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-cells). You can easily use Aspose.Cells for Java API directly in your Maven projects with simple configurations.

First you need to specify Aspose Repository configuration / location in your Maven `pom.xml` as below:

```xml
<repositories>
    <repository>
          <id>AsposeJavaAPI</id>
          <name>Aspose Java API</name>
          <url>http://repository.aspose.com/repo/</url>
    </repository>
</repositories>
```

Then define Aspose.Cells for Java API dependency in your `pom.xml` as follows:

```xml
<dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-cells</artifactId>
        <version>20.7</version>
    </dependency>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-cells</artifactId>
        <version>20.7</version>
        <classifier>javadoc</classifier>
    </dependency>
    <dependency>
        <groupId>org.bouncycastle</groupId>
        <artifactId>bcprov-jdk15on</artifactId>
        <version>1.60</version>
    </dependency>
</dependencies>
```

Congratulations! You have successfully defined the Aspose.Cells for Java Maven dependency in your Maven project.

## Convert Table to Range with Options using Java

```java
// For complete examples and data files, please go to https://github.com/aspose-cells/Aspose.Cells-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ConvertTableToRangeWithOptions.class) + "Tables/";
// Open an existing file that contains a table/list object in it
Workbook workbook = new Workbook(dataDir + "book1.xlsx");

TableToRangeOptions options = new TableToRangeOptions();
options.setLastRow(5);

// Convert the first table/list object (from the first worksheet) to normal range
workbook.getWorksheets().get(0).getListObjects().get(0).convertToRange(options);

// Save the file
workbook.save(dataDir + "ConvertTableToRangeWithOptions_out.xlsx");
```

[Product Page](https://products.aspose.com/cells/java) | [Docs](https://docs.aspose.com/display/cellsjava/Home) | [Demos](https://products.aspose.app/cells/family) | [API Reference](https://apireference.aspose.com/java/cells) | [Examples](https://github.com/aspose-cells/Aspose.Cells-for-Java) | [Blog](https://blog.aspose.com/category/cells/) | [Free Support](https://forum.aspose.com/c/cells) | [Temporary License](https://purchase.aspose.com/temporary-license)
