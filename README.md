# Azure Media Services v3 using .NET 8.0 (archived)

Microsoft has announced the retirement of Azure Media Services and so Jeskei is pressing ahead with its own media services platform built around IPFS for media storage and decentralised encoding and management services.

This repository will be archived and no further updates will be made to it.

## Usage

Backend services for interacting with Azure Media Services v3 using .NET 8.0 SDK, to encode, package, live stream, and protect videos with Azure Media Services v3 using [.NET 8.0 SDK](https://dotnet.microsoft.com/download).

To install the latest version of the Azure.ResourceManager.Media client SDK, go to the Nuget package [Azure.ResourceManager.Media](https://www.nuget.org/packages/Azure.ResourceManager.Media).

## Contents

| Folder | Description |
|-------------|-------------|
| **Account** ||
| [Account/CreateAccount](/Account/CreateAccount)|Create a Media Services account and set the primary storage account, in addition to advanced configuration settings including Key Delivery IP allowlist, Managed Identity, storage auth, and bring your own encryption key.|
| [Account/GetAccounts](/Account/GetAccounts)|List all Media Services accounts in a resource group and select one by its name.|
| [Account/Quotas](/Account/Quotas)|Get account quotas.|
| **Assets** ||
| [Assets/AssetManagement](/Assets/AssetManagement)|Manage assets in Media Services. Demonstrates how to create assets, set the container name, alternate identification, as well as list assets using paging and oData filters.|
| **Analytics** ||
| [AudioAnalytics/AudioAnalyzer](/AudioAnalytics/AudioAnalyzer)|Create a audio analyzer transform, upload a media file to an input asset, submit a job with the transform and download the results for verification.|
| **Encoding** ||
| [VideoEncoding/Encoding_PredefinedPreset](/VideoEncoding/Encoding_PredefinedPreset)|Submit a job using a built-in preset and an HTTP URL input, publish output asset for streaming, and download results for verification.|
| [VideoEncoding/Encoding_H264](/VideoEncoding/Encoding_H264)|Submit a job using a custom H.264 encoding preset, publish output asset for streaming, and download results for verification.|
| [VideoEncoding/Encoding_H264_ConstantRateFactor](/VideoEncoding/Encoding_H264_ConstantRateFactor)|Create a custom encoding Transform using custom H.264 Constant Rate Factor (CRF) encoding settings.|
| [VideoEncoding/Encoding_H264_ContentAware](/VideoEncoding/Encoding_H264_ContentAware)|Submit a job using a the built in Content Aware encoding preset for H.264. For details on the Content Aware Encoding preset, see the article - [Content Aware Encoding](https://learn.microsoft.com/azure/media-services/latest/encode-content-aware-concept).|
| [VideoEncoding/Encoding_H264_ContentAware_Constrained](/VideoEncoding/Encoding_H264_ContentAware_Constrained)|Submit a job using a custom constrained version of the Content Aware encoding preset for H.264. This is useful for situations where you need to control the behavior of the CAE encoder by reducing the number of outputs or bitrates into a defined range. Using the PresetConfigurations class, you can control the output for the CAE presets. For details on the Content Aware Encoding preset, see the article - [Content Aware Encoding](https://learn.microsoft.com/azure/media-services/latest/encode-content-aware-concept).|
| [VideoEncoding/Encoding_H264_Rotate90degrees](/VideoEncoding/Encoding_H264_Rotate90degrees)|Submit a job using a custom H.264 encoding preset and a rotation filter that rotates a video by 90 degrees, publish output asset for streaming, and download results for verification.|
| [VideoEncoding/Encoding_H264_To_TransportStream](/VideoEncoding/Encoding_H264_To_TransportStream)|Create a custom encoding Transform using custom H.264 encoding settings and output to MPEG transport stream format.|
| [VideoEncoding/Encoding_BuiltIn_CopyCodec](/VideoEncoding/Encoding_BuiltIn_CopyCodec)|Use the built-in Copy codec preset that can take a source video file that is already encoded using H264 and AAC audio, and copy it into MP4 tracks that are ready to be streamed by Azure Media Services.|
| [VideoEncoding/Encoding_BuiltIn_CopyCodecWithProxy](/VideoEncoding/Encoding_BuiltIn_CopyCodecWithProxy)|Use the built-in Copy codec preset that can take a source video file that is already encoded using H264 and AAC audio, and copy it into MP4 tracks that are ready to be streamed by Azure Media Services. In addition, this preset generates a fast proxy MP4 from the source video.|
| [VideoEncoding/Encoding_Custom_CopyCodecSpriteProxy](/VideoEncoding/Encoding_Custom_CopyCodecSpriteProxy)|Use a custom Copy codec preset that can take a source video file that is already encoded using H264 and AAC audio, and copy it into MP4 tracks that are ready to be streamed by Azure Media Services. In addition, this preset generates a fast proxy MP4 from the source video and a VTT sprite thumbnail.|
| [VideoEncoding/Encoding_HEVC](/VideoEncoding/Encoding_HEVC)|Submit a job using a custom HEVC encoding preset, publish output asset for streaming, and download results for verification.|
| [VideoEncoding/Encoding_HEVC_ContentAware](/VideoEncoding/Encoding_HEVC_ContentAware)|Submit a job using a the built in Content Aware encoding preset for HEVC (H.265). Using the PresetConfigurations class, you can control the output for the CAE presets. For details on the Content Aware Encoding preset, see the article - [Content Aware Encoding](https://learn.microsoft.com/azure/media-services/latest/encode-content-aware-concept).|
| [VideoEncoding/Encoding_HEVC_ContentAware_Constrained](/VideoEncoding/Encoding_HEVC_ContentAware_Constrained)|Submit a job using a custom constrained version of the Content Aware encoding preset for HEVC (H.265). This is useful for situations where you need to control the behavior of the CAE encoder by reducing the number of outputs or bitrates into a defined range. Using the PresetConfigurations class, you can control the output for the CAE presets. For details on the Content Aware Encoding preset, see the article - [Content Aware Encoding](https://learn.microsoft.com/azure/media-services/latest/encode-content-aware-concept).|
| [VideoEncoding/Encoding_StitchTwoAssets](/VideoEncoding/Encoding_StitchTwoAssets)|Submit a job using the JobInputSequence to stitch together 2 or more assets that may be clipped by start or end time. The resulting encoded file is a single video with all assets stitched together.  The sample will also  publish output asset for streaming and download results for verification.|
| [VideoEncoding/Encoding_SpriteThumbnail](/VideoEncoding/Encoding_SpriteThumbnail)|Submit a job using a custom preset with a thumbnail sprite, publish output asset for streaming, and download results for verification.|
| [VideoEncoding/Encoding_OverlayImage](/VideoEncoding/Encoding_OverlayImage)|Overlay an image logo or watermark on a video, publish output asset for streaming, and download results for verification.|
| [VideoEncoding/Encoding_MultiChannelAudio](/VideoEncoding/Encoding_MultiChannelAudio)|Create an encoding Transform that uses channel mapping and audio track selection from the input source to output two new AAC audio tracks.|
| [VideoEncoding/Encoding_Live_Archive_To_MP4](/VideoEncoding/Encoding_Live_Archive_To_MP4)|Use the archived output from a live event and extract only the top highest bitrate video track to be packaged into an MP4 file for export to social media platforms, or for use with Video Indexer.|
| **Live Streaming** ||
| [Live/LiveEventWithDVR](/Live/LiveEventWithDVR)|Create a LiveEvent with a full archive up to 25 hours and an filter on the asset with 5 minutes DVR window, then use the filter to create a locator for streaming.|
| **VOD Streaming** ||
| [Streaming/AssetFilters](/Streaming/AssetFilters)|Create a transform with built-in AdaptiveStreaming preset, submit a job, create an asset-filter and an account-filter, associate the filters to streaming locators and print urls for playback.|
| [Streaming/StreamHLSAndDASH](/Streaming/StreamHLSAndDASH)|Create a transform with built-in AdaptiveStreaming preset, submit a job, publish output asset for HLS and DASH streaming.|
| [Streaming/StreamExistingMp4](/Streaming/StreamExistingMp4)|Upload and stream from an existing, pre-encoded MP4 file.  This can be useful if you have content encoded in FFMPEG or an external encoder tool or service that you would like to upload and stream from Media Services.  This sample shows the process for uploading the MP4 file (single bitrate), the code for generating the server manifest (.ism) as well as the client manifest (.ismc) that are required for streaming with Dynamic Packaging from the Streaming Endpoint (origin server)|
| **Content protection** ||
| [ContentProtection/BasicAESClearKey](/ContentProtection/BasicAESClearKey)|Create a transform with built-in content aware encoding preset and an HTTP URL input, submit a job, create a ContentKeyPolicy using a secret key, associate the ContentKeyPolicy with StreamingLocator, get a token and print a url for playback in Azure Media Player. When a stream is requested by a player, Media Services uses the specified key to dynamically encrypt your content with AES-128 and Azure Media Player uses the token to decrypt.|
| [ContentProtection/BasicPlayReady](/ContentProtection/BasicPlayReady)|Create a transform with built-in AdaptiveStreaming preset and an HTTP URL input, submit a job, create a ContentKeyPolicy with PlayReady configuration using a secret key, associate the ContentKeyPolicy with StreamingLocator, get a token and print a url for playback in a Azure Media Player on Microsoft Edge. When a user requests PlayReady-protected content, the player application requests a license from the Media Services license service. If the player application is authorized, the Media Services license service issues a license to the player. A PlayReady license contains the decryption key that can be used by the client player to decrypt and stream the content.|
| [ContentProtection/BasicWidevine](/ContentProtection/BasicWidevine)|Create a transform with built-in AdaptiveStreaming preset and an HTTP URL input, submit a job, create a ContentKeyPolicy with Widevine configuration using a secret key, associate the ContentKeyPolicy with StreamingLocator, get a token and print a url for playback in a Azure Media Player on Google Chrome. When a user requests Widevine-protected content, the player application requests a license from the Media Services license service. If the player application is authorized, the Media Services license service issues a license to the player. A Widevine license contains the decryption key that can be used by the client player to decrypt and stream the content.|
| [ContentProtection/BasicPlayReadyAndWidevine](/ContentProtection/BasicPlayReadyAndWidevine)|Create a transform with built-in Content Aware Encoding preset and an HTTP URL input, submit a job, create a ContentKeyPolicy with PlayReady and Widevine configurations using a secret key, associate the ContentKeyPolicy with StreamingLocator, get a token and print a url for playback in a Azure Media Player on Microsoft Edge or Google Chrome. When a user requests PlayReady or Widevine protected content, the player application requests a license from the Media Services license service. If the player application is authorized, the Media Services license service issues a license to the player. A license contains the decryption key that can be used by the client player to decrypt and stream the content.|
| [ContentProtection/OfflineFairPlay](/ContentProtection/OfflineFairPlay)|Dynamically encrypt your content with Apple FairPlay DRM and play the content without requesting each time a new license from license service. create a transform with built-in AdaptiveStreaming preset and an HTTP URL input, submit a job, create a ContentKeyPolicy with open restriction and FairPlay persistent configuration, associate the ContentKeyPolicy with a StreamingLocator and print a url for playback.|When a user plays the first time the FairPlay-protected content, the player application requests a license from the Media Services license service. The Media Services license service issues a license to the player and the license is persisted. Because the license is persisted, subsequent playback won't send a request to Media Services license service again.
| [ContentProtection/OfflinePlayReadyAndWidevine](/ContentProtection/OfflinePlayReadyAndWidevine)|Dynamically encrypt your content with PlayReady and Widevine DRM and play the content without requesting each time a new license from license service. Create a transform with built-in AdaptiveStreaming preset and an HTTP URL input, submit a job, create a ContentKeyPolicy with a token restriction and PlayReady/Widevine persistent configuration, associate the ContentKeyPolicy with a StreamingLocator, get a token and print a url for playback. When a user plays the first time the DRM-protected content, the player application requests a license from the Media Services license service. If the player application is authorized, the Media Services license service issues a license to the player and the license is persisted. Because the license is persisted, subsequent playback won't send a request to Media Services license service again.|

## Prerequisites

- A Windows 10/11 PC, Mac or Linux
- [Visual Studio 2022](https://visualstudio.microsoft.com/) (Windows 10/11), or optional [Visual Studio Code](https://code.visualstudio.com/) (Windows, Mac or Linux)
- .NET 8.0 SDK : <https://dotnet.microsoft.com/download>

## Setup

- Clone or download this sample repository.
- Open the solution file Jeskei-Media-API.sln in Visual Studio 2022, or open the folder in Visual Studio Code.
- Update the settings in **appsettings.json** in the root folder of the repository to match your Azure subscription, resource group and Media Services account.
- To ignore changes on `appsettings.json` and avoid pushing custom data back to your repository, you may run the following git command: `git update-index --assume-unchanged  appsettings.json`
- Read sample's README.md to see what key concepts to review and how to set up and run the sample.
- Select the project to Run in the Debugger (ctrl-shift-D in VS Code on Window) and press F5 to launch

## Troubleshooting and known issues

| Issue or Error message | Notes |
|-------------|-----------|
|"Encountered error while fetching the list of EventHub PartitionIds" | Make sure that you are using the SAS policy for the EventHub and not the EventHub namespace. Also make sure that your .env or appsettings.json file is pointing to the name of the EventHub (instance) and not the EventHub namespace (which is higher level entity in the portal).|
