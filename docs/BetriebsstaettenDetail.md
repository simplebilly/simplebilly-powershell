# BetriebsstaettenDetail
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Beschaefigte** | **Int64** |  | 
**MonatlicherBeitrag** | **String** |  | 
**Name** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$BetriebsstaettenDetail = Initialize-PSOpenAPIToolsBetriebsstaettenDetail  -Beschaefigte null `
 -MonatlicherBeitrag null `
 -Name null
```

- Convert the resource to JSON
```powershell
$BetriebsstaettenDetail | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

