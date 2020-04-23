# Optical Character Recognition (OCR) C++ API

[Aspose.OCR for C++](https://products.aspose.com/ocr/cpp) is a standalone OCR API that enhances your C++ apps to perform the [OCR operation on JPEG, PNG, & BMP images](https://docs.aspose.com/display/ocrcpp/Supported+File+Formats) for extraction of English content.

## Image OCR API Features

- Recognize characters from images.
- Calculate the skew angle of images.
- Currently it supports English language.

## Read Image Formats for OCR

**Raster Formats:** JPEG, BMP ( 32bit and 16bit images are not supported), PNG

## Supported Charset for Recognition

EN

## Pre-requisites

Aspose OCR library requires `onnxruntime.dll` in the system path.

## Getting Started with Aspose.OCR for C++

Are you ready to give Aspose.OCR for C++ a try? Simply execute `Install-Package Aspose.OCR.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.OCR for C++ and want to upgrade the version, please execute `Update-Package Aspose.OCR.Cpp` to get the latest version.

Execute the following code snippet to see how Aspose.OCR API performs with your own samples or check the [GitHub Repository](https://github.com/aspose-ocr/Aspose.OCR-for-C) for other common usage scenarios.

## Perform OCR on PNG Image via C++ Code

```cpp
// For complete examples and data files, please go to https://github.com/aspose-ocr/Aspose.OCR-for-C
std::string image_path = "../Data/Source/sample.png";
const wchar_t* result = aspose::ocr::recognize_page(image_path.c_str());
std::wcout << result << L'\n';
```

## Evaluation Version Limitation

The evaluation version of Aspose.OCR for C++ limits the number of characters extracted from an image to 300.

[Product Page](https://products.aspose.com/ocr/cpp) | [Documentation](https://docs.aspose.com/display/ocrcpp/Home) | [Demo](https://products.aspose.app/ocr/family) | [API Reference](https://apireference.aspose.com/ocr/cpp) | [Examples](https://github.com/aspose-ocr/Aspose.OCR-for-C) | [Blog](https://blog.aspose.com/category/ocr/) | [Free Support](https://forum.aspose.com/c/ocr) |  [Temporary License](https://purchase.aspose.com/temporary-license)
