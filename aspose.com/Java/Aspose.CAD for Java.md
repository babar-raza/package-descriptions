# Aspose.CAD for Java

[Aspose.CAD for Java](https://products.aspose.com/cad/java) allows developers to convert AutoCAD DWG and DXF files to PDF and Raster images. It is a native API and does not require AutoCAD or any other software to be installed. You can also convert the selected layers and layouts from the AutoCAD files. The conversion to PDF and Raster images is of very high quality.

This repository contains [Examples](Examples), Plugins and Showcases for [Aspose.CAD for Java](https://products.aspose.com/cad/java) to help you learn and write your own applications.

<p align="center">

  <a title="Download complete Aspose.CAD for Java source code" href="https://github.com/aspose-cad/Aspose.CAD-for-Java/archive/master.zip">
	<img src="http://i.imgur.com/hwNhrGZ.png" />
  </a>
</p>

# CAD File Conversion API for Java

[Aspose.CAD for Java](https://products.aspose.com/cad/java) is a standalone class library to enhance your Java applications to process & render CAD drawings without requiring AutoCAD or any other rendering workflow. The CAD Class Library allows high quality [conversion of DWG, DWF, DWT and DXF](https://docs.aspose.com/display/cadjava/Supported+File+Formats) files, layouts and layers to PDF & raster image formats.

## CAD File Processing Features

- [Adjust CAD drawing size](https://docs.aspose.com/display/cadjava/Adjusting+CAD+Drawing+Size).
- Convert CAD drawings to other file formats.
- [Export 3D AutoCAD Images to PDF](https://docs.aspose.com/display/cadjava/Exporting+CAD#ExportingCAD-Export3DAutoCADImagestoPDF).
- Exporting CAD Layouts to PDF
- Set timeout on save to avoid spending lot of time or consuming a lot of memory.

## Read CAD Formats

**AutoCAD:** DWG, DWT, DWF, DWXF, IFC, PLT
**MicroStation:** DGN
**The Advanced Visualizer:** OBJ
**Other:** STL, IGES, CFF2

## Save CAD As

**Fixed Layout:** PDF
**Raster Images:** PNG, BMP, TIFF, JPEG, GIF

## Read & Write

**CAD:** DXF
(Write features is partially supported.)

## Supported Platforms

- Desktop Applications in MS Windows and Servers
- Enterprise Web Applications
- Linux (Ubuntu, openSUSE, CentOS and others)
- Unix

## Supported Java Versions

- `J2SE 6.0 (1.6)`
- `J2SE 7.0 (1.7)`
- `J2SE 8.0 (1.8)`

# Get Started with Aspose.CAD for Java

Aspose hosts all Java APIs at the [Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-cad). You can easily use Aspose.BarCode for Java API directly in your Maven projects with simple configurations.

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

Then define Aspose.CAD for Java API dependency in your `pom.xml` as follows:

```xml
<dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-cad</artifactId>
        <version>20.6</version>
    </dependency>
</dependencies>
```

Congratulations! You have successfully defined the Aspose.CAD for Java Maven dependency in your Maven project.

## Converting .DXF CAD Drawing to .PNG Format using Java

```java
String srcFile = dataDir + "conic_pyramid.dxf";

Image image = Image.load(srcFile); 

// Create an instance of CadRasterizationOptions
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

// Set page width & height
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);

// Create an instance of PngOptions for the resultant image
ImageOptionsBase options = new PngOptions();

//Set rasterization options
options.setVectorRasterizationOptions(rasterizationOptions);

// Save resultant image
image.save(dataDir + "conic_pyramid_raster_image_out_.png", options);
```

[Product Page](https://products.aspose.com/cad/java) | [Docs](https://docs.aspose.com/display/cadjava/Home) | [Demos](https://products.aspose.app/cad/family) | [API Reference](https://apireference.aspose.com/java/cad/) | [Examples](https://github.com/aspose-cad/Aspose.CAD-for-Java) | [Blog](https://blog.aspose.com/category/cad/) | [Free Support](https://forum.aspose.com/c/cad) |  [Temporary License](https://purchase.aspose.com/temporary-license)
