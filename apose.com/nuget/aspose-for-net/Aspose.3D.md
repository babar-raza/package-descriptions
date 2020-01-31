Aspose.3D for .NET is a standalone, on premise API to help developers seamlessly integrate 3D processing & rendering functionality into .NET based applications.
Aspose.3D for .NET enhances your .NET applications to work with various materials (lambert, phong, shader-based, PBR, PBR specular), textures (diffuse, advanced texture), meshes (polygon, triangle-based) geometries (vertex, NURBS, parameterized), vertex elements, local transformation, instancing, scene graph, custom property, skeleton, morph deformer, property animation, mesh compression and more. 

## 3D File Processing Features
- Detect format of a 3D file.
- Import, create, customize, & save 3D scenes.
- Create 3D mesh & scale geometries of a 3D scene.
- Configure cube by setting up normals or UV.
- Perform element formatting using 3D transformations.
- Share geometry data among multiple nodes of a mesh.
- Add 3D scene animation.
- Work with 3D objects & models.

## Read & Write 3D Formats
**Autodesk:** FBX 7.2 to 7.5 (ASCII/Binary)
**3D Systems CAD::** STL (ASCII/Binary)
**Wavefront:** OBJ
**Discreet 3D Studio:** 3DS
**Universal3D:** U3D
**Collada:** DAE
**GL Transmission:** glTF (ASCII/Binary)
**Google Draco:** DRC
**RVM:** (Text/Binary)
**Portable Document Format:** PDF
**Other:** AMF, PLY (ASCII/Binary)

## Save 3D Files As
**WEB:** HTML

## Read 3D Formats
**DirectX:** X (ASCII/Binary)
**Siemens:** JT 
**Other:** DXF, ASF, VRML, 3MF

## Platform Independence
Aspose.3D for .NET is written in C# and supports Windows Forms as well as ASP.NET apps. Development can be performed on any platform that has .NET environment for both 32-bit and 64-bit applications. It supports .NET Frameworks 2.0 uptil 4.7.2 as well as Client Profile version for .NET Framework 4.0.

## Getting Started with Aspose.3D for .NET
Are you ready to give Aspose.3D for .NET a try? Simply execute `Install-Package Aspose.3D` from the Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.3D for .NET and want to upgrade the version, please execute `Update-Package Aspose.3D` to get the latest version.

## Build a Scene with Primitive 3D Models using C#
You can execute below code snippet to see how Aspose.3D API performs in your environment or check the [GitHub Repository](https://github.com/aspose-3d/Aspose.3D-for-.NET) for other common usage scenarios.
```csharp
// initialize a Scene object
Scene scene = new Scene();
// create a Box model
scene.RootNode.CreateChildNode("box", new Box());
// create a Cylinder model
scene.RootNode.CreateChildNode("cylinder", new Cylinder());
// save drawing in FBX format
scene.Save(dir + "output.fbx", FileFormat.FBX7500ASCII);
```

## Export 3D Scene to Compressed AMF via C#
Aspose.3D for .NET enables you to save 3D meshes in custom binary format, get all property values of 3D scenes as well as flip their coordinate system. Following example demonstrates the conversion of a 3D scene to AMF format while applying compression to it.
```csharp
// load a scene
Scene scene = new Scene();
var box = new Box();
var tr = scene.RootNode.CreateChildNode(box).Transform;
tr.Scale = new Vector3(12, 12, 12);
tr.Translation = new Vector3(10, 0, 0);
tr = scene.RootNode.CreateChildNode(box).Transform;
// scale transform
tr.Scale = new Vector3(5, 5, 5);
// set Euler angles
tr.EulerAngles = new Vector3(50, 10, 0);
scene.RootNode.CreateChildNode();
scene.RootNode.CreateChildNode().CreateChildNode(box);
scene.RootNode.CreateChildNode().CreateChildNode(box);
// save compressed AMF file
scene.Save(dir + "output.amf", new AMFSaveOptions() { EnableCompression = true });
```
[Product Page](https://products.aspose.com/3d/net) | [Documentation](https://docs.aspose.com/display/3dnet/Home) | [API Reference](https://apireference.aspose.com/net/3d) | [Code Examples](https://github.com/aspose-3d/Aspose.3D-for-.NET) | [Blog](https://blog.aspose.com/category/3d/) | [Free Support](https://forum.aspose.com/c/3d) |  [Temporary License](https://purchase.aspose.com/temporary-license)
