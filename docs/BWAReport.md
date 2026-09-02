# BWAReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Expenses** | [**BWAExpenses**](BWAExpenses.md) |  | 
**GeneratedAt** | **String** |  | 
**Period** | **String** |  | 
**Revenue** | [**BWARevenue**](BWARevenue.md) |  | 
**Summary** | [**BWASummary**](BWASummary.md) |  | 

## Examples

- Prepare the resource
```powershell
$BWAReport = Initialize-PSOpenAPIToolsBWAReport  -Expenses null `
 -GeneratedAt null `
 -Period null `
 -Revenue null `
 -Summary null
```

- Convert the resource to JSON
```powershell
$BWAReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

