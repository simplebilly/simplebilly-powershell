# UpdateTenantSettings
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CompanyType** | [**CompanyType**](CompanyType.md) |  | 
**Features** | [**PartialFeatureSettings**](PartialFeatureSettings.md) |  | [optional] 

## Examples

- Prepare the resource
```powershell
$UpdateTenantSettings = Initialize-PSOpenAPIToolsUpdateTenantSettings  -CompanyType null `
 -Features null
```

- Convert the resource to JSON
```powershell
$UpdateTenantSettings | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

