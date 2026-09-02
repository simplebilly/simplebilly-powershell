# GdprNotification
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**Id** | **String** |  | 
**IsRead** | **Boolean** |  | 
**Message** | **String** |  | [optional] 
**TenantId** | **String** |  | 
**Title** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GdprNotification = Initialize-PSOpenAPIToolsGdprNotification  -CreatedAt null `
 -Id null `
 -IsRead null `
 -Message null `
 -TenantId null `
 -Title null
```

- Convert the resource to JSON
```powershell
$GdprNotification | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

