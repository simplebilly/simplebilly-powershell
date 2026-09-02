# UpdateSubscriptionRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventType** | **String** |  | [optional] 
**IsActive** | **Boolean** |  | [optional] 
**Name** | **String** |  | [optional] 
**Secret** | **String** |  | [optional] 
**Url** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$UpdateSubscriptionRequest = Initialize-PSOpenAPIToolsUpdateSubscriptionRequest  -EventType null `
 -IsActive null `
 -Name null `
 -Secret null `
 -Url null
```

- Convert the resource to JSON
```powershell
$UpdateSubscriptionRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

