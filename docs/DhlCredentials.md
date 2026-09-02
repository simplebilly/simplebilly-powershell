# DhlCredentials
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ApiKey** | **String** | DHL-API-Key from developer.dhl.com (required for tracking). | 
**ClientId** | **String** | Client credentials from the DHL developer app; required for label creation. | [optional] 
**ClientSecret** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$DhlCredentials = Initialize-PSOpenAPIToolsDhlCredentials  -ApiKey null `
 -ClientId null `
 -ClientSecret null
```

- Convert the resource to JSON
```powershell
$DhlCredentials | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

