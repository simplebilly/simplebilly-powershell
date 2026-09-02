# BudgetErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Jahr** | **Int32** |  | 
**Monat** | **Int32** |  | 
**MonatsBudget** | [**BudgetKategorie[]**](BudgetKategorie.md) |  | 
**PrognoseRestjahr** | [**BudgetKategorie[]**](BudgetKategorie.md) |  | 

## Examples

- Prepare the resource
```powershell
$BudgetErgebnis = Initialize-PSOpenAPIToolsBudgetErgebnis  -Jahr null `
 -Monat null `
 -MonatsBudget null `
 -PrognoseRestjahr null
```

- Convert the resource to JSON
```powershell
$BudgetErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

