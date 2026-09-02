# GdprTenant
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **String** |  | 
**Role** | **String** |  | 
**TenantId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GdprTenant = Initialize-PSOpenAPIToolsGdprTenant  -Name null `
 -Role null `
 -TenantId null
```

- Convert the resource to JSON
```powershell
$GdprTenant | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

