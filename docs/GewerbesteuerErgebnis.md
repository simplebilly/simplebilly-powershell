# GewerbesteuerErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Freibetrag** | **String** |  | 
**Gesamtbelastung** | **String** |  | 
**Gewerbeertrag** | **String** |  | 
**Hebesatz** | **String** |  | 
**Jahr** | **Int32** |  | 
**Koerperschaftsteuer** | **String** |  | 
**Land** | **String** |  | 
**Messbetrag** | **String** |  | 
**Steuer** | **String** |  | 
**SteuerArt** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GewerbesteuerErgebnis = Initialize-PSOpenAPIToolsGewerbesteuerErgebnis  -Freibetrag null `
 -Gesamtbelastung null `
 -Gewerbeertrag null `
 -Hebesatz null `
 -Jahr null `
 -Koerperschaftsteuer null `
 -Land null `
 -Messbetrag null `
 -Steuer null `
 -SteuerArt null
```

- Convert the resource to JSON
```powershell
$GewerbesteuerErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

