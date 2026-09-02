# EventSubscription
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CallbackUrl** | **String** |  | 
**EventType** | **String** |  | 
**IsActive** | **Boolean** |  | 
**SubscriptionId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$EventSubscription = Initialize-PSOpenAPIToolsEventSubscription  -CallbackUrl null `
 -EventType null `
 -IsActive null `
 -SubscriptionId null
```

- Convert the resource to JSON
```powershell
$EventSubscription | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

