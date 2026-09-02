# GatewayOAuthAuthorizeRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GatewayType** | **String** |  | 
**RedirectUri** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GatewayOAuthAuthorizeRequest = Initialize-PSOpenAPIToolsGatewayOAuthAuthorizeRequest  -GatewayType null `
 -RedirectUri null
```

- Convert the resource to JSON
```powershell
$GatewayOAuthAuthorizeRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

