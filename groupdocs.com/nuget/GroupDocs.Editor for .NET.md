It is a .NET API that enhances your apps to perform document, spreadsheets, DSV & XML files editing operations for a wide range of file formats.

## Document Editor Processing Features

- Edit word processing documents in a flow or paged mode.
- Fetch language information for multi-lingual document editing.
- Extract font information to provide consistent editing and appearance behavior.
- Edit multi-tabbed spreadsheets.
- Supports DSV (Delimiter-Separated Values) documents.
- Specify separator, flexible numeric and data conversion for CSV & TSV files.
- Availability of memory usage optimization for large CSV & TSV files.
- Fix incorrect XML document structure.
- Recognize URIs and email addresses in XML files.
- Extract basic information about the edited document.
- Set character encoding of the input text document.
- Grab document metadata information.
- Fetch whole HTML document or BODY content.
- Get HTML document along with all its resources (stylesheets, images).
- Open any supported format file in HTML format and save to disk.
- Fetch HTML markup from DB or remote storage.

## Editable File Formats

**Word Processing:** DOC, DOCX, DOCM, DOT, DOTM, DOTX, FlatOPC, ODT, OTT, RTF, WordML
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLTX, XLTM, XLSB, XLAM, SXC, SpreadsheetML, ODS, FODS, DIF, DSV, CSV, TSV
**Presentation:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, ODP, OTP
**Other:** TXT, HTML, XML

## Auto-detect File Formats

**Word Processing:** DOC, DOCX, DOCM, DOT, DOTM, DOTX, ODT, OTT, RTF
**Spreadsheet:** XLS, XLT, XLSX, XLSM, XLTX, XLTM, XLSB, XLAM, SXC, SpreadsheetML, ODS, FODS, DIF
**Presentation:** PPT, PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, ODP, OTP

## Platform Independence

GroupDocs.Editor for .NET does not require any external software or third party tool to be installed. GroupDocs.Editor for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure
**Mac OS:** Mac OS X
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET and Mono frameworks.

## Getting Started with GroupDocs.Editor for .NET

You do not need to install anything to get started with GroupDocs.Editor for .Net. Just create an account at GroupDocs for Cloud and get your application information. That is all! You are ready to use GroupDocs.Editor for .Net.

Simply execute `Install-Package GroupDocs.Editor` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Editor assembly in your project. If you already have GroupDocs.Editor for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Editor` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-editor/GroupDocs.Editor-for-.NET) for other common usage scenarios.

## Load, Edit & Save Multi-tab Spreadsheet via C# Code

```csharp
//1. Get a path to the input file (or stream with file content).
//In this case it is sample XLSX (OOXML) with two tabs.
string inputFilePath = Constants.SAMPLE_XLSX;

//2. Load it into Editor instance from stream
using (FileStream inputStream = File.OpenRead(inputFilePath))
{
    using (Editor editor = new Editor(delegate { return inputStream;}, delegate { return new SpreadsheetLoadOptions();}))
    {
        //3. Let's create an intermediate EditableDocument from 1st tab
        SpreadsheetEditOptions editOptions1 = new SpreadsheetEditOptions();
        editOptions1.WorksheetIndex = 0;//index is 0-based
        EditableDocument firstTabBeforeEdit = editor.Edit(editOptions1);

        //4. Let's create an intermediate EditableDocument from 2nd tab
        SpreadsheetEditOptions editOptions2 = new SpreadsheetEditOptions();
        editOptions2.WorksheetIndex = 1;//index is 0-based
        EditableDocument secondTabBeforeEdit = editor.Edit(editOptions2);

        //5. Save first tab from EditableDocument #1 to separate document
        SpreadsheetSaveOptions saveOptions1 = new SpreadsheetSaveOptions(SpreadsheetFormats.Xlsm);
        string outputFilename1 = Path.GetFileNameWithoutExtension(inputFilePath) + "_tab1.xlsm";
        string outputPath1 = Path.Combine(Constants.GetOutputDirectoryPath(), outputFilename1);
        editor.Save(firstTabBeforeEdit, outputPath1, saveOptions1);

        //6. Save second tab from EditableDocument #2 to separate document
        SpreadsheetSaveOptions saveOptions2 = new SpreadsheetSaveOptions(SpreadsheetFormats.Xlsb);
        string outputFilename2 = Path.GetFileNameWithoutExtension(inputFilePath) + "_tab2.xlsb";
        string outputPath2 = Path.Combine(Constants.GetOutputDirectoryPath(), outputFilename2);
        editor.Save(secondTabBeforeEdit, outputPath2, saveOptions2);

        //7. Dispose both EditableDocument instances
        firstTabBeforeEdit.Dispose();
        secondTabBeforeEdit.Dispose();
    }
}
```

[Product Page](https://products.groupdocs.com/editor/net) | [Documentation](https://docs.groupdocs.com/display/editornet/Home) | [API Reference](https://apireference.groupdocs.com/net/editor) | [Code Samples](https://github.com/groupdocs-editor/GroupDocs.Editor-for-.NET) | [Blog](https://blog.groupdocs.com/category/editor/) | [Free Support](https://blog.groupdocs.com/category/editor/) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
