# Prints quotas for a Media Services account

Use the metrics API to retrieve account quotas.

## Example output

```
Resource               Current     Quota
--------            ----------  --------
Assets                      19   1000000
Content Key Polices          1   1000000
Streaming Policies           0       100
Live Events                  2         5
Running Live Events          0         5
Transforms                           100
Jobs                              500000
Jobs Scheduled               0
```

## Prerequisites

Required Assemblies:

* Azure.Identity
* Azure.Monitor.Query
* Azure.ResourceManager.Media

## Build and run

Update the settings in **appsettings.json** in the root folder of the repository to match your Azure subscription, resource group and Media Services account.
Then build and run in Visual Studio or VS Code.

This will authenticate using any of the methods supported by [`DefaultAzureCredential`](https://learn.microsoft.com/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet).
