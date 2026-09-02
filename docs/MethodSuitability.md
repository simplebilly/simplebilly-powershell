# MethodSuitability
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Carrier** | **String** |  | 
**Rate** | [**ShippingRate**](ShippingRate.md) |  | [optional] 
**Reasons** | **String[]** |  | 
**Service** | **String** |  | 
**Suitable** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$MethodSuitability = Initialize-PSOpenAPIToolsMethodSuitability  -Carrier null `
 -Rate null `
 -Reasons null `
 -Service null `
 -Suitable null
```

- Convert the resource to JSON
```powershell
$MethodSuitability | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

