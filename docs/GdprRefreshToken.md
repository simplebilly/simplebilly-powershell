# GdprRefreshToken
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**ExpiresAt** | **System.DateTime** |  | 
**Id** | **String** |  | 
**RevokedAt** | **System.DateTime** |  | [optional] 
**TenantId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GdprRefreshToken = Initialize-PSOpenAPIToolsGdprRefreshToken  -CreatedAt null `
 -ExpiresAt null `
 -Id null `
 -RevokedAt null `
 -TenantId null
```

- Convert the resource to JSON
```powershell
$GdprRefreshToken | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

