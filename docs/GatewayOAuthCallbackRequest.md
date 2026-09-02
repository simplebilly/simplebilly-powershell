# GatewayOAuthCallbackRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **String** |  | 
**GatewayType** | **String** |  | 
**RedirectUri** | **String** |  | 
**State** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GatewayOAuthCallbackRequest = Initialize-PSOpenAPIToolsGatewayOAuthCallbackRequest  -Code null `
 -GatewayType null `
 -RedirectUri null `
 -State null
```

- Convert the resource to JSON
```powershell
$GatewayOAuthCallbackRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

