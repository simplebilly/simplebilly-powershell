# OAuthAuthorizeResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AuthorizationUrl** | **String** |  | 
**State** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$OAuthAuthorizeResponse = Initialize-PSOpenAPIToolsOAuthAuthorizeResponse  -AuthorizationUrl null `
 -State null
```

- Convert the resource to JSON
```powershell
$OAuthAuthorizeResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

