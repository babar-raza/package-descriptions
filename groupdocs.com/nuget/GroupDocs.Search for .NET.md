# .NET API for Search & Index

This .NET API enhances your apps to [perform robust search & index operations](https://products.groupdocs.com/search/net) based on fuzzy as well as synonym algorithms. Supports several types of searches.

## Document Search Processing Features

- Create index in memory or on the local disk.
- Merge several indexes.
- Improve search performance by optimizing index.
- Index password protected files.
- Index with stop words.
- Support for indexing additional fields.
- Supports blended characters.
- Support for characters indexed as a whole word.
- Support for character replacement during indexing.
- Support for custom text extractors.
- Option for compact and metadata index.
- Save extracted text in index with different level of compression.
- Document filtering during indexing.
- Delete indexed paths from index.
- Filter documents in search results.
- Search for different object types, such as, text, numbers, dates, filenames etc.
- Combining different types of search into one search query.
- Alias substitution in search queries.
- Perform spell check during search.
- Perform keyboard layout correction during search.
- Search queries in text or flexible object form.
- Highlighting search results in the text of the entire document or in text segments.
- Multiple simultaneous thread safe search.
- Thread safe search during indexing, updating or merging operation.
- Search over several indexes simultaneously.

## New Features in Version 20.4

- Implemented changing path without reindexing for renamed documents.
- Implemented the ability to change attributes of indexed documents without reindexing.

For the detailed notes, please visit [GroupDocs.Search for .NET 20.4 Release Notes](https://docs.groupdocs.com/display/searchnet/GroupDocs.Search+for+.NET+20.4+Release+Notes).

## Indexing Content File Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheets:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, XLA, XLAM, ODS, OTS, CSV, TSV, XML
**Presentations:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP
**Emails:** PST, OST, EML, EMLX, MSG
**Notes:** ONE
**Archives:** ZIP
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2

## Indexing Metadata File Formats

**Word Processing:** DOC, DOT, DOCX, DOCM, DOTX, DOTM, TXT, ODT, OTT, RTF
**Spreadsheets:** XLS, XLT, XLSX, XLSM, XLSB, XLTX, XLTM, XLA, XLAM, ODS, OTS, CSV, TSV, XML
**Presentations:** PPT, PPS, POT, PPTX, PPTM, POTX, POTM, PPSX, PPSM, ODP
**Emails:** PST, OST, EML, EMLX, MSG
**Notes:** ONE
**Archives:** ZIP
**Audio:** MP3, WAV
**Portable:** PDF
**Markup:** HTML, XHTML, MHTML, MD, XML
**eBook:** CHM, EPUB, FB2
**Image:** BMP, GIF, JP2, PNG, WEBP, TIFF, JPG, PSD, DJVU
**Metafiles:** EMF, WMF
**Project Management:** MPP
**Torrent:** TORRENT
**Visio Diagram:** VSD, VSS
**Medical Imagery:** DCM
**Video:** AVI, MOV, QT, FLV, ASF

## Supported Search Types

- Simple word
- Boolean
- Regular expression
- Faceted
- Case sensitive
- Flexible fuzzy
- Synonym
- Homophone
- Wildcard
- Phrase
- Data range
- Numeric range
- Search by chunks
- Object type search

## Platform Independence

GroupDocs.Search for .NET does not require any external software or third party tool to be installed. GroupDocs.Search for .NET supports any 32-bit or 64-bit operating system where .NET or Mono framework is installed. The other details are as follows:

**Microsoft Windows:** Microsoft Windows Desktop (x86, x64) (XP & up), Microsoft Windows Server (x86, x64) (2000 & up), Windows Azure
**Mac OS:** Mac OS X
**Linux:** Linux (Ubuntu, OpenSUSE, CentOS and others)
**Development Environments:** Microsoft Visual Studio (2010 & up), Xamarin.Android, Xamarin.IOS, Xamarin.Mac, MonoDevelop 2.4 and later.
**Supported Frameworks:** GroupDocs.Conversion for .NET  supports .NET and Mono frameworks.

## Getting Started with GroupDocs.Search for .NET

Are you ready to give GroupDocs.Search for .NET a try? Simply execute `Install-Package GroupDocs.Search` from Package Manager Console in Visual Studio to fetch & reference GroupDocs.Search assembly in your project. If you already have GroupDocs.Search for .Net and want to upgrade it, please execute `Update-Package GroupDocs.Search` to get the latest version.

Please check the [GitHub Repository](https://github.com/groupdocs-search/GroupDocs.Search-for-.NET) for other common usage scenarios.

## Use C# to Perform Regular Expression Search

```csharp
string indexFolder = @"c:\MyIndex\";
string documentsFolder = @"c:\MyDocuments\";

// creating an index in the specified folder
Index index = new Index(indexFolder);

// indexing documents from the specified folder
index.Add(documentsFolder);

// search for the phrase in text form
// the first caret character at the beginning indicates that this is a regular expression search query
string query1 = "^^(.)\\1{1,}";
// search for two or more identical characters at the beginning of a word
SearchResult result1 = index.Search(query1); 

// search for the phrase in object form
// search for two or more identical characters at the beginning of a word
SearchQuery query2 = SearchQuery.CreateRegexQuery("^(.)\\1{1,}");
SearchResult result2 = index.Search(query2);
```

## Spell Check with Smart Search via C# Code

```csharp
string indexFolder = @"c:\MyIndex\";
string documentsFolder = @"c:\MyDocuments\";

// creating an index in the specified folder
Index index = new Index(indexFolder);

// indexing documents from the specified folder
index.Add(documentsFolder);

// creating a search options instance
SearchOptions options = new SearchOptions();
// enabling the spelling correction
options.SpellingCorrector.Enabled = true;
// setting the maximum number of mistakes
options.SpellingCorrector.MaxMistakeCount = 1;
// enabling the option for only the best results of the spelling correction
options.SpellingCorrector.OnlyBestResults = true;

// search for the word "Rleativity" containing a spelling error
// the word "Relativity" will be found that differs from the search query in two transposed letters
SearchResult result = index.Search("Rleativity", options);
```

## Limitations

[Product Page](https://products.groupdocs.com/search/net) | [Documentation](https://docs.groupdocs.com/display/searchnet/Home) | [Live Demo](https://products.groupdocs.app/search/family) | [API Reference](https://apireference.groupdocs.com/net/search) | [Examples](https://github.com/groupdocs-search/GroupDocs.Search-for-.NET) | [Blog](https://blog.groupdocs.com/category/search/) | [Free Support](https://forum.groupdocs.com/c/search) | [Temporary License](https://purchase.groupdocs.com/temporary-license)
