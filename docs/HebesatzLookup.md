# HebesatzLookup
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Bundesland** | **String** |  | 
**CountryCode** | **String** |  | 
**GemeindeName** | **String** |  | 
**Gemeindeschluessel** | **String** |  | 
**HebesatzGewerbesteuer** | **Double** |  | 
**HebesatzGrundsteuerB** | **Double** |  | [optional] 
**Jahr** | **Int32** |  | 
**Landkreis** | **String** |  | [optional] 
**ValidFrom** | **String** |  | 
**ValidTo** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$HebesatzLookup = Initialize-PSOpenAPIToolsHebesatzLookup  -Bundesland null `
 -CountryCode null `
 -GemeindeName null `
 -Gemeindeschluessel null `
 -HebesatzGewerbesteuer null `
 -HebesatzGrundsteuerB null `
 -Jahr null `
 -Landkreis null `
 -ValidFrom null `
 -ValidTo null
```

- Convert the resource to JSON
```powershell
$HebesatzLookup | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

