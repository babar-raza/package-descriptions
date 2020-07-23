# PHP Library for Excel File Formats

[Aspose.Cells for PHP via Java](https://products.aspose.com/cells/php-java) is a feature-rich API to create, process, manipulate & convert Excel & OpenOffice spreadsheets using PHP. API offers Excel file generation, conversion, worksheets styling, Pivot Table & chart management & rendering, reliable formula calculation engine and much more - all without any dependency on Office Automation or Microsoft Excel®.

<p align="center">
  <a title="Download ZIP" href="https://github.com/aspose-cells/Aspose.Cells-for-PHP-via-Java/archive/master.zip">
    <img src="http://i.imgur.com/hwNhrGZ.png" alt="Download Aspose.Cells for PHP via Java Examples, Plugins and Showcases" />
  </a>
</p>

## PHP Excel Library Features

### File Formats and Conversions

- High quality conversions from Excel to other supported formats.
- Convert any Spreadsheet to PDF with high fidelity.
- Load and save documents in the tab delimited file format.
- Easily extract worksheet text by saving in plain text format.
- many more.

### Rendering

- Render Excel worksheet pages to raster images & spreadsheet pages to vector images.
- Specify image resolution, quality, compression and other options.
- many more.

### Spreadsheet Content Features

- Copy an existing worksheet along with included images, charts & other objects.
- Implement data sorting, data validations and smart markers.
- Preserve or remove addin, VBA, macros.
- Add, preserve or extract OLE objects from the spreadsheets.
- Apply file encryption.
- many more.

### Spreadsheet Formatting Features

- Apply formatting (fonts, colors, effects, border etc.) to chracters in the cells.
- Apply format settings on a worksheet, row, column as well as a range of cells.
- many more.

### Page Setup Features

- Configure page orientation, scaling as well as paper size.
- Specify page margins and page centering.
- many more.

## Read & Write Excel Files

**Microsoft Excel:** XLS, XLSX, XLSB, XLTX, XLTM, XLSM, XML\
**OpenOffice:** ODS\
**Text:** CSV, Tab-Delimited, TXT\
**Web:** HTML, MHTML

## Save Excel Files As

**Fixed Layout:** PDF, XPS\
**Images:** JPEG, PNG, BMP, SVG, TIFF, GIF, EMF

## Get Started with Aspose.Cells for PHP via Java

Aspose.Cells for PHP via Java consists of two individual parts, the script wrapper (aspose.cells.php) and Aspose.Cells for Java. These components communicate via PHP/Java Bridge whereas both require separate environments & processes for execution.

### Prerequisites

1. JDK
2. PHP/Java Bridge
3. Web Server like Tomcat
4. PHP

## Installation

1. Install Tomcat on any location such as `\java\apache-tomcat-9.0.24`.
2. Copy JavaBridge.war to `webapps` folder of Tomcat such as `\java\apache-tomcat-9.0.24\webapps`.
3. Copy *aspose-cells-xx.x.jar* and *bcprov-jdk15on-xxx.jar* to `lib` folder such as `\java\apache-tomcat-9.0.24\lib`.
4. Run `\bin\startup.bat`, *JavaBridge.war* will be deployed to `\java\apache-tomcat-9.0.24\webapps\JavaBridge`.
5. Test [http://localhost:8080/JavaBridge/test.php](http://localhost:8080/JavaBridge/test.php) to ensure that PHP works fine.
6. Copy *aspose.cells.php* and *example.php* to `\java\apache-tomcat-9.0.24\webapps\JavaBridge`.
7. Open [http://localhost:8080/JavaBridge/example.php](http://localhost:8080/JavaBridge/example.php) or create your own PHP file as follows.

You will find the Jar and PHP library in the `vendor/aspose/cells` folder.

### Sample Usage

```php
<?php
require_once("http://localhost:8080/JavaBridge/java/Java.inc");
require_once("aspose.cells.php");

use aspose\cells;
use aspose\cells\Workbook;
use aspose\cells\CellsHelper;
use aspose\cells\Color;

$workbook = new Workbook();
$workbook->getWorksheets()->get("Sheet1")->getCells()->get("A1")->putValue("testing...");
$workbook->save("result.xlsx");

echo aspose\cells\BorderType::BOTTOM_BORDER;
echo "\n";

echo "CellsHelper version: ".CellsHelper::getVersion();
echo "\n";
?>
```

## Installation on Various Operating Systems

Aspose.Cells for PHP via Java is distributed as a ZIP archive.

To setup environment, install and use Aspose.Cells for PHP via Java, follow the instructions:

### Linux

- Download [PHP](http://www.php.net/downloads.php) source and  install it. Or, use `sudo apt install php-xxx` command to install php binary.
- Install *Oracle JDK (1.7 or 1.8) for Linux*, configure `JAVA_HOME` environment variable.
- Download/Get *Aspose.Cells for PHP via Java* API and extract it. There will be a folder named *aspose.cells*.
- Run `PHP/Java Bridge` in the aforementioned folder with the below command.
`$JAVA_HOME/bin/java -Djava.ext.dirs=lib -jar JavaBridge.jar SERVLET_LOCAL:8080 >/dev/null 2>&1 &`
- Run *example.php* in *aspose.cells* folder to run the example with the below command:
`$ php example.php`

### Windows

- Download [PHP](http://www.php.net/downloads.php) windows binary and add *php.exe* to *PATH*.
- Install *Oracle JDK (1.7 or 1.8) for Windows* and configure `JAVA_HOME` environment variable.
- Download *Aspose.Cells for PHP via Java* API and extract it. There will be a folder named *aspose.cells*.
- Run *PHP/Java Bridge* in the above folder with below command. Select `8080` HTTP listener port when the bridge started and click **OK**.
`> %JAVA_HOME%/bin/java -Djava.ext.dirs=lib -jar JavaBridge.jar`
- Run *example.php* in *aspose.cells* folder to run the example with below command:
`> php example.php`

### Mac

- Install PHP.
- Install *Oracle JDK (1.7 or 1.8) for Mac*, configure `JAVA_HOME` environment variable.
- Download *Aspose.Cells for PHP via Java* API and extract it. There will be a folder named *aspose.cells*.
- Run *PHP/Java Bridge* in the above folder with below command. Select `8080` HTTP listener port when the bridge started and click **OK**.
`$ $JAVA_HOME/bin/java -Djava.ext.dirs=lib -jar JavaBridge.jar`
- Run *example.php* in *aspose.cells* folder to run the example with below command:
`$ php example.php`

## Limitations

- Importing/exporting data from an `Array`, `ArrayList`, `ResultSet` etc. is not supported.
- Printing is not supported.

[Product Page](https://products.aspose.com/cells/php-java) | [Documentation](https://docs.aspose.com/display/cellsphpjava/Aspose.Cells+for+PHP+via+Java+Home) | [API Reference](https://apireference.aspose.com/php/cells) | [Code Examples](https://github.com/aspose-cells/Aspose.Cells-for-PHP-via-Java) | [Blog](https://blog.aspose.com/category/cells/) | [Free Support](https://forum.aspose.com/c/cells) | [Temporary License](https://purchase.aspose.com/temporary-license)
