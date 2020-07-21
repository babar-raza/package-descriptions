## Aspose.Imaging for Java

This package contains Java example code for [Aspose.Imaging for Java](https://products.aspose.com/imaging/java).

<p align="center">
  <a title="Download ZIP" href="https://github.com/asposeimaging/Aspose_Imaging_Java/archive/master.zip">
     <img src="http://i.imgur.com/hwNhrGZ.png" />
  </a>
</p>

# .NET API for Image Processing

It is a [standalone Imaging API](https://products.aspose.com/imaging/java) that enable your Java apps to draw as well as perform basic to advanced level processing of raster & vector images.

Aspose.Imaging for Java offers robust image compression and high processing speed through native byte access and a range of efficient algorithms. It has the ability to manipulate, export, and convert images.

## Imaging API Features

- Create, Open and Save Images.
- Manipulate and convert images from one format to the other supported formats.
- Crop, rotate, resize, and deskew images.
- Ability to export images in multi threaded environment.
- Modify Text In Text layer inside a `PSD` file.
- [Many, many more](https://docs.aspose.com/display/imagingjava/Developer+Guide).

## Read & Write Image Formats

**Raster Formats:** JPEG2000, JPEG, BMP, TIFF, GIF, PNG, APNG
**Metafiles:** EMF, EMZ, WMF, WMZ
**Other:** SVG, SVGZ, DICOM

## Save Images As

**Fixed:** PDF
**Photoshop:** PSD
**Markup:** HTML5 Canvas

## Read Image Formats

**Various:** DjVu, DNG, ODG, CMX, CDR, DIB, OTG, FODG, EPS (raster preview only), WEBP

## Supported Operating Systems

Aspose.Imaging for Java can be virtually run in any OS where Java is installed (since JDK 1.6)

- Windows (since 7)
- Linux
- MacOS
- Any OS where Java is installed.

Aspose.Imaging works for both x86 and x64 versions of the above listed operating systems.

**Note:** In Linux OS, it is recommended to install the package with Microsoft compatible fonts (e.g. `sudo apt-get install ttf-mscorefonts-installer`).

## Get Started with Aspose.Imaging for Java

Aspose hosts all Java APIs at the [Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-imaging). You can easily use Aspose.BarCode for Java API directly in your Maven projects with simple configurations.

First you need to specify Aspose Repository configuration / location in your Maven `pom.xml` as below:

```xml
<repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://repository.aspose.com/repo/</url>
    </repository>
</repositories>
```

Then define Aspose.Imaging for Java API dependency in your `pom.xml` as follows:

```xml
<dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-imaging</artifactId>
        <version>20.6</version>
        <classifier>jdk16</classifier>
   </dependency>
</dependencies>
```

Congratulations! You have successfully defined the Aspose.Imaging for Java Maven dependency in your Maven project.

## Crop EMF Image by Rectangle using Java

```java
MetafileImage metaImage = (MetafileImage) Image.load(dataDir + "Picture1.emf");

// Create an instance of Rectangle class with desired size
Rectangle rectangle = new Rectangle(10, 10, 100, 100);

// Perform the crop operation on object of Rectangle class
metaImage.crop(rectangle);

// Save the result in PNG format
metaImage.save(dataDir + "CropbyRectangle_out.png", new PngOptions());
```

[Product Page](https://products.aspose.com/imaging/java) | [Docs](https://docs.aspose.com/display/imagingjava/Home) | [Demos](https://products.aspose.app/imaging/family) | [API Reference](https://apireference.aspose.com/java/imaging) | [Examples](https://github.com/aspose-imaging/Aspose.Imaging-for-Java) | [Blog](https://blog.aspose.com/category/imaging/) | [Free Support](https://forum.aspose.com/c/imaging) | [Temporary License](https://purchase.aspose.com/temporary-license)