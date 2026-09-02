# ShippingCredentials
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Dhl** | [**DhlCredentials**](DhlCredentials.md) |  | [optional] 
**Ups** | [**UpsCredentials**](UpsCredentials.md) |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ShippingCredentials = Initialize-PSOpenAPIToolsShippingCredentials  -Dhl null `
 -Ups null
```

- Convert the resource to JSON
```powershell
$ShippingCredentials | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

