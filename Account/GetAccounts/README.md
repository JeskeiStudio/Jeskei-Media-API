# Get Media Services accounts from a resource group

List all Media Services accounts in a resource group and select one by its name.

## Prerequisites

Required Assemblies:

* Azure.Identity
* Azure.ResourceManager.Media
* Microsoft.Extensions.Hosting

## Build and run

Update the settings in **appsettings.json** in the root folder of the repository to match your Azure subscription, resource group and Media Services account.
Then build and run in Visual Studio or VS Code.

This will authenticate using any of the methods supported by [`DefaultAzureCredential`](https://learn.microsoft.com/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet).
