# GdprUsageEvent
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**EventType** | **String** |  | 
**Id** | **String** |  | 
**Quantity** | **Int32** |  | 
**TenantId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GdprUsageEvent = Initialize-PSOpenAPIToolsGdprUsageEvent  -CreatedAt null `
 -EventType null `
 -Id null `
 -Quantity null `
 -TenantId null
```

- Convert the resource to JSON
```powershell
$GdprUsageEvent | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

