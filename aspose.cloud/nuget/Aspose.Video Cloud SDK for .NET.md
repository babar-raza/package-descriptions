# .NET Cloud REST API for Video Processing

This video manipulation REST API helps your cloud-based applications to [retrieve video files hosted on the cloud](https://products.aspose.cloud/video/net) & modify them from within your C# & .NET apps.

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

## New Features in Version 18.2.1

- This is the first version of Aspose.Video for Cloud.

For the detailed notes, please visit [Aspose.Video Cloud 18.2.1 Release Notes](https://docs.aspose.cloud/display/videocloud/Aspose.Video+Cloud+18.2.1+Release+Notes).

## Supported Video Formats

WMV, AVI, FLV, MKV, MK3D, MKA, MKS, WEBM, MP4, MXF, MOV, QT

## Supported Video Codecs

Apple ProRes, DNxHD, H.264, H.265, Motion JPEG, VP6, VP8, VP9, XviD, Windows Media Video v9

## Various Settings

Resolution: up to 4K (3840 x 2160), Chroma subsampling: 4:2:0, 4:2:2, Color depth: 8 bit, 10 bit

## Supported Audio Codecs

AAC, AC-3, MP3, Opus, WMA

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
