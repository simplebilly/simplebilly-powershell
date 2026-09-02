# GdprActivity
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Action** | **String** |  | 
**CreatedAt** | **System.DateTime** |  | 
**Description** | **String** |  | [optional] 
**Id** | **String** |  | 
**TenantId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GdprActivity = Initialize-PSOpenAPIToolsGdprActivity  -Action null `
 -CreatedAt null `
 -Description null `
 -Id null `
 -TenantId null
```

- Convert the resource to JSON
```powershell
$GdprActivity | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

