This video manipulation REST API helps your cloud-based applications to retrieve video files hosted on the cloud & modify them from within your C# & .NET apps.

Aspose.Video Cloud SDK for .NET is available to use under an MIT license. Enhance your C#, ASP.NET, and other .NET cloud programs to join multiple cloud videos into a single clip, change the video codec (x265, x264, QuickTime H.264 and others). Aspose.Video Cloud SDK for .NET supports all popular video formats and assists you in setting various properties of cloud videos, such as, resolution, volume level, FPS and others. Use this REST API to add an additional audio track to your video clip.

## Video Processing Features

- Video conversion from AVI to MP4 format.
- Add image or text watermark in the video clip.
- Add multiple audio tracks to a video clip.
- Change video resolution, aspect ratio, bit-rate & FPS.
- Combine multiple video clips & join them together.
- Change video encoding by applying various codecs.
- Programmatically change video playback speed.
- Drop video volume level to 50% of the current volume.
- Extract a video frame and save it as a thumbnail image.
- Extract a clip from the video file and save it as a separate video.
- Fetch all properties of a particular video file.
- Fetch video file from web and upload it to the cloud storage.


## Supported Video Formats

WMV, AVI, FLV, MKV, MK3D, MKA, MKS, WEBM, MP4, MXF, MOV, QT

## Supported Video Codecs

Apple ProRes, DNxHD, H.264, H.265, Motion JPEG, VP6, VP8, VP9, XviD, Windows Media Video v9

## Various Settings

Resolution: up to 4K (3840 x 2160), Chroma subsampling: 4:2:0, 4:2:2, Color depth: 8 bit, 10 bit

## Supported Audio Codecs

AAC, AC-3, MP3, Opus, WMA

## Platform Independence

Aspose.Video Cloud’s platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Getting Started with Aspose.Video Cloud SDK for .NET

You do not need to install anything to get started with Aspose.Video Cloud SDK for .NET. Just create an account at [Aspose for Cloud](https://dashboard.aspose.cloud/#/apps) and get your application information.

Simply execute `Install-Package Aspose.Video-Cloud` from the Package Manager Console in Visual Studio to fetch & reference Aspose.Video assembly in your project. If you already have Aspose.Video Cloud SDK for .NET and want to upgrade it, please execute `Update-Package Aspose.Video-Cloud` to get the latest version.

Please check the [GitHub Repository](https://github.com/aspose-video-cloud/aspose-video-cloud-dotnet) for other common usage scenarios.

## Use C# to Get Information about a Hosted AVI File

The following code sample demonstrates, how to fetch information of a cloud hosted AVI video file using C# code:

```csharp
var localName = "sample.avi";
var remoteName = "TestGetVideo.avi";
var fullName = Path.Combine(this.dataFolder, remoteName);

this.StorageApi.PutCreate(fullName, null, null, File.ReadAllBytes(BaseTestContext.GetDataDir() + localName));
var request = new GetVideoRequest(remoteName, this.dataFolder);
var actual = this.VideoApi.GetVideo(request);
```

## Convert AVI to MP4 Video File using C# Code

The following C# code sample elaborates, how to convert a video AVI file to MP4 video file in the cloud:

```csharp
var localName = "sample.avi";
var remoteName = "toconvert.avi";
var fullName = Path.Combine(this.dataFolder, remoteName);
var resultPath = Path.Combine(this.dataFolder, "converted.mp4");
ConvertOptions options = new ConvertOptions();

this.StorageApi.PutCreate(fullName, null, null, File.ReadAllBytes(BaseTestContext.GetDataDir() + localName));

var request = new PostConvertVideoRequest(remoteName, "mp4", resultPath, options, this.dataFolder);
var actual = this.VideoApi.PostConvertVideo(request);
```

[Product Page](https://products.aspose.cloud/video/net) | [Documentation](https://docs.aspose.cloud/display/videocloud/Home) | [API Reference](https://apireference.aspose.cloud/video/) | [Code Samples](https://github.com/aspose-video-cloud/aspose-video-cloud-dotnet) | [Blog](https://blog.aspose.cloud/category/video/) | [Free Support](https://forum.aspose.cloud/c/video) | [Free Trial](https://dashboard.aspose.cloud/#/apps)