# TenantSettings
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CompanyType** | [**CompanyType**](CompanyType.md) |  | 
**DpaAcceptedAt** | **System.DateTime** |  | [optional] 
**DpaAcceptedBy** | **String** |  | [optional] 
**DpaVersion** | **String** |  | [optional] 
**Features** | [**AnyType**](.md) | Active feature toggles for the tenant. | 

## Examples

- Prepare the resource
```powershell
$TenantSettings = Initialize-PSOpenAPIToolsTenantSettings  -CompanyType null `
 -DpaAcceptedAt null `
 -DpaAcceptedBy null `
 -DpaVersion null `
 -Features null
```

- Convert the resource to JSON
```powershell
$TenantSettings | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

