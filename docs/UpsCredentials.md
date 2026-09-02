# UpsCredentials
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ClientId** | **String** | OAuth 2.0 client credentials from developer.ups.com. | 
**ClientSecret** | **String** |  | 
**ShipperNumber** | **String** | UPS account number; required for label creation, optional for rates/tracking. | [optional] 

## Examples

- Prepare the resource
```powershell
$UpsCredentials = Initialize-PSOpenAPIToolsUpsCredentials  -ClientId null `
 -ClientSecret null `
 -ShipperNumber null
```

- Convert the resource to JSON
```powershell
$UpsCredentials | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

