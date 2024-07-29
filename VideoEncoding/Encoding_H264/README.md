# Encode with a custom Transform

Create a custom encoding Transform using custom H.264 encoding settings. Perform the following tasks:

1. Creates a custom encoding transform using H.264
1. Creates an input asset and upload a media file into it.
1. Submits a job and monitoring the job using polling method.
1. Downloads the output asset.
1. Prints URLs for streaming.

## Prerequisites

Required Assemblies:

* Azure.Identity
* Azure.ResourceManager.Media
* Azure.Storage.Blobs
* System.Linq.Async

An Azure Media Services account. See the steps described in [Create a Media Services account](https://learn.microsoft.com/azure/media-services/latest/account-create-how-to).

## Build and run

Update the settings in **appsettings.json** in the root folder of the repository to match your Azure subscription, resource group and Media Services account.
Then build and run in Visual Studio or VS Code.