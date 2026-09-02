# OAuthCallbackRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **String** |  | 
**Config** | [**AnyType**](.md) |  | [optional] 
**ConnectionId** | **String** |  | [optional] 
**Platform** | **String** |  | 
**ShopDomain** | **String** |  | [optional] 
**State** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$OAuthCallbackRequest = Initialize-PSOpenAPIToolsOAuthCallbackRequest  -Code null `
 -Config null `
 -ConnectionId null `
 -Platform null `
 -ShopDomain null `
 -State null
```

- Convert the resource to JSON
```powershell
$OAuthCallbackRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

