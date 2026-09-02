# UpdateConnectionRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ApiKey** | **String** |  | [optional] 
**ApiSecret** | **String** |  | [optional] 
**Config** | [**AnyType**](.md) |  | [optional] 
**IsActive** | **Boolean** |  | [optional] 
**Label** | **String** |  | [optional] 
**ShopDomain** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$UpdateConnectionRequest = Initialize-PSOpenAPIToolsUpdateConnectionRequest  -ApiKey null `
 -ApiSecret null `
 -Config null `
 -IsActive null `
 -Label null `
 -ShopDomain null
```

- Convert the resource to JSON
```powershell
$UpdateConnectionRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

