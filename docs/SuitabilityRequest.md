# SuitabilityRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerAnnualVolume** | **Int32** |  | [optional] 
**Items** | [**CartItemInput[]**](CartItemInput.md) |  | 
**Recipient** | [**Address**](Address.md) |  | 
**VarSender** | [**Address**](Address.md) |  | 

## Examples

- Prepare the resource
```powershell
$SuitabilityRequest = Initialize-PSOpenAPIToolsSuitabilityRequest  -CustomerAnnualVolume null `
 -Items null `
 -Recipient null `
 -VarSender null
```

- Convert the resource to JSON
```powershell
$SuitabilityRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

