# TaxRateCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CountryCode** | **String** | ISO 3166-1 alpha-2 country code. | 
**EffectiveFrom** | **System.DateTime** | Date this rate took effect; &#x60;None&#x60; &#x3D; not date-bound. | [optional] 
**IsDefault** | **Boolean** | Default rate for the country (one per country); fallback for lookups when no dated rate applies. | 
**Name** | **String** | Human name, e.g. &quot;&quot;VAT&quot;&quot;. | 
**RatePercent** | **Int64** | Rate in hundredths of a percent: 1900 &#x3D; 19.00%. | 

## Examples

- Prepare the resource
```powershell
$TaxRateCreate = Initialize-PSOpenAPIToolsTaxRateCreate  -CountryCode null `
 -EffectiveFrom null `
 -IsDefault null `
 -Name null `
 -RatePercent null
```

- Convert the resource to JSON
```powershell
$TaxRateCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

