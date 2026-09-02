# NotificationDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**Id** | **String** |  | 
**IsRead** | **Boolean** |  | 
**Message** | **String** |  | [optional] 
**SentViaEmail** | **Boolean** |  | 
**TenantId** | **String** |  | 
**Title** | **String** |  | 
**UserId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$NotificationDto = Initialize-PSOpenAPIToolsNotificationDto  -CreatedAt null `
 -Id null `
 -IsRead null `
 -Message null `
 -SentViaEmail null `
 -TenantId null `
 -Title null `
 -UserId null
```

- Convert the resource to JSON
```powershell
$NotificationDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

