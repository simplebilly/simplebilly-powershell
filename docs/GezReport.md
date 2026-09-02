# GezReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BeitragsfreieKfz** | **Int64** |  | 
**BeitragspflichtigeKfz** | **Int64** |  | 
**Betriebsstaetten** | [**BetriebsstaettenDetail[]**](BetriebsstaettenDetail.md) |  | 
**Hinweis** | **String** |  | 
**HotelzimmerBeitrag** | **String** |  | 
**JaehrlicherBeitrag** | **String** |  | 
**Jahr** | **Int32** |  | 
**KfzBeitrag** | **String** |  | 
**MonatlicherBeitrag** | **String** |  | 
**VierteljaehrlicherBeitrag** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GezReport = Initialize-PSOpenAPIToolsGezReport  -BeitragsfreieKfz null `
 -BeitragspflichtigeKfz null `
 -Betriebsstaetten null `
 -Hinweis null `
 -HotelzimmerBeitrag null `
 -JaehrlicherBeitrag null `
 -Jahr null `
 -KfzBeitrag null `
 -MonatlicherBeitrag null `
 -VierteljaehrlicherBeitrag null
```

- Convert the resource to JSON
```powershell
$GezReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

