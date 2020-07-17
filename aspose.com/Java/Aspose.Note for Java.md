# Aspose.Note for Java

[Aspose.Note for Java](https://products.aspose.com/note/java) is a class library that enables applications to interact with Microsoft Office OneNote programmatically without its installation on the server. It is a pure alternate for MS OneNote Object Model provides much better performance and ease of use to manage OneNote documents. Aspose.Note for Java API delivers the features to read, convert, create and edit/manipulate the content of the Microsoft OneNote file format.

This repository contains [Examples](Examples), [Plugins](Plugins) and projects that will help you to write your own application using [Aspose.Note for Java](https://products.aspose.com/note/java).

<p align="center">
  <a title="Download complete Aspose.Note for Java source code" href="https://github.com/asposenote/Aspose_Note_Java/archive/master.zip">
    <img src="http://i.imgur.com/hwNhrGZ.png" />
  </a>
</p>

## Microsoft OneNote File Processing Features

- Load, Save and Convert ONeNote documents.
- [Generate Root and Sub Level Pages in OneNote](https://docs.aspose.com/display/notejava/Working+with+Pages#WorkingwithPages-GeneratingRootandSubLevelPagesinOneNote).
- Get page revisions and roll back to previous version.
- Extract images from a OneNote document.
- [Extract or replace text from a Specified Page](https://docs.aspose.com/display/notejava/Working+with+Text) of a OneNote Document.
- Create a Table with Locked Columns in the OneNote Document.
- [Attach a File to the OneNote Document](https://docs.aspose.com/display/notejava/Working+with+Attachments).
- Ceate,save, read, convert [OneNote Notebook](https://docs.aspose.com/display/notejava/Working+with+OneNote+Notebook).
- [Many, many more](https://docs.aspose.com/display/notejava/Developer+Guide).

## Read & Write OneNote Format

**Microsoft OneNote:** ONE

## Save OneNote Files As

**Fixed Layout:** PDF
**Images:** GIF, JPEG, PNG, BMP, TIFF

## Read Formats

ONETOC2

## Supported Operating Systems

Aspose.Note for Java supports any operating system where Java runtime is installed including, but not limited to:

### Windows

- Microsoft Windows 2003 Server ( x64, x86)
- Microsoft Windows 2008 Server ( x64, x86)
- Microsoft Windows 2012 Server ( x64, x86)
- Microsoft Windows 2012 R2 Server ( x64, x86)
- Microsoft Windows Vista ( x64, x86)
- Microsoft Windows XP ( x64, x86)
- Microsoft Windows 7 ( x64, x86)
- Microsoft Windows 8, 8.1 ( x64, x86)
- Microsoft Windows 10 ( x64, x86)

## Supported Java Versions

- `J2SE 7.0 (1.7)`
- `J2SE 8.0 (1.8)`
- or above

## Get Started with Aspose.Note for Java

Aspose hosts all Java APIs at the [Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-note). You can easily use Aspose.BarCode for Java API directly in your Maven projects with simple configurations.

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

Then define Aspose.Note for Java API dependency in your `pom.xml` as follows:

```xml
<dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-note</artifactId>
        <version>20.5</version>
        <classifier>jdk17</classifier>
    </dependency>
</dependencies>
```

Congratulations! You have successfully defined the Aspose.Note for Java Maven dependency in your Maven project.

## Convert OneNote document to PDF with the Default Options using Java

```java
// For complete examples and data files, please go to https://github.com/aspose-note/Aspose.Note-for-Java
// Load the document into Aspose.Note.

String inputFile = "Sample1.one";
Path inputPath = Utils.getPath(LoadDocIntoAsposeNoteUsingPdfsaveoptions.class, inputFile);
String outputFile = "LoadDocIntoAsposeNoteUsingPdfsaveoptions.pdf";
Path outputPath = Utils.getPath(LoadDocIntoAsposeNoteUsingPdfsaveoptions.class, outputFile);

Document oneFile = new Document(inputPath.toString());

// Save the document as PDF
oneFile.save(outputPath.toString(), new PdfSaveOptions());
```

[Product Page](https://products.aspose.com/note/java) | [Docs](https://docs.aspose.com/display/notejava/Home) | [Demos](https://products.aspose.app/note/family) | [API Reference](https://apireference.aspose.com/java/note) | [Examples](https://github.com/aspose-note/Aspose.Note-for-Java) | [Blog](https://blog.aspose.com/category/note/) | [Free Support](https://forum.aspose.com/c/note) | [Temporary License](https://purchase.aspose.com/temporary-license)
