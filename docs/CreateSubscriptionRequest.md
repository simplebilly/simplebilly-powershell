# CreateSubscriptionRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventType** | **String** |  | 
**IsActive** | **Boolean** |  | [optional] 
**Name** | **String** |  | 
**Secret** | **String** |  | [optional] 
**Url** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$CreateSubscriptionRequest = Initialize-PSOpenAPIToolsCreateSubscriptionRequest  -EventType null `
 -IsActive null `
 -Name null `
 -Secret null `
 -Url null
```

- Convert the resource to JSON
```powershell
$CreateSubscriptionRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

