# ShippingRate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Breakdown** | **String** |  | [optional] 
**Carrier** | **String** |  | 
**CrossBorderSurcharge** | **String** |  | [optional] 
**DestinationCountry** | **String** | ISO-2 code of destination country. | 
**EstimatedDays** | **Int32** |  | [optional] 
**FromApi** | **Boolean** | True when the rate was obtained via an API call rather than calculation. | 
**InsuredValue** | **String** |  | [optional] 
**IslandSurcharge** | **String** |  | [optional] 
**OriginCountry** | **String** | ISO-2 code of origin country. | 
**Rate** | **String** |  | 
**Service** | **String** |  | 
**VolumeDiscount** | **String** |  | [optional] 
**WeightKg** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$ShippingRate = Initialize-PSOpenAPIToolsShippingRate  -Breakdown null `
 -Carrier null `
 -CrossBorderSurcharge null `
 -DestinationCountry null `
 -EstimatedDays null `
 -FromApi null `
 -InsuredValue null `
 -IslandSurcharge null `
 -OriginCountry null `
 -Rate null `
 -Service null `
 -VolumeDiscount null `
 -WeightKg null
```

- Convert the resource to JSON
```powershell
$ShippingRate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

