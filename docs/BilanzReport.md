# BilanzReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Aktiva** | [**BilanzItem[]**](BilanzItem.md) |  | 
**Balanced** | **Boolean** |  | 
**GeneratedAt** | **String** |  | 
**Passiva** | [**BilanzItem[]**](BilanzItem.md) |  | 
**Period** | **String** |  | 
**TotalAktiva** | **String** |  | 
**TotalPassiva** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$BilanzReport = Initialize-PSOpenAPIToolsBilanzReport  -Aktiva null `
 -Balanced null `
 -GeneratedAt null `
 -Passiva null `
 -Period null `
 -TotalAktiva null `
 -TotalPassiva null
```

- Convert the resource to JSON
```powershell
$BilanzReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

