# CreateConnectionRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ApiKey** | **String** |  | [optional] 
**ApiSecret** | **String** |  | [optional] 
**Config** | [**AnyType**](.md) |  | [optional] 
**Label** | **String** |  | 
**Platform** | **String** |  | 
**ShopDomain** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$CreateConnectionRequest = Initialize-PSOpenAPIToolsCreateConnectionRequest  -ApiKey null `
 -ApiSecret null `
 -Config null `
 -Label null `
 -Platform null `
 -ShopDomain null
```

- Convert the resource to JSON
```powershell
$CreateConnectionRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

