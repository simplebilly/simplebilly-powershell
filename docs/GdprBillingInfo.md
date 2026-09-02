# GdprBillingInfo
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CurrentPeriodEnd** | **System.DateTime** |  | [optional] 
**CurrentPeriodStart** | **System.DateTime** |  | [optional] 
**Plan** | **String** |  | [optional] 
**Status** | **String** |  | [optional] 
**TenantId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GdprBillingInfo = Initialize-PSOpenAPIToolsGdprBillingInfo  -CurrentPeriodEnd null `
 -CurrentPeriodStart null `
 -Plan null `
 -Status null `
 -TenantId null
```

- Convert the resource to JSON
```powershell
$GdprBillingInfo | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

