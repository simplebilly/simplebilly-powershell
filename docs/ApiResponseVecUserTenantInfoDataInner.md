# ApiResponseVecUserTenantInfoDataInner
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomDomain** | **String** |  | [optional] 
**Role** | **String** |  | 
**Subdomain** | **String** |  | [optional] 
**TenantId** | **String** |  | 
**TenantName** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ApiResponseVecUserTenantInfoDataInner = Initialize-PSOpenAPIToolsApiResponseVecUserTenantInfoDataInner  -CustomDomain null `
 -Role null `
 -Subdomain null `
 -TenantId null `
 -TenantName null
```

- Convert the resource to JSON
```powershell
$ApiResponseVecUserTenantInfoDataInner | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

