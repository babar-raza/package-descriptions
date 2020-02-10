Aspose.3D Cloud SDK for .NET REST API provides you a seamless way to integrate 3D object manipulation features into your cloud-based C# & other .NET apps.

Aspose.3D Cloud SDK for .NET is available under an MIT license. It enhances your C# code to create 3D entities, objects and models in the cloud. Your .NET cloud-based apps would be able to work with various 3D entities, such as, box, sphere, plane, torus, & cylinder. Aspose.3D Cloud SDK for .NET allows your C# cloud apps to extract raw data or 3D content from Adobe Acrobat 3D PDF files.

## 3D Processing Features

- Create 3D entities (Box, Sphere, Plane, Torus, Cylinder).
- Perform processing of 3D models and attributes.
- Perform transformation, translation, rotation & scaling of 3D objects.
- Conversion of 3D files to another format.
- Convert whole of the 3D file or convert a specific part only.
- Extract 3D scenes and export to various formats.
- Perform parametric modeling, 3D modeling & data processing.
- Create cloud-based folder structure & perform cloud-based conversion of 3D files.
- Extract raw data or 3D content from a password-protected 3D PDF file.
- Supports working with triangulate meshes, triangulate whole or part of the 3D scene.
- Address nodes by object addressing path or remove nodes with attached light or camera.
- Remove 3D objects from a scene.

## Read & Write 3D Formats

3DS, AMF, RVM, DAE, DRC, FBX, GLTF, OBJ, PDF, PLY, STL, U3D

## Read 3D Formats

DXF, JT, DirectX X, 3MF, ASE

## Platform Independence

Aspose.3D Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.3D Cloud SDK for .NET

You do not need to install anything to get started with Aspose.3D Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.3D-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.3D assembly in your project. If you already have Aspose.3D Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.3D-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-3d-cloud/aspose-3d-cloud-dotnet) for other common usage scenarios.

## Using C# to Convert FBX 3D file to PDF

The following code sample demonstrates, how to convert a 3D FBX file to PDF using C# code:

```csharp
string name = "Input.fbx";
string newformat = "pdf";
string newfilename = "Output.pdf";
string folder = "3DTest";
bool isOverwrite = true;
string storage = "First Storage";
var response = threeDCloudApi.PostConvertByFormatWithHttpInfo(name, newformat, newfilename, folder, isOverwrite, storage);
Assert.AreEqual(response.StatusCode, 200);
```

[Product Page](https://products.aspose.cloud/3d/net) | [Documentation](https://docs.aspose.cloud/display/3dcloud/Aspose.3D+Cloud+Product+Family+Home) | [API Reference](https://apireference.aspose.cloud/3d/) | [Code Samples](https://github.com/aspose-3d-cloud/aspose-3d-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/3d/) | [Free Support](https://forum.aspose.cloud/c/3d) | [Free Trial](https://dashboard.aspose.cloud/#/apps)