# OAuthAuthorizeRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Config** | [**AnyType**](.md) | Optional platform-specific config (e.g. Shopify &#x60;shop_domain&#x60;, &#x60;api_key&#x60;, &#x60;api_secret&#x60;) needed to build the authorization URL. | [optional] 
**Platform** | **String** |  | 
**RedirectUri** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$OAuthAuthorizeRequest = Initialize-PSOpenAPIToolsOAuthAuthorizeRequest  -Config null `
 -Platform null `
 -RedirectUri null
```

- Convert the resource to JSON
```powershell
$OAuthAuthorizeRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

