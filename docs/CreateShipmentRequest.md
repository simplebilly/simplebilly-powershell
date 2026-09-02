# CreateShipmentRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Carrier** | **String** | Carrier name as configured in shipping settings: &#x60;ups&#x60; or &#x60;dhl&#x60;. | 
**Service** | **String** |  | [optional] 
**WeightKg** | **Double** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$CreateShipmentRequest = Initialize-PSOpenAPIToolsCreateShipmentRequest  -Carrier null `
 -Service null `
 -WeightKg null
```

- Convert the resource to JSON
```powershell
$CreateShipmentRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

