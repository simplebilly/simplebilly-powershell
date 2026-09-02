# EmissionEntry
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityValue** | **String** | Activity amount in &#x60;unit&#x60; (kWh, l, km, t, tkm, EUR). | 
**CategoryId** | **String** | GHG-Protocol category key, e.g. &quot;&quot;purchased_goods&quot;&quot;, &quot;&quot;business_travel&quot;&quot;. | 
**Description** | **String** |  | 
**EfSource** | **String** | Emission-factor source, e.g. &quot;&quot;UBA-2024&quot;&quot;, &quot;&quot;DEFRA-2024&quot;&quot;. | 
**EfVersion** | **String** |  | 
**Method** | [**EmissionMethod**](EmissionMethod.md) | &quot;&quot;activity&quot;&quot; | &quot;&quot;spend&quot;&quot; | &quot;&quot;supplier&quot;&quot;. | 
**Scope** | [**GhgScope**](GhgScope.md) | GHG scope: &quot;&quot;1&quot;&quot; | &quot;&quot;2&quot;&quot; | &quot;&quot;3&quot;&quot;. | 
**Tco2e** | **String** | Computed server-side: activity * factor / 1000, rounded to 4 dp. | 
**Unit** | **String** | Unit of the activity value. | 
**UpdatedAt** | **System.DateTime** |  | [optional] 
**Year** | **Int32** | Reporting year. | 

## Examples

- Prepare the resource
```powershell
$EmissionEntry = Initialize-PSOpenAPIToolsEmissionEntry  -ActivityValue null `
 -CategoryId null `
 -Description null `
 -EfSource null `
 -EfVersion null `
 -Method null `
 -Scope null `
 -Tco2e null `
 -Unit null `
 -UpdatedAt null `
 -Year null
```

- Convert the resource to JSON
```powershell
$EmissionEntry | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

