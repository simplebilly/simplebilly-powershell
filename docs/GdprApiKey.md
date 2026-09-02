# GdprApiKey
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**ExpiresAt** | **System.DateTime** |  | [optional] 
**Id** | **String** |  | 
**KeyId** | **String** |  | 
**Name** | **String** |  | 
**Revoked** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$GdprApiKey = Initialize-PSOpenAPIToolsGdprApiKey  -CreatedAt null `
 -ExpiresAt null `
 -Id null `
 -KeyId null `
 -Name null `
 -Revoked null
```

- Convert the resource to JSON
```powershell
$GdprApiKey | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

