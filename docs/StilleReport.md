# StilleReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Jahresueberschuss** | **String** |  | 
**Partners** | [**StillePartnerZeile[]**](StillePartnerZeile.md) |  | 
**Year** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$StilleReport = Initialize-PSOpenAPIToolsStilleReport  -Jahresueberschuss null `
 -Partners null `
 -Year null
```

- Convert the resource to JSON
```powershell
$StilleReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

